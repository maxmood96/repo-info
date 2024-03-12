## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:097beaa68f13cbca630ae6d6ebc36f822d83f5a5832e0c7dfadb6a87aa0cd6f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

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

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d12b0094d5949d746a8486d502643770e2f36c342a6379da63ff14a0ec4b1cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231965018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2171b8f31314d73ea892efa419fdd66bd280b3295d2f9e2ee68a07a2a5aa20b8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:50:05 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:50:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:50:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:50:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:50:08 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:50:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:50:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:50:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:50:31 GMT
RUN boot
# Tue, 12 Mar 2024 01:50:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb450795f7ec7c9a3f449d4b89a1813bc06e338a4ccecb2a734b6e798364b28a`  
		Last Modified: Tue, 12 Mar 2024 02:06:35 GMT  
		Size: 142.0 MB (142008478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb498ff3e7f054097bf8efaa59b55a2af4ce44011a3966cf1f39d886c06d0474`  
		Last Modified: Tue, 12 Mar 2024 02:06:25 GMT  
		Size: 1.1 MB (1064958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d867fa9417d560678297c363c1216bda3b605aa61370657ac87f5267ddd7ca66`  
		Last Modified: Tue, 12 Mar 2024 02:06:28 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
