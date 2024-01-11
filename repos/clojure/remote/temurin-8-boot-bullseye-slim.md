## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:7af9805a7f93fc92d41eacdabb9748e511038704c74fd97b1bf31c0f0a212c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:76dd71be58d5d5e55d30755384577da084981fe117b0a95db4554a72629855c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194916254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2aaecbb9be144c4a46611b8b9e14c8b85fb5568a61f4efa096e9b9d3fd8fa6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:54:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:54:01 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:54:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:54:01 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:54:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:54:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:54:07 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:54:28 GMT
RUN boot
# Thu, 11 Jan 2024 04:54:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174aa11106f2d3d4da01484fac2da5df4e3ce9ec4196afe1ba0d6908551deaf2`  
		Last Modified: Thu, 11 Jan 2024 05:15:12 GMT  
		Size: 103.6 MB (103598261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a2edf9d38b86b998b45d47df1284a64099e053932b3d71fee8174589c6fe5`  
		Last Modified: Thu, 11 Jan 2024 05:15:04 GMT  
		Size: 1.1 MB (1079493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15109adb220834a2f05b4d7784c3b8feaf114b9d2c9c55564b1b9e90c31017ef`  
		Last Modified: Thu, 11 Jan 2024 05:15:07 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de03e0aa48f4ef5f074c5eb5c4f1f23fc733a7db824308575d427a6d9c9a3799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192652803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5028fcc577261bc47d168d1641521f6bc8cccab85e23c30db1777bc5ab98c9fa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:55:48 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:55:50 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:55:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:55:50 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:55:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:55:55 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:56:12 GMT
RUN boot
# Tue, 19 Dec 2023 06:56:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8460c2429b384c138ca104a8d205038e1877169d7a2d55c0430c97fdacb19c12`  
		Last Modified: Tue, 19 Dec 2023 07:13:30 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5605ae6b7e71b74e3ff77b98011364d9ce7ba940c2c1f4ce8968b34911765fc1`  
		Last Modified: Tue, 19 Dec 2023 07:13:23 GMT  
		Size: 1.1 MB (1066838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efa6c46d6810ba6f00c1a865ba87daa0a3fa5cdfd82e9d8525e0d457ae61c7b`  
		Last Modified: Tue, 19 Dec 2023 07:13:27 GMT  
		Size: 58.8 MB (58820375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
