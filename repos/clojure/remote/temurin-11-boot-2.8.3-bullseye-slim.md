## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:6db3d23fcad15da16feb274d907a053764d59335f3194c6e6968a6abb3d2586a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8ea9ccd16526458e5431e826b1b46204a6c30980d3090b9a56462e1218f18bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289784906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b8ea06721fa6235f589fcb5bf0445c12159b12ed84a420732a03fc2cc2bd2d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:44:16 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:44:18 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:44:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:44:19 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:44:24 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:44:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:44:25 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:44:43 GMT
RUN boot
# Wed, 01 Mar 2023 07:44:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56844ef93a6b4ee76d993441c680d901208ad2f1618368d240a20da46ff08911`  
		Last Modified: Wed, 01 Mar 2023 07:57:07 GMT  
		Size: 198.5 MB (198475514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ead91513c976b545622aad0f1ef9cc79a9010887628f9c6d18ca3114af8a0`  
		Last Modified: Wed, 01 Mar 2023 07:56:53 GMT  
		Size: 1.1 MB (1077383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24a8be780e65ba2adc582d1df641ca2c35e80b5703d264d70bcc40edee70583`  
		Last Modified: Wed, 01 Mar 2023 07:56:57 GMT  
		Size: 58.8 MB (58820606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d17ca57f1e81afb4223976b7a04ab1d098e00e7708b8cac656d2e567ef38c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285188306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4391d0ef7eb21bbf92dfb43ee5043e18f02a48775718ae307e06a0f6f65e0aa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:04:34 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:04:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:04:38 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:04:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:04:38 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:04:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:04:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:04:44 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:05:01 GMT
RUN boot
# Wed, 01 Mar 2023 03:05:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98c705f083b7d7e1bef89e4744939ae93866db4876e439d400bf551560d2010`  
		Last Modified: Wed, 01 Mar 2023 03:16:00 GMT  
		Size: 195.2 MB (195240377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d495ae96fb2d6b3a0e40fff1bbd69c39310f29fb6df0c4514776e9559ff3e4`  
		Last Modified: Wed, 01 Mar 2023 03:15:50 GMT  
		Size: 1.1 MB (1064592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd9b6cc3f6b221c6b279b5667b9f6bc6da1a61615d5345bfc10175072bf1bb`  
		Last Modified: Wed, 01 Mar 2023 03:15:53 GMT  
		Size: 58.8 MB (58820523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
