## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ce3d4ff5ebbbb7d75aece634fc08373d6f2f575cc5a03ec344c4d91b1c4328de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d255638195f196d7b29e2eb622c1ee96ad649fb10302592b332c635ffb916b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289865584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fcde7671c693215e0418429efd3e7d8c2d3ce9ebc230c780f6026d383c0e79`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:04:09 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:04:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:04:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Apr 2023 20:04:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Apr 2023 20:04:11 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:04:16 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Apr 2023 20:04:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Apr 2023 20:04:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Apr 2023 20:04:34 GMT
RUN boot
# Wed, 26 Apr 2023 20:04:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4732512befd268374b48fb0d71e1d7b92ee077512c8190c2a7378323351f7fb`  
		Last Modified: Wed, 26 Apr 2023 20:21:00 GMT  
		Size: 198.5 MB (198549520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f26673e206eb87dd67eb7d812af2c81d99b21f112a00c9da789b3a38de139ff`  
		Last Modified: Wed, 26 Apr 2023 20:20:46 GMT  
		Size: 1.1 MB (1077496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14711f38ba35c2366bcd02c934d3d8fd7ea2eb41df9c3a358c2a67a6bc9e106c`  
		Last Modified: Wed, 26 Apr 2023 20:20:49 GMT  
		Size: 58.8 MB (58820340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ee9f3c594c386a04912a1f4b95548b393b61854f5a80952e29c19ecab7c3c36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285262228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa86cdff8c5f350c6073a90b1909a04e40913dc53924187eca2e75bfc931bbf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:46:48 GMT
COPY dir:8d5d0106b2c3fe64c4905be44080473b7828ffb48e0e107739a7ba7a3cb627cf in /opt/java/openjdk 
# Wed, 03 May 2023 17:46:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:46:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:46:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:46:53 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:46:57 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:46:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:47:14 GMT
RUN boot
# Wed, 03 May 2023 17:47:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fdca64c090abce4b51b43574d16ea2ef8901894d1cc771bbedb52a44a6ba3`  
		Last Modified: Wed, 03 May 2023 17:55:07 GMT  
		Size: 195.3 MB (195324206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e21c4f7f6f66746942a54c8132eb0b7aea45b1c53ba007e7159990576759b`  
		Last Modified: Wed, 03 May 2023 17:54:56 GMT  
		Size: 1.1 MB (1064802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a21b480297cfa2fb1950636dd7a7684e28fb418551af924f2add576777ddf2`  
		Last Modified: Wed, 03 May 2023 17:54:59 GMT  
		Size: 58.8 MB (58820487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
