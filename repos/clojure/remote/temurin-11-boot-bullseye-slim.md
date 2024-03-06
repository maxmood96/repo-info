## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:418d7feca6e99e0a7e89ddf9a49fd3d9eb77486adc33319ffd032bd1f97e1b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f67fd36547b36ecf14d5f10fcc1c68a1129bec3b2bcc49d2984caad9bebb5ab9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236591803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eeee03e4dffac78b20000b026e6a431bb0250cf33225072e740a7d4f0bb54d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:03:14 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:03:16 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:03:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:03:16 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:03:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:03:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:03:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:03:42 GMT
RUN boot
# Wed, 06 Mar 2024 14:03:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81ae9e98f49cc29c0ab057f1252129d8ce2d72eb0e68b0cc28dea6a0f9685dd`  
		Last Modified: Wed, 06 Mar 2024 14:23:57 GMT  
		Size: 145.3 MB (145271155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca705b0e228c48e00995646a92dc2a76bb1e689377a800f8feb8194aa37f4aef`  
		Last Modified: Wed, 06 Mar 2024 14:23:46 GMT  
		Size: 1.1 MB (1077696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c0afdd05cc08d7e2984bcedfcf58bd15dd4e11c0c44e182a4dce9e408633c`  
		Last Modified: Wed, 06 Mar 2024 14:23:49 GMT  
		Size: 58.8 MB (58820527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7d725e88ab85dadcec2a393e60f556fb33fca069c781d8543b14f52eff1b32a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7a7e429182fcd7e16d8af530cca9ce106460b3e27773e6f35e4c2ff70ea697`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:17:20 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:17:23 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:17:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:17:23 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:17:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:17:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:17:47 GMT
RUN boot
# Wed, 06 Mar 2024 13:17:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e29c8b4b8407175ca98aa52e0e9c0ab05943a911b8f39dda5790f1454c2e6d`  
		Last Modified: Wed, 06 Mar 2024 13:34:32 GMT  
		Size: 142.0 MB (142008478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae72fcf629e8c4fb1d0483f7b41ea64ccc725c27276daa391cdc4a614439fddc`  
		Last Modified: Wed, 06 Mar 2024 13:34:24 GMT  
		Size: 1.1 MB (1064999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee7416285a212b0821102235e9578f7e5070507643b43cc93b84ce4d691a6ac`  
		Last Modified: Wed, 06 Mar 2024 13:34:26 GMT  
		Size: 58.8 MB (58820551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
