## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:1437c294d57d5f16704dd00ca2174f26a6c2595ebea5866628f61a46ef33ac28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0a5ace97f73b34fcd5e3c8f34e4fa0824b3a40ff28614dd84c8d5df9bf325853
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145930176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318a3d3464af595620c2e5f2ce32ff7bf61526101881144573af7f6263ac37ff`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:06:08 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:06:09 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:06:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:06:09 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:06:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:06:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:06:15 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:06:32 GMT
RUN boot
# Sat, 04 Feb 2023 14:06:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2e51264c882c87c91946d030677c2c91c91959e652ff8ca78e35a61148bb39`  
		Last Modified: Sat, 04 Feb 2023 14:20:17 GMT  
		Size: 54.6 MB (54635589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966c067a30284dd788e8e808a4fa7c646e6044b0de6df884ed6180fa204f735b`  
		Last Modified: Sat, 04 Feb 2023 14:20:10 GMT  
		Size: 1.1 MB (1077364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6260cb86b965d87680bec50fcfea6906c23783231e0b09fa3f322c09b574d29`  
		Last Modified: Sat, 04 Feb 2023 14:20:13 GMT  
		Size: 58.8 MB (58820304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be2dcce8bd9a1f31a0cfec0c4ba330b5da09a506ab5d2e2b3935f1bd6a410cb5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143657860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29828d70d8e14a0a4db4b0fdacbe75371a918d750a79f1320a45285c542e0986`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:03:14 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:03:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:03:15 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:03:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:03:15 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:03:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:03:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:03:20 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:03:38 GMT
RUN boot
# Sat, 04 Feb 2023 17:03:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728eccb26a7c7b50bd803fa4105ba630442ce5bc87412fd21de9d8e74052ed1e`  
		Last Modified: Sat, 04 Feb 2023 17:15:30 GMT  
		Size: 53.7 MB (53727893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831a0f615743cac1a924431553c2ce7d33d4d1b53779a930177d5dc9bc8821c8`  
		Last Modified: Sat, 04 Feb 2023 17:15:25 GMT  
		Size: 1.1 MB (1064668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6ab9c5c6994358705dc256a6b65e3ac9e4a747949288f03ce9f34136b58cae`  
		Last Modified: Sat, 04 Feb 2023 17:15:27 GMT  
		Size: 58.8 MB (58820507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
