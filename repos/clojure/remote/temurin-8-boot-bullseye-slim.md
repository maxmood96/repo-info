## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ca4fc548e47a0484399b5a59d206d074cdae5eec90ce83e13df6eedb9d57ff5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

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

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2c96a508b50a67105a84d5beae5eeda3df8a1fedeb0ea42eda5e8c4db11f783
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143691003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069bec405ad299afd83c8232feccae80d9321e6684af9a808489ffc2cf80fdf2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:44:12 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:44:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:44:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 06:44:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 06:44:13 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 06:44:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 06:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 06:44:18 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 06:44:36 GMT
RUN boot
# Tue, 04 Jul 2023 06:44:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b2f40633878980b926bd5c39f216162f482779ac62dfe05a4cac4558cd3356`  
		Last Modified: Tue, 04 Jul 2023 06:53:48 GMT  
		Size: 53.7 MB (53742698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2309eeb9dfd8fef77e4f5dcf3108410d58724574a8a8858af1bbdf84760089`  
		Last Modified: Tue, 04 Jul 2023 06:53:53 GMT  
		Size: 1.1 MB (1064794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b6a22a96e076ccf1330dac1b58b86017439a1ff0ec93a0b946b8fb38a0951d`  
		Last Modified: Tue, 04 Jul 2023 06:53:46 GMT  
		Size: 58.8 MB (58820554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
