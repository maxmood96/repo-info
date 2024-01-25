## `clojure:temurin-8-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:d6efc1e66f7685cd16b83134fc54441127b44e6583ab148c76d9c455aab2c3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fd958c1afe6e4079dc3e6be82cc18c2ef4a11c39b3cea65353abbf33ad0736a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195036240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc930a0660e032590c69416c63de918cc46b6c6cf83fef31459fd0feff44d5`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:00:23 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:00:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:00:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:00:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:00:24 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:00:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:00:32 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:00:50 GMT
RUN boot
# Wed, 24 Jan 2024 22:00:50 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab585263d7579e6a278c92f7eb0200b4b642ae084fe62d265f67f06f6b45ba`  
		Last Modified: Wed, 24 Jan 2024 22:32:04 GMT  
		Size: 103.6 MB (103591881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9725843436e877f5d81a73389a941463d7926db4c0db6cbef40cdda8ba68ae`  
		Last Modified: Wed, 24 Jan 2024 22:31:56 GMT  
		Size: 3.5 MB (3498087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6897c04c937bd1479a2c3963aa679bc2a1d28ef9a713b34c70aa5d0a9899f8e`  
		Last Modified: Wed, 24 Jan 2024 22:31:59 GMT  
		Size: 58.8 MB (58820351 bytes)  
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
