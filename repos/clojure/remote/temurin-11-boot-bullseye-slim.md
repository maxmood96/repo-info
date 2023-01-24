## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ae54601c5d465a7b530dae09c3782ad69b443ccdbc86029a4cb5fa2bf5838d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f0b5f84eebb7e0bc811afb2e4bd8d3f9878587c22438c09d7980f55074d80b1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289749333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e420ef85380e13d7b22e499f2c270f7968c3e95298684ce3e4ba698e09a770`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 03:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 03:23:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Jan 2023 03:23:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Jan 2023 03:23:12 GMT
WORKDIR /tmp
# Wed, 11 Jan 2023 03:23:17 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Jan 2023 03:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Jan 2023 03:23:17 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Jan 2023 03:23:36 GMT
RUN boot
# Wed, 11 Jan 2023 03:23:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8aacbdc703fb8bffb366db7bad141878085908a64edbb70ddec167ec5a1a1c`  
		Last Modified: Wed, 11 Jan 2023 03:36:28 GMT  
		Size: 1.1 MB (1077331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bceaf651a1403e224031700cb4daec4ed1daf0c5305a61ad234a31fca269ab`  
		Last Modified: Wed, 11 Jan 2023 03:36:31 GMT  
		Size: 58.8 MB (58820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f45276edf13ffe3d65402ff6175ebb86fc51471fe6cfef69f5bab2625adfee21
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285170144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c716fc9852539ffb7058179ec11a933a4fba547b679fccfb211affbb9ba21`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 20:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 20:59:26 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 24 Jan 2023 20:59:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 24 Jan 2023 20:59:26 GMT
WORKDIR /tmp
# Tue, 24 Jan 2023 20:59:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 24 Jan 2023 20:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Jan 2023 20:59:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 24 Jan 2023 20:59:48 GMT
RUN boot
# Tue, 24 Jan 2023 20:59:49 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257f3874deacd852098d12ec60f0387aa6d44fe361429d767ebf2a9878f99aa4`  
		Last Modified: Tue, 24 Jan 2023 21:10:50 GMT  
		Size: 1.1 MB (1064700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82945f3b56ad30b1739c413cd07233b81a9b21ac6a32ba8944399ab5f47bb38b`  
		Last Modified: Tue, 24 Jan 2023 21:10:53 GMT  
		Size: 58.8 MB (58820677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
