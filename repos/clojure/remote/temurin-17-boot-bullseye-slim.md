## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:7141889b8947dd5e731f571e89f394f0cea56af80b9451b8c515d168bc7dc9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f06f817f8c468dac43b9487338a9e2fadbf1af8b4666193e46d4d907214afb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236091974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b57f9ecff966a1d174a539757cdbc968912793bf7cac0d3e1775a6a64ddfe5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 02:46:18 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Sat, 02 Sep 2023 04:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 04:09:19 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 04:09:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 04:09:19 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 04:09:24 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 04:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 04:09:24 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 04:09:43 GMT
RUN boot
# Sat, 02 Sep 2023 04:09:43 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 04:09:43 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 04:09:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d4946b1998501e173a27b5106ab354beefe3a0cead8354e4f41fc3bc266f22`  
		Last Modified: Sat, 02 Sep 2023 02:48:51 GMT  
		Size: 144.8 MB (144775778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfb4b511d15ecad434a2425f02a7d3ef7d294289c39e0dc464042a286df5c01`  
		Last Modified: Sat, 02 Sep 2023 04:18:03 GMT  
		Size: 1.1 MB (1077535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adf3b0c212b123fa9cbd437625254d2b902f836756196be1f5f6ceafd8bc9d4`  
		Last Modified: Sat, 02 Sep 2023 04:18:06 GMT  
		Size: 58.8 MB (58820582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c73cb0bd3be8cde4b0a4a7410e52568b4aca1eded1ae30ab2a0c0c766d9c1a`  
		Last Modified: Sat, 02 Sep 2023 04:18:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14e0d778dbcf89f0cbded29a619e74e9e948accaa74993665ddefb07636b9655
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233492105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac48bbbc0017a9ebee9cd2108eed9bd0d5e514bf3411db264d8f0a1ff1b07f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:48:00 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:48:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:48:04 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:48:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:48:04 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:48:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:48:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:48:09 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:48:25 GMT
RUN boot
# Sat, 02 Sep 2023 01:48:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 01:48:26 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 01:48:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75390d7bc4a96162e240272aeff28881955f7af498179aa85faecd879748f913`  
		Last Modified: Sat, 02 Sep 2023 01:55:46 GMT  
		Size: 143.5 MB (143543515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6609d00c40d78b8dfbbef7aecbccb296e31409a782e41d7c2eb33229765bdf6`  
		Last Modified: Sat, 02 Sep 2023 01:55:37 GMT  
		Size: 1.1 MB (1064830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c463f0425e6740b6d9abdb541b3a8129352472b86b9506031c099ef10da4c69`  
		Last Modified: Sat, 02 Sep 2023 01:55:39 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fe3c7d5e4d5ae1b7c61d7bd7c47f88113b7f6ae2d6f9540d47f8b1a29b5e17`  
		Last Modified: Sat, 02 Sep 2023 01:55:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
