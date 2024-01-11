## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:b6b972aef8edfaacada70ed93a28dd6e2a6a0e146297f7cfd51e8b1859d73966
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
$ docker pull clojure@sha256:46e5d563496208266e41d008910614bff53bd75e5908ba28889008f05bf79262
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231953242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c34555b8f6013d5b541fdaeb428e85c661ad2a466fc6465d7bd1e02c9927eef`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:05:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:05:34 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:05:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:05:34 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:05:38 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:05:39 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:05:57 GMT
RUN boot
# Thu, 11 Jan 2024 08:05:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d30fd9fd0af76cc6c927a5fdc13d016cbe3fbf4d812fa6301451faa6686bd4`  
		Last Modified: Thu, 11 Jan 2024 08:21:38 GMT  
		Size: 1.1 MB (1066828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b13f9e5ac69cee31b3f54b650464a4c3c7108e0449901f1acc395dfe00b6f13`  
		Last Modified: Thu, 11 Jan 2024 08:21:42 GMT  
		Size: 58.8 MB (58820568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
