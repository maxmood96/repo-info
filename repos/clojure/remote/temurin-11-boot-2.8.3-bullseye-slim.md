## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:909fc0bb62481d3be62558daeb92e6ce4d60d00912c35dfb4bfb4e837f85e7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b15b61999ae9d1ba93fb14cc75119ff2e9222a45c561794edc99f7c5c074b265
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289768014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767d9973d6850955a44e8080ba4376a6562ab7eea45fca248aa38a727d7ba4ae`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:54:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:54:40 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 17:54:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:54:40 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:54:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 17:54:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:54:46 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 17:55:06 GMT
RUN boot
# Tue, 15 Nov 2022 17:55:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425b609a0283725ecedc5fbc22ee9f28708bd5f04fa72a6680005f8e401d57`  
		Last Modified: Tue, 15 Nov 2022 18:08:27 GMT  
		Size: 1.1 MB (1079009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb531d152d8673156c1bbe393745dc012e7c328c205d8fd1ab40142feac30951`  
		Last Modified: Tue, 15 Nov 2022 18:08:30 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7806b1000e117467ef37f3ada444c833d4c49dbf9aa2edca6c27f0ed30413fd2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285148596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85848e7b1ece374ef8c43a68e7e54f128f0b9e15e4080a0b8c1bb913a03c7ffa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:59 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:52:04 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:52:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:52:04 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:52:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:52:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:52:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:52:26 GMT
RUN boot
# Tue, 15 Nov 2022 05:52:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cde71cdd6ac565f043bc4ec8903ab809981c13bc3c9e55dd5b7290a1bb0801`  
		Last Modified: Tue, 15 Nov 2022 06:03:30 GMT  
		Size: 195.2 MB (195201143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca3e675ac3bcfefb13e5fddac98a1a8446aae135c4d4df761f78af5a552c9b1`  
		Last Modified: Tue, 15 Nov 2022 06:03:19 GMT  
		Size: 1.1 MB (1066312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d86afbd018281c8beebe8a01f262ccdbc90e73c267fdfda166fad1fb672a616`  
		Last Modified: Tue, 15 Nov 2022 06:03:21 GMT  
		Size: 58.8 MB (58820536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
