## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:b6d336066ff142893d42ccf3aa9900a17c36be00e75ca24870ee647176063e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ea6d1e9cd9332504aefea2377ea26eb242c867090b7da8b4f78bdc86590867a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236141745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f99d65846954ddf076fc0cae98be703e4fcfc3cc5f1f205131f0b7037163dc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 02:47:42 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Sat, 02 Sep 2023 04:05:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 04:05:14 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 04:05:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 04:05:14 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 04:05:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 04:05:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 04:05:20 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 04:05:41 GMT
RUN boot
# Sat, 02 Sep 2023 04:05:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f79c552b7bf3e1325e1edb4c27a281803086b37e0755ff605dd144125dad98`  
		Last Modified: Sat, 02 Sep 2023 02:51:09 GMT  
		Size: 144.8 MB (144825994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31192f01700c4f252b35248914a7e5fcb08dcf33f32a8834e6c85f354cd4a358`  
		Last Modified: Sat, 02 Sep 2023 04:15:42 GMT  
		Size: 1.1 MB (1077572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50aedad87266c3527efb286c28c933d30213920a76578ac8be40a666fe6decf`  
		Last Modified: Sat, 02 Sep 2023 04:15:45 GMT  
		Size: 58.8 MB (58820501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:119dc9699549818833ab18f4b2b6bde9b83470a7ae06823b8bf645254499648b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231518558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a517ea0b09f7eb1394516016085dd4d5088fb3f324c92e7bda0e68c66132b7e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:44:25 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:44:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:44:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:44:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:44:29 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:44:34 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:44:34 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:44:53 GMT
RUN boot
# Sat, 02 Sep 2023 01:44:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b924b77d195ee682d4adf6c744cba3a607633e56b93e8e8d9161e1a29b17fc4c`  
		Last Modified: Sat, 02 Sep 2023 01:53:29 GMT  
		Size: 141.6 MB (141570383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52456ab1a7b8f3e40dc2f5930b0b715cac5442cf29aa839c059cc1d68272d66b`  
		Last Modified: Sat, 02 Sep 2023 01:53:21 GMT  
		Size: 1.1 MB (1064876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e52705d096e8881848a5becc6b8ff6fd77725844aa6f96e0ec4f39fbf70d6d`  
		Last Modified: Sat, 02 Sep 2023 01:53:23 GMT  
		Size: 58.8 MB (58820483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
