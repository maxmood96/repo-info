## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:d40aaddf4b658773e205c0f0edbad346c109f008cb63792baf4368093d0f14db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:197e9eba87de2f6e3141628f0a207db9db0947f42174183342b4a65a4b2c5106
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236584391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e1d8030e6a3ceaab05a425e0fb2624cef23eefa4a6927c58b639dcfc146002`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:59:48 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:59:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:59:48 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:59:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:59:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:59:54 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:00:14 GMT
RUN boot
# Thu, 11 Jan 2024 05:00:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3cc2ec75d8b129c72c5b98f89baa3d457733324b121efea02a41561fa9f6a0`  
		Last Modified: Thu, 11 Jan 2024 05:18:29 GMT  
		Size: 1.1 MB (1079468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa1d82d20f57c0cfe7b1e6a26098ab473b36a8d624ec712a55e45c3d044d942`  
		Last Modified: Thu, 11 Jan 2024 05:18:32 GMT  
		Size: 58.8 MB (58820631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7ec8dbfaa5fa73cab5b70a18cd24b90fd12e1e7ed042362162aa46997fa5681
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231953201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f1c7d59694bf0bacb37f960dce9a73f1328c9d8d6cc49a68f7365d754b7ddb`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 03:01:51 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:00:27 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:00:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:00:27 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:00:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:00:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:00:49 GMT
RUN boot
# Tue, 19 Dec 2023 07:00:49 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9b17def4f28a4c890f414b976902690074fb9a259e92623f2bce7129f95d48`  
		Last Modified: Tue, 19 Dec 2023 03:04:57 GMT  
		Size: 142.0 MB (142001838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06b109f39d5ea0094941274b7964f8e2204f1a168d38401e651a6d636cee6f4`  
		Last Modified: Tue, 19 Dec 2023 07:16:31 GMT  
		Size: 1.1 MB (1066810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8b9c6fec3690feac5ffcfa00f8500a569e336835f0dae3b3e6b2706c0002ea`  
		Last Modified: Tue, 19 Dec 2023 07:16:34 GMT  
		Size: 58.8 MB (58820501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
