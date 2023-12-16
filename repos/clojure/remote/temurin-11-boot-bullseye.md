## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:3155030213b7764f1caefe31f0a2b618803ec7149d66b9315768058cbb12ce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f277877c1b273b84c6d7526680171a6838fd7fafb254aeb6c99e1d927c728534
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0656e168efb1b2dea164dae81c3d0b3d2d188e45d2fd7970e9ded949639780f2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:25:48 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:25:49 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 15:25:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 15:25:49 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:25:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 15:25:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 15:25:56 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 15:26:13 GMT
RUN boot
# Sat, 16 Dec 2023 15:26:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9702745df0f994c9330f46f592ee18df8d4a2d46378b8cf5cd6e1abd161c0e0`  
		Last Modified: Sat, 16 Dec 2023 15:44:54 GMT  
		Size: 145.3 MB (145266339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dce9704efbddc74b679492a8c3374db7d67c3ca4adfbb1dc82d35a877391d2`  
		Last Modified: Sat, 16 Dec 2023 15:44:43 GMT  
		Size: 2.4 MB (2368695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1d1514458c18b039cf1901cc7974558b0000dcfd03c6f465d21e92b6213631`  
		Last Modified: Sat, 16 Dec 2023 15:44:46 GMT  
		Size: 58.8 MB (58820447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05c7643bff7067b96d06aec2a994cb0215373935e3a14de2e91aae05a878d04f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2d831da05f451415951af440d786f3760b0f84f952a7f98b4329a33a775cb8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 13:03:25 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Sat, 16 Dec 2023 13:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 13:03:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 13:03:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 13:03:29 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:03:34 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 13:03:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 13:03:35 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 13:03:50 GMT
RUN boot
# Sat, 16 Dec 2023 13:03:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af54c8e663dc85f64ce40fefa66d7c03c32ea39f2b5b91b849f62df8782494b`  
		Last Modified: Sat, 16 Dec 2023 13:16:08 GMT  
		Size: 142.0 MB (142001837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c909865373725638abcbc9e7aeca13f7ad07b1308aaeb0c3e21dae47dbdf6c`  
		Last Modified: Sat, 16 Dec 2023 13:15:59 GMT  
		Size: 2.4 MB (2357479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e1e89c840201441d33215bf22ddcd4ba92cda12a0e1e75e27b21277f14b3c6`  
		Last Modified: Sat, 16 Dec 2023 13:16:02 GMT  
		Size: 58.8 MB (58820407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
