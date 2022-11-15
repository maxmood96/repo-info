## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:36722f94c1e954787e1277ca14e42d515e8d856692d2481554c75fd60f148c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:518ec3b7ab5f023f926ad264d8a4962f0c7db9cbe68c6a436b6d871aeef1ef22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314676881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0eea929b3c64a073e89c536829bed2486d89d77569c6ad84b5760c0cc1b54d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:54:03 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:54:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 17:54:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:54:05 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:54:11 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 17:54:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:54:12 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 17:54:31 GMT
RUN boot
# Tue, 15 Nov 2022 17:54:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b1d80bdfeef6cb6cdf5a91dce43100373840e0ed893c308f6732d8bf622362`  
		Last Modified: Tue, 15 Nov 2022 18:08:18 GMT  
		Size: 198.5 MB (198455814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423cc6b4ed8ad83395417c3dfb3306a8acaf0d1006e179c8c941af4d93c14dc6`  
		Last Modified: Tue, 15 Nov 2022 18:08:03 GMT  
		Size: 2.4 MB (2361935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29586a0c8998ed420a240cef1ed64120a0db075517d83e4640e4268f0af5f695`  
		Last Modified: Tue, 15 Nov 2022 18:08:06 GMT  
		Size: 58.8 MB (58820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9774748a79fcee05b051f49a9582010bac979beaa21b5a61204be2342cc6e790
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310073610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce19581599e1788d11e9b004db37c17642a9d723a8170e492c08f8a76ee5b649`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:26 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:51:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:51:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:51:31 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:51:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:51:36 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:51:53 GMT
RUN boot
# Tue, 15 Nov 2022 05:51:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6410c82310e7ed376d2f9bdb09d5bba8c5586def41b40a45fc26ed1c405a8a0`  
		Last Modified: Tue, 15 Nov 2022 06:03:10 GMT  
		Size: 195.2 MB (195201165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bccdd89e8887895edda6c63975314da5e866d4fd2b6e5b584d4cd825750876`  
		Last Modified: Tue, 15 Nov 2022 06:02:59 GMT  
		Size: 2.4 MB (2352268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd21132d1d7fcdb2ba6ea807bc54421c634950afd8075505681b5bec14d41b5`  
		Last Modified: Tue, 15 Nov 2022 06:03:01 GMT  
		Size: 58.8 MB (58820315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
