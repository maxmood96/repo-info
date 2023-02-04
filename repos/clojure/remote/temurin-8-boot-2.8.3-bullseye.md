## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:97d86dfd451f6df3a16d9e150b9ef2dd4cb135088c14f738809a36ebb7495cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b42ff8272495efa6d060c5005109a4a3b123e65f49ef3a05d82eaea4691aed95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170842270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bf758eb8981b25d13d43f88b3a17475e9e1bc96e6ef0f32cbe89c9d226fd96`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:05:28 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:05:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:05:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:05:29 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:05:35 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:05:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:05:35 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:06:03 GMT
RUN boot
# Sat, 04 Feb 2023 14:06:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed6af97ccf16f95286359a7baad8fc2394e5c5fdeb6b0e3d4faa3a9509aa270`  
		Last Modified: Sat, 04 Feb 2023 14:20:01 GMT  
		Size: 54.6 MB (54635589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5356942665d9527802bac3fb85d706fc46268d209808b068c39a8b0066ef9`  
		Last Modified: Sat, 04 Feb 2023 14:19:55 GMT  
		Size: 2.4 MB (2360701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0589837ebbe5faab215cbcfcaaa7ff2340ac36cc31cb6c960af126af861a32b`  
		Last Modified: Sat, 04 Feb 2023 14:19:58 GMT  
		Size: 58.8 MB (58820668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62110ce6067859132c750adfece7050fe3314911fe788dbbaa1cd6d91090dccf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168581494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522103e6d6f0aac33d46777cfdcff8249fdc457d712f0253b0db605812de1289`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:02:16 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:02:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:02:18 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:02:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:02:18 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:02:23 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:02:24 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:03:04 GMT
RUN boot
# Sat, 04 Feb 2023 17:03:04 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1981d852fd5152d416c9ad7e8c497a15ca9447400a625831b166262fdf77c59d`  
		Last Modified: Sat, 04 Feb 2023 17:15:16 GMT  
		Size: 53.7 MB (53727941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4a2ab3d7bdaebe05eb82aaf1aa584a5fb175bcbcb7e91994c5343b7eb74aa`  
		Last Modified: Sat, 04 Feb 2023 17:15:11 GMT  
		Size: 2.4 MB (2350665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d7ca0d4737840ca1bb37ed34255fd3ce52e84b5cbe29978eee686eb6d9c51`  
		Last Modified: Sat, 04 Feb 2023 17:15:14 GMT  
		Size: 58.8 MB (58820961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
