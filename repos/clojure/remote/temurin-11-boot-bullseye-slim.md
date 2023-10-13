## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ddfa709a7100f353d697ea16f2ff75b0d0888499fbec8fc9ecd8353be0916a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3d1b396c4df69e9301778aeedf7f7c57e23353d71c75d1e796929cacae861633
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236143565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b355ddde90ea5add40a9f4e70871252e0b8f0465a63626852f109b72c331e028`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:54:57 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:54:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:54:58 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:54:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:54:58 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:55:04 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:55:04 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:55:21 GMT
RUN boot
# Wed, 11 Oct 2023 18:55:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c7d268b2d9d763f0e7dc3a3f3a3b314da393f08674da13cc1c53288c04fb75`  
		Last Modified: Wed, 11 Oct 2023 19:05:37 GMT  
		Size: 144.8 MB (144825963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8198f7b662f3898a262391355e9484f275a3bfe7b70f77f70599657d2997d2`  
		Last Modified: Wed, 11 Oct 2023 19:05:26 GMT  
		Size: 1.1 MB (1079449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02c6d290bbb6e7e5fa704260ea8b1484fe7ecdd66edd12294d1c513daf3120`  
		Last Modified: Wed, 11 Oct 2023 19:05:29 GMT  
		Size: 58.8 MB (58820291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40aec89a88d49ea7c474a51f82ca7e29eab64787dae71ce90cdae573ac0c1258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231522006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4dff2e149d15b6837b1e6a02eeda0972a97e04f88101d5f210e617cd5c01c9c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:13:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:13:36 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:13:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:13:36 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:13:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:13:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:13:41 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:13:58 GMT
RUN boot
# Fri, 13 Oct 2023 10:13:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b071b04e08ba4bac56e57f3dbcc40de8bebfa48cf5f0e238999ce6cd365a0999`  
		Last Modified: Fri, 13 Oct 2023 10:30:11 GMT  
		Size: 1.1 MB (1066866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c29b0907c5dd8ab5423c96be7e41d3d83a9e2aa48f0d1918b81bbec1c81b932`  
		Last Modified: Fri, 13 Oct 2023 10:30:14 GMT  
		Size: 58.8 MB (58820456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
