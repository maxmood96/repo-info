## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:1a06008cebcf84df6d81e6ac019ddb0c8cddaa6266099211d65280641ba3418d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6d13d7847bcf5e9de5292ba550f43ae71c73169092f4d8d7386240d63d2009f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145957674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b10872cfac6116a405800854b541c895882cf2087645832e8ac86b25793d241`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:00:25 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:00:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:00:25 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:00:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:00:26 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:00:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:00:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:00:50 GMT
RUN boot
# Tue, 04 Jul 2023 04:00:50 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccffc950a8b498b94fe1759b3349b3af9e7c64526ddf777677aa45c612160b7`  
		Last Modified: Tue, 04 Jul 2023 04:11:59 GMT  
		Size: 54.6 MB (54642103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93fa21beb99102d732ff5c8ccb15cb8a91ffed5d5b69862b5d55012c2b3244b`  
		Last Modified: Tue, 04 Jul 2023 04:11:53 GMT  
		Size: 1.1 MB (1077536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b85a5eed49171da9007eda97ac7ee4fc14a4e7b09fa6c91a1bbe2de1b0dce17`  
		Last Modified: Tue, 04 Jul 2023 04:11:56 GMT  
		Size: 58.8 MB (58820647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c0121184129b872dcd44625b9b28fdac630b3414f13128483c76a577d72846ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143690826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4feb9b38699c2da5e6ccba3bc24031e0595af74d871e6e72780296616f61b650`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jun 2023 04:51:12 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 13 Jun 2023 04:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:51:14 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Jun 2023 04:51:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Jun 2023 04:51:14 GMT
WORKDIR /tmp
# Tue, 13 Jun 2023 04:51:19 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Jun 2023 04:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jun 2023 04:51:19 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Jun 2023 04:51:38 GMT
RUN boot
# Tue, 13 Jun 2023 04:51:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c42dbe9973fad0e5db82fff74ab48ee24033b2296cd2ca6fdcba69bad893d2`  
		Last Modified: Tue, 13 Jun 2023 05:00:32 GMT  
		Size: 53.7 MB (53742662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9b6fcda3aedb785b8140b3f436e957c38f2432ef3105ba11c8c424ad63e8c`  
		Last Modified: Tue, 13 Jun 2023 05:00:28 GMT  
		Size: 1.1 MB (1064827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f65ac90055caa13ed11c5ea58aaa9733282740c60dce501ac500e80018950`  
		Last Modified: Tue, 13 Jun 2023 05:00:30 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
