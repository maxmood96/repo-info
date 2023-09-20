## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:09615d144a9b131665a00b8822ff39bcaca5a0a84cfb041f0e8c8ea2121358de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3dcf8c3703e4df0c8be0924dab60ef9bc7ff1da3cd55658b1c19c8fca1434330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236141856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80a1aaa53920e964edb3a8bd0bb9e6a9840931c73a395a872896fa13b8859cc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:25:26 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:25:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:25:27 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 20 Sep 2023 07:25:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:25:27 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:25:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 20 Sep 2023 07:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:25:33 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 20 Sep 2023 07:25:52 GMT
RUN boot
# Wed, 20 Sep 2023 07:25:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386a93addc060819e53101917ea458e4b015b760aeb9ab2f21c38b4ff88c1e7d`  
		Last Modified: Wed, 20 Sep 2023 07:35:54 GMT  
		Size: 144.8 MB (144826040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79cd3742f41dd715bd5934214e9276cd1aa2f6cf4062fdbf7003448a4c298b9`  
		Last Modified: Wed, 20 Sep 2023 07:35:43 GMT  
		Size: 1.1 MB (1077533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b9523b5f9ef6e3a15a67953d6e98893aaeebd55ad4a1d415b910327d7ccf5c`  
		Last Modified: Wed, 20 Sep 2023 07:35:47 GMT  
		Size: 58.8 MB (58820572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:999acd17216707036a473ffbbd2a1845b8fdd5a5bac8d4fa6179b9c0a73a489a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231518520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f2059fed78f5cfe86284e01b26f220946ccb67fd589c9a8eeb2b0d29b18b0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 06:47:24 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:07:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:07:09 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 09:07:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:07:09 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:07:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 09:07:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:07:14 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 09:07:32 GMT
RUN boot
# Thu, 07 Sep 2023 09:07:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b018ed6a392610f1ab69e85cc642842b49d22521199586d6067dfd326f17f2`  
		Last Modified: Thu, 07 Sep 2023 06:49:54 GMT  
		Size: 141.6 MB (141570382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1b02bec70918e3ed138026de64cfaff1608af9031a657fbb661b095238b03a`  
		Last Modified: Thu, 07 Sep 2023 09:16:12 GMT  
		Size: 1.1 MB (1064804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea4d7e18efa87880c0d0797cbbe61f3dc242d0897dcfb467b9505957310b5d8`  
		Last Modified: Thu, 07 Sep 2023 09:16:15 GMT  
		Size: 58.8 MB (58820431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
