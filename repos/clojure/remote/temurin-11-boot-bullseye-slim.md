## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:55444d7768e5453f603c4a09f53f641735e6067b2ab3c030db36b4794ecfeb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:abc59cd031f999403ec99031764ffd02236f84bf3d286555cb40161fdedf46a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236583946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a39857dfcbf2c84c8eba3e99aed0c68be65fa2b74ea6a8729b61ed6507ab2c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 07:39:06 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:55:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:55:47 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 09:55:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 09:55:47 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 09:55:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 09:55:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 09:55:53 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 09:56:10 GMT
RUN boot
# Sat, 02 Dec 2023 09:56:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e28bbb7ed8d446eab9126cf70b8a8696a1b2c97ace981f72b9e7fa4a8fa7e1`  
		Last Modified: Sat, 02 Dec 2023 07:43:21 GMT  
		Size: 145.3 MB (145266435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f672f9d89b841d3741b1201db74b2560d6815ebaaaa5038a35c41724be7d776c`  
		Last Modified: Sat, 02 Dec 2023 10:14:30 GMT  
		Size: 1.1 MB (1079490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1bfddcde4d86b6817d85a520a439e79312095db5d48a63121e43070205a902`  
		Last Modified: Sat, 02 Dec 2023 10:14:33 GMT  
		Size: 58.8 MB (58820197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe556f4a15b073da0aaae5b899ece596e4a1ab8e3f39f950e6069a7d669aa2cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231953220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fa90abbb3c5ba6db644fe150ac1e3f90786cdd2e8a7192d401ac2e8b02935a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:45:58 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:46:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:46:01 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:46:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:46:01 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:46:06 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:46:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:46:06 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:46:22 GMT
RUN boot
# Sat, 02 Dec 2023 08:46:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c9736680f80d26b6300f944e7ba80ac7f1a756c950bdf599346e7954ad2dff`  
		Last Modified: Sat, 02 Dec 2023 09:04:30 GMT  
		Size: 142.0 MB (142001789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d5f110e93a6f10db102eda1adb0ab90d546679d7e69f9da8a55c5f00d0d34`  
		Last Modified: Sat, 02 Dec 2023 09:04:21 GMT  
		Size: 1.1 MB (1066849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cc069257a0e9daa681cdd766f6ece115dff488fd689f090562d8e0a91b15bc`  
		Last Modified: Sat, 02 Dec 2023 09:04:24 GMT  
		Size: 58.8 MB (58820459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
