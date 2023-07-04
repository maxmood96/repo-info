## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:950205fb52540a42954bcd9b7e1b5b6498d1dfee17149c6c6c7f5d86b006a4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7d83fbbdd3eb52d58a26edbd5e5bc4b9f52ef5904193d6dd04bbfbc4a14dfa02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308818555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f509d593bfffadbec94a2ee801b67871761b3a08d34cbdee31e0b40953dbd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:05:49 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:05:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:05:51 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:05:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:05:51 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:05:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:05:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:05:57 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:06:14 GMT
RUN boot
# Tue, 04 Jul 2023 04:06:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 04:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 04:06:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d5749ce62c0fb43ce9ee4298e4f571f0584facdde1f4b6b77b68dcf21129c2`  
		Last Modified: Tue, 04 Jul 2023 04:15:06 GMT  
		Size: 192.6 MB (192580329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867a42286c8fd64788bcca9ecdbc386ad3706ec5ab9af2f0b17a4c49597bce42`  
		Last Modified: Tue, 04 Jul 2023 04:14:54 GMT  
		Size: 2.4 MB (2361998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f131ac5030f2260ecf46ebac6600983427ef72bf57ed714fb3e3e3f068a602`  
		Last Modified: Tue, 04 Jul 2023 04:14:56 GMT  
		Size: 58.8 MB (58820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86200f2de86cafe4a518ec081a6f7b8d8286bbba1570314c826c5a43e6d629f3`  
		Last Modified: Tue, 04 Jul 2023 04:14:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6411c8fa1af47017998a971e46d5d74cc4af554e980329da73d84adbbea29cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306263931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d42ee4c7dc2fe1b83e1ea78ac48188103d64aa809c7a5afe3cd8edb0eeb3431`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:46:29 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:46:33 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 04:46:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 04:46:33 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:46:38 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 04:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 04:46:38 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 04:46:56 GMT
RUN boot
# Fri, 16 Jun 2023 04:46:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Jun 2023 04:46:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jun 2023 04:46:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172252176b2d2b44f66626001ffedf36355c238558bbc403980303e6b6c92ae9`  
		Last Modified: Fri, 16 Jun 2023 04:56:58 GMT  
		Size: 191.4 MB (191387640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d209f9a9a585297e98927ab8aece778729273ea765bf993bb6486bf27fb93c`  
		Last Modified: Fri, 16 Jun 2023 04:56:47 GMT  
		Size: 2.4 MB (2351326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7b155d8f7d2e9e0af3797d52f2d75d2183be3414ac33775d731a870d7199d0`  
		Last Modified: Fri, 16 Jun 2023 04:56:50 GMT  
		Size: 58.8 MB (58820431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29a311b04bd6c06a341b1cb4a27fae423071a6c36312dead7470b3f4208df1d`  
		Last Modified: Fri, 16 Jun 2023 04:56:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
