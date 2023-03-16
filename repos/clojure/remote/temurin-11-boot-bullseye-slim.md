## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:2f0fc9a2e2c407cc764f3931dbd606861de2b6a8c9015750b08097e361a59e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dabf8cea8ddd956ec877188900cac5029b079bd319c8c5c251570a4c559229c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289784794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b700c5d98bac50bd76d74218df1ab7e7e0ea49a6aba7c9437233d528eb0892`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 08:55:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 08:55:44 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Mar 2023 08:55:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Mar 2023 08:55:44 GMT
WORKDIR /tmp
# Thu, 02 Mar 2023 08:55:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2023 08:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Mar 2023 08:55:51 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Mar 2023 08:56:08 GMT
RUN boot
# Thu, 02 Mar 2023 08:56:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dab5aa68add03adf4167c255aa376340ee346e91dba8b80c08987b9f67e4026`  
		Last Modified: Thu, 02 Mar 2023 09:12:39 GMT  
		Size: 1.1 MB (1077401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095e04add91b422c5f50c4421ac4756ba99e5803bcb948d717c18d52ecd2b098`  
		Last Modified: Thu, 02 Mar 2023 09:12:42 GMT  
		Size: 58.8 MB (58820534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de1990ce51df905d1921566abc43da8031baf26e780b59d1f2ca47386d7ccf6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285190394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6711be6e1eaa5f94edfb4837fa32e14fe39da83596f58a19237f56eee379f0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:50:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:50:17 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 04:50:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 04:50:17 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:50:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 04:50:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 04:50:22 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 04:50:39 GMT
RUN boot
# Thu, 16 Mar 2023 04:50:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24983f114872d3707601b195a8d85154b14d2fd1a950b1b4ac09ec6e4e483d`  
		Last Modified: Thu, 16 Mar 2023 05:04:37 GMT  
		Size: 1.1 MB (1064603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca502a55c96622ae93d10635032edcf9e95ea15fba81245024e8449e6799596`  
		Last Modified: Thu, 16 Mar 2023 05:04:40 GMT  
		Size: 58.8 MB (58820444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
