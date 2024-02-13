## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:920e2a8f1a649b60686230fed4ae9fcc805988a76597d7ecd4e7e4bd5536901a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b9a16f4c2d9834f2f9fec35116577725d00fb1ae8a49922c70566f166035cf75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236591649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0c0113a08ee558657a79b2202fe4645da98e97c7eb70d50cc77da66d8f46c3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:54:29 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:54:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:54:30 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:54:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:54:30 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:54:36 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:54:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:54:36 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:54:56 GMT
RUN boot
# Tue, 13 Feb 2024 01:54:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1987d360c04f1cbea8ebe89aef06d9a25692e56c8318d3d7ebfb1237db6ad13`  
		Last Modified: Tue, 13 Feb 2024 02:13:54 GMT  
		Size: 145.3 MB (145271024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1117889304c3482d6dd1fbe7a58ea3ab613b819ed097a416a6245bdf05408c3`  
		Last Modified: Tue, 13 Feb 2024 02:13:42 GMT  
		Size: 1.1 MB (1077681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62d359dd0de1d06ae2102894177c84e37b97572b2d48325b38445acad028199`  
		Last Modified: Tue, 13 Feb 2024 02:13:45 GMT  
		Size: 58.8 MB (58820519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2c308ae01bee94aa3a15f06c74d237a83b4bb5eba38af8d1146c705eb6094bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231962962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6175f7228d2e540ae5c098ed916b8bcecc1dee09833194a966211f37f1d24a1b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:01:10 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:01:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:01:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:01:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:01:13 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:01:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:01:18 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:01:36 GMT
RUN boot
# Tue, 13 Feb 2024 02:01:36 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c411c25b52a8957cc5d7d5d564cac17873d0ca75b01912abc1217e5b3ed65c4`  
		Last Modified: Tue, 13 Feb 2024 02:18:07 GMT  
		Size: 142.0 MB (142006401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e686563ece7f152806160d3fb904c58eb0363e5374d4fe3083afb90ef6af4e`  
		Last Modified: Tue, 13 Feb 2024 02:17:58 GMT  
		Size: 1.1 MB (1065001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773a4f161eaecde555f8f78ce03c88bcb5ec575beee936577365244d500ea761`  
		Last Modified: Tue, 13 Feb 2024 02:18:01 GMT  
		Size: 58.8 MB (58820483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
