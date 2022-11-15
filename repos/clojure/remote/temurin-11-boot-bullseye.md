## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:956f72a518c41e8b3f9e3ae2d83da4b516ccaf9d96688684305df5090ba1aa3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e0220a8d445f94380d348a0929b3a96962c6183db4d12a9b2c81b71d7dcace1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314684879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c88a2a5537ae704deafa781c9d3518561ea3da183965e08f659411cffc6087`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:11:42 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:11:44 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:11:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:11:45 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:11:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:11:50 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:12:10 GMT
RUN boot
# Sat, 05 Nov 2022 01:12:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888ca723db20161bd481e5a8af9ae7b9145b403d0fa3f2f444e7c6a21909570c`  
		Last Modified: Sat, 05 Nov 2022 01:25:58 GMT  
		Size: 198.5 MB (198455847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89052280c96745e6b7276e9d6a92bb668427b1e1ad4c6d6e9094f53de42ed1e3`  
		Last Modified: Sat, 05 Nov 2022 01:25:44 GMT  
		Size: 2.4 MB (2362167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982c49d36bfea95914abcbaccd25cb397ccca89bbd8ad3b238952c8e6cc1e9`  
		Last Modified: Sat, 05 Nov 2022 01:25:48 GMT  
		Size: 58.8 MB (58820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9774748a79fcee05b051f49a9582010bac979beaa21b5a61204be2342cc6e790
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310073610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce19581599e1788d11e9b004db37c17642a9d723a8170e492c08f8a76ee5b649`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:26 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:51:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:51:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:51:31 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:51:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:51:36 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:51:53 GMT
RUN boot
# Tue, 15 Nov 2022 05:51:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6410c82310e7ed376d2f9bdb09d5bba8c5586def41b40a45fc26ed1c405a8a0`  
		Last Modified: Tue, 15 Nov 2022 06:03:10 GMT  
		Size: 195.2 MB (195201165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bccdd89e8887895edda6c63975314da5e866d4fd2b6e5b584d4cd825750876`  
		Last Modified: Tue, 15 Nov 2022 06:02:59 GMT  
		Size: 2.4 MB (2352268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd21132d1d7fcdb2ba6ea807bc54421c634950afd8075505681b5bec14d41b5`  
		Last Modified: Tue, 15 Nov 2022 06:03:01 GMT  
		Size: 58.8 MB (58820315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
