## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:5c958f6109bf6c108024c89477de3a5d800b663d064951d69218ae76e2731af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b203e049b44705ab99fd9b5b0fa0c2aaab1d116398fb0101e9307f8e0d2b2607
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236588897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74a84b1d6ed30333d60aa745c4834ea0db77d7ce7a2f9d4e96afac40256c60`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:11:43 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:11:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:11:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:11:44 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:11:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:11:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:11:51 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:12:10 GMT
RUN boot
# Fri, 02 Feb 2024 17:12:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51c4479436104d74ffa4a3d93686573e899aa1d342f5c43e963b26942d6975`  
		Last Modified: Fri, 02 Feb 2024 17:32:04 GMT  
		Size: 145.3 MB (145271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02961fe261630e46f1db8b062a8f0b4a48dfb890a03dafb9ab629ff69d6631`  
		Last Modified: Fri, 02 Feb 2024 17:31:53 GMT  
		Size: 1.1 MB (1079482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188a8c10c3e5ee709b29ddc3ebcc212ac2d7c63fb62bfad3e55f3be15d9192f1`  
		Last Modified: Fri, 02 Feb 2024 17:31:56 GMT  
		Size: 58.8 MB (58820568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e48949356ebbd9abca099aea48ab4da34dce15fb8878d5bb243f65f1f9b5c3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231958108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f3baabccaa6380387b498f1749cbb859ae76d36b48f9276fc26029b13b5adb`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:21:24 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:21:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:21:28 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:21:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:21:28 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:21:33 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:21:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:21:33 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:21:51 GMT
RUN boot
# Fri, 02 Feb 2024 08:21:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971292bc5a4cf5c576af3b6872d17499b5584c7af4217c5cd7375f2d989371b1`  
		Last Modified: Fri, 02 Feb 2024 08:39:02 GMT  
		Size: 142.0 MB (142006417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137f80018a6a065145e154b0589ecdc5248f8669774da948d108deb399710bfe`  
		Last Modified: Fri, 02 Feb 2024 08:38:54 GMT  
		Size: 1.1 MB (1066871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe3357dd9ddfac2c76f5bfde574a9d5a47f12991760a3dd3454d7d24a2cea6`  
		Last Modified: Fri, 02 Feb 2024 08:38:56 GMT  
		Size: 58.8 MB (58820486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
