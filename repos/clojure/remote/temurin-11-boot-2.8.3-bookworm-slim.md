## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:fd4fa74037e9f31ac67090dc48cec6df1045201e0e037d94147536fc29047a0b
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
$ docker pull clojure@sha256:f78ba850aa7eb5fdd3e744107ae0591ad5851b71e6b80b22a2757974dc5587b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233332880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f184fad1761a5b6451828e1d3fc3de50be98588797515519a2f31965a24fbf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:25:03 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:25:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:25:07 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:25:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:25:07 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:25:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:25:12 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:25:31 GMT
RUN boot
# Thu, 01 Feb 2024 06:25:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c45e79333257621ebdb964760990997f3a264d1e457e0bfb0ba6e5b5865a5b`  
		Last Modified: Thu, 01 Feb 2024 06:42:36 GMT  
		Size: 142.0 MB (142006518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ee1897f2ac5b04483a37f83641195c8fa8f8daec50ab6635fd3f42e01f5cbc`  
		Last Modified: Thu, 01 Feb 2024 06:42:27 GMT  
		Size: 3.3 MB (3324972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b23e6ea0efbd9fb6bfee45d22b84801d46d7af5bf2535cd231c8f39944e18`  
		Last Modified: Thu, 01 Feb 2024 06:42:30 GMT  
		Size: 58.8 MB (58820558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
