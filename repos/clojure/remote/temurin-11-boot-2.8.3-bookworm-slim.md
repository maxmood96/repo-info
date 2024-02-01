## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:7c766978ad1a0e2a2fd6fda052a4117c582cff0fbabc6c3e53cb21a334d4130b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f0a54aa0074cd3c346ed2e119b63656eb6305343b60bb6aba18154d97cc8be6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236743672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6641ec47218b849a2143ed8f042f8cd4270e23f62e04068c5125153ceef2b8a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:49:05 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:49:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:49:06 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:49:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:49:06 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:49:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:49:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:49:12 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:49:32 GMT
RUN boot
# Wed, 31 Jan 2024 23:49:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5064ff6b6cb70868d3b2861016a4e99a9515996a6839bad68a869ad30eb6f8ff`  
		Last Modified: Thu, 01 Feb 2024 00:08:51 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f2e75b4d7572cef8131897dd5891f042be314491f1f4cffe2b0c7f37af9f82`  
		Last Modified: Thu, 01 Feb 2024 00:08:41 GMT  
		Size: 3.5 MB (3501729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1e8e4f020e13704e100bb3c38c3cdcd2187e2566b6310f4e6afd6e627095f1`  
		Last Modified: Thu, 01 Feb 2024 00:08:43 GMT  
		Size: 58.8 MB (58820537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:277fdd150f66ffc3ee1eb90b29d7adbc703c2b4d850603af5061e6925029e5b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233306107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc3ccdc18507086f38cf4980f6945a67f4bc53baa0859fc3a9d8f2aa0f1bc4d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:14:50 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:14:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:14:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:14:54 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:14:59 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:14:59 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:15:15 GMT
RUN boot
# Wed, 24 Jan 2024 22:15:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8cf01ad17b220dbadf311b0a8fa97aff8f5780e283142d70fed56b9231c268`  
		Last Modified: Wed, 24 Jan 2024 22:36:58 GMT  
		Size: 142.0 MB (142006467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f34398d63a833a0ebb813242179520bed2b641885f0adcb8d52d38b82b74a14`  
		Last Modified: Wed, 24 Jan 2024 22:36:49 GMT  
		Size: 3.3 MB (3321996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb412028f51c11803f6d5ad9db5cd3dc53cb22f7eb60676083854feba019461`  
		Last Modified: Wed, 24 Jan 2024 22:36:52 GMT  
		Size: 58.8 MB (58820309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
