## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:f57e968ae55656d4d76eb00ec63b07448dfa886ac539dc99f982589efed8ce13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:34a9912925b817f4471034818e4aa8e93bdd47bb4126914e3bbd1f5b5a2b2a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194912477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b759d3a8c8cef1fb7682b2aa9ebac6ba13c64bf8183c28e634ad12e25a98e0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:48:40 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:48:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:48:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:48:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:48:41 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:48:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:48:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:48:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:49:06 GMT
RUN boot
# Tue, 13 Feb 2024 01:49:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41190a3d826a196367bcb15e909443c6b1b2fc4d1bedc92ad3a5af7d1024b2f0`  
		Last Modified: Tue, 13 Feb 2024 02:10:21 GMT  
		Size: 103.6 MB (103591873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5833b632753489d9fb42950d3a16d1b2615988e6ae360c6113e41bd913550078`  
		Last Modified: Tue, 13 Feb 2024 02:10:13 GMT  
		Size: 1.1 MB (1077690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f487a7b5ce06bffb75b7af806830a50a87417593087c61a56b0e2487d1fb701`  
		Last Modified: Tue, 13 Feb 2024 02:10:16 GMT  
		Size: 58.8 MB (58820489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5459c6ef9bcfbec46822a00a4c9d249b3dd6617b43a46e1a03c7e3eeed7138db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192659666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b669f2188e56f56e7dbd7d4336ecf1083473b7f666e95d2acc4ac5a70d3a0a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:56:09 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:56:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:56:12 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:56:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:56:12 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:56:17 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:56:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:56:17 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:56:35 GMT
RUN boot
# Tue, 13 Feb 2024 01:56:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea3d69331c927f1edd5e6701c7ee5ffad7bafc5ff2fd996c1c29854bfa9beea`  
		Last Modified: Tue, 13 Feb 2024 02:14:35 GMT  
		Size: 102.7 MB (102703041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a52fdfa25ef43096aaf64f1bd2df74d4eef7494e4558a7c61b83ba27b3322ad`  
		Last Modified: Tue, 13 Feb 2024 02:14:29 GMT  
		Size: 1.1 MB (1064999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166aec1401a302a1bd585f104920e3cd28d2b036f0c64cfd641c1aeeade934d0`  
		Last Modified: Tue, 13 Feb 2024 02:14:32 GMT  
		Size: 58.8 MB (58820549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
