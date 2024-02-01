## `clojure:temurin-8-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:a0694b8e635cd61f7986ee704b31f89ee6bc82ceed004355c01e30d7e2a3a69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9418bbbf6d2d52070a327b52a0e9a50e42638e259a0665a75ae66698a3434c57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195064601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6d63d0d06a2c54564fb6ccce1968b73da536ea29facda5d33b2b635241d47d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:43:27 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:43:28 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:43:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:43:28 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:43:34 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:43:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:43:53 GMT
RUN boot
# Wed, 31 Jan 2024 23:43:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8737523e74fd9c99538de2ca50cca6b04391d8a935a352206bd85358725e987e`  
		Last Modified: Thu, 01 Feb 2024 00:05:28 GMT  
		Size: 103.6 MB (103591879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad978e757b8fc014b3fb663951f8a06db1fcfaf09eac500edf328a52b267ab8a`  
		Last Modified: Thu, 01 Feb 2024 00:05:20 GMT  
		Size: 3.5 MB (3501719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d8f1524426374b2a62138f99169181a9635e667a690fd9b217ec5374d5f19b`  
		Last Modified: Thu, 01 Feb 2024 00:05:23 GMT  
		Size: 58.8 MB (58820538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a111dc3e3ac9d976dbd47b9103ba183729debb6b099fd8e9082224244d165f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194029290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6f697a48bdbf781c3f5fac77aec13d8f16bf2e409b6bf03b2b0cf4622c27db`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:20:06 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:20:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:20:09 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:20:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:20:09 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:20:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:20:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:20:14 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:20:32 GMT
RUN boot
# Thu, 01 Feb 2024 06:20:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ff00c3057caf77824dec5403166b179825f63e8162fb481183e1ae304bfe83`  
		Last Modified: Thu, 01 Feb 2024 06:39:20 GMT  
		Size: 102.7 MB (102703030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9728be8c86e09f7506020920762e21f0d9f728e8e8e4ffac93e24c8d67f16f27`  
		Last Modified: Thu, 01 Feb 2024 06:39:14 GMT  
		Size: 3.3 MB (3324952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28be9a69e4b170b86f42116563a70af8c9eab2bb674364758d63cb74e2fdb2`  
		Last Modified: Thu, 01 Feb 2024 06:39:16 GMT  
		Size: 58.8 MB (58820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
