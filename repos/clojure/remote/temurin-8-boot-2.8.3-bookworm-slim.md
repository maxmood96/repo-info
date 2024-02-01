## `clojure:temurin-8-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:d7fad1bdf7623961417524c6abb7b60da013939a19ed75504a03733fc65aa8ff
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
$ docker pull clojure@sha256:d69d68cd009ecf2f39a2e504f0634d93ed26b523fb228b6ab77dec9f6e3d6e90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194002591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cbd0851e063ef7da6eb359bb19d8a3fe641e8767d0f0017543ca23e1aa4f0a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:07:13 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:07:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:07:15 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:07:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:07:16 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:07:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:07:21 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:07:37 GMT
RUN boot
# Wed, 24 Jan 2024 22:07:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903d057319578dd32f89414278e5f97bb9f54627f15d1a723142e79a5d4eb6b`  
		Last Modified: Wed, 24 Jan 2024 22:32:24 GMT  
		Size: 102.7 MB (102703041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde83660e27257c02e42f4484a2c5f69a9b8ad325f3ec325af09b3d36bb3f654`  
		Last Modified: Wed, 24 Jan 2024 22:32:18 GMT  
		Size: 3.3 MB (3322022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82395daad204ea5926f350d42102a01843516d719ce2ef5d535d272a5131b57a`  
		Last Modified: Wed, 24 Jan 2024 22:32:21 GMT  
		Size: 58.8 MB (58820193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
