## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:ce8226dad8d4d87e24e80dacbf2eeda9cbf3f3b1d1ce958422e7da87fd1c2c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:92bc5add4cf3c67e9a13fdae239f155c5382f91832254f3b8a3d9dca0b29f624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236588834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de74cc4666b21da743b5fd4e065a3bab0c95b1ad85ac74c483ae21660ec5e3fc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:50:14 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:50:15 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:50:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:50:16 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:50:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:50:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:50:21 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:50:41 GMT
RUN boot
# Wed, 31 Jan 2024 23:50:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237cb6d9dedd71662d3dfef2792a61299af8d4b495bbb2a1e8f51c6f89c22ddd`  
		Last Modified: Thu, 01 Feb 2024 00:09:34 GMT  
		Size: 145.3 MB (145270936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a0fd4a1b29914c5528747a90854647fa44175561142158b4fe1e10d818e4e5`  
		Last Modified: Thu, 01 Feb 2024 00:09:23 GMT  
		Size: 1.1 MB (1079474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95edbefb260db8c5c5d1b253640d906e4ad30669eae43d777cf1da26794c887`  
		Last Modified: Thu, 01 Feb 2024 00:09:26 GMT  
		Size: 58.8 MB (58820597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

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
