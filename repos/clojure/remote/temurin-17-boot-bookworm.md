## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:073f2041ec7fa0abdcb48eeb80e5d573a93f2e33d61687577f405e32ef7674b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e82bcebf158e72a03fcae6516b736297a31c0f68bb963b80aad0a77b281cd9ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258783442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b49baf3dcce34c7b73ec10bbe883c329ec42e8fc2d58f7c9c42081d5a56e16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:07 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:04:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:04:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:04:09 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:04:15 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:04:15 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:04:33 GMT
RUN boot
# Tue, 19 Dec 2023 07:04:33 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:04:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:04:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f624b107a059794584ade4c93fa06b271cee1c08c552c6218c7f9f9b45f4706`  
		Last Modified: Tue, 19 Dec 2023 07:21:37 GMT  
		Size: 144.9 MB (144873942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ecafb9a068edf872448b77edffe933513faf17ccc2d552495138a6356c937`  
		Last Modified: Tue, 19 Dec 2023 07:21:26 GMT  
		Size: 5.5 MB (5527047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fdbffb45fd04e1bfa1a2bcc6f7c12f64ac1f991541760e0ca8d94052b26b46`  
		Last Modified: Tue, 19 Dec 2023 07:21:28 GMT  
		Size: 58.8 MB (58820473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c690f49fa8c3175c09b9a54de8e1c9d61cf1371d9eed4fbd93d7a1c011a76c`  
		Last Modified: Tue, 19 Dec 2023 07:21:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3ab0a72563be74cd86ad1b70d39f8760b5c72456bd95a070dc4a2eb31051284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257443944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2fdd4f4deea2a290f5e2f0cb957d4cc393d0d7af1fc3f260e97968cfa272d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:03:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:03:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:03:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:03:39 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:03:45 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:03:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:04:00 GMT
RUN boot
# Tue, 19 Dec 2023 07:04:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:04:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:04:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c921ebaa0e3aa9234b54378bc303467ff63a194e02c492c4836def5239e7f3`  
		Last Modified: Tue, 19 Dec 2023 07:18:48 GMT  
		Size: 143.7 MB (143681701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9962100de87eb14ef7d23fdf549d3ccab8cba3bfb115ef84a168c84a74f96b`  
		Last Modified: Tue, 19 Dec 2023 07:18:39 GMT  
		Size: 5.3 MB (5349306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05677dbe403a6241d072327d491e1c703e109e4b080630655f98d1ea6a07f5c8`  
		Last Modified: Tue, 19 Dec 2023 07:18:41 GMT  
		Size: 58.8 MB (58820278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddf1407d793a8556f027f0c12e1ba8e09dc9c5558d333c3d2e9eda0e41bb8c4`  
		Last Modified: Tue, 19 Dec 2023 07:18:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
