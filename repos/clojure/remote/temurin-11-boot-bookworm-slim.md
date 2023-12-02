## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:68f42114a367afae003ecabaa6469b7d48fb016493059cdf78fa92144b167aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f989bfd8f3f6988888816cae97ff44a4f76a7ac9b988872fff1f8bfcac7929ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236738505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51832ea4d87bc511be98151819d5e8a08b7dcccb160b2c686cd1320c777f104b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:54:40 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:54:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:54:41 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 09:54:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 09:54:41 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 09:54:48 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 09:54:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 09:54:48 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 09:55:05 GMT
RUN boot
# Sat, 02 Dec 2023 09:55:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4050ac330d97fd84a1d6329cccff3c6d67aeace4dadb496e6d7467c8568e3c1`  
		Last Modified: Sat, 02 Dec 2023 10:14:01 GMT  
		Size: 145.3 MB (145266397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58891b125cf3438ef47d280d8705b57a18996587c28a72baa9a65ed3ad3ee1aa`  
		Last Modified: Sat, 02 Dec 2023 10:13:50 GMT  
		Size: 3.5 MB (3501704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c095306fe417b0eea359e25dafeb98c7df4d40d0a747a6ef72963cf3fdd152d`  
		Last Modified: Sat, 02 Dec 2023 10:13:55 GMT  
		Size: 58.8 MB (58820496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae2908e7d4ff2f7df716b03c6d80e45003143722ad2b4d69273d6638e191a8b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233326339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfcbe153dee04984f743ee1f90a70e244d854dbb8c03e89ed6b75afa8504af5`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:45:02 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:45:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:45:05 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:45:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:45:06 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:45:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:45:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:45:11 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:45:27 GMT
RUN boot
# Sat, 02 Dec 2023 08:45:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499cde67ef4ddbbb49efba4d14e85c99ac1dcc40592a7b8c7cac48b4f81d299b`  
		Last Modified: Sat, 02 Dec 2023 09:03:55 GMT  
		Size: 142.0 MB (142001789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76579d9a69f44eb89e0089c86c56f1b42eda3ba2eb3015cc689fd2dfa3fb8922`  
		Last Modified: Sat, 02 Dec 2023 09:03:46 GMT  
		Size: 3.3 MB (3324864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3b5418849a58c6c0c3cd947727ff11f3634baebfe9f1158d5965bd440ff09`  
		Last Modified: Sat, 02 Dec 2023 09:03:49 GMT  
		Size: 58.8 MB (58820409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
