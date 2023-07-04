## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:5a30c79ced3d3b31b66503db6c71462db940154a42e8eec11e7f8bec0ae7d581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:535a1ff0ca0846f8706158048d2952b701a99f94f2c446e0ac520d495b89c5ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289864989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f233179e52adf1f02b9deb5dbdc2ad8b713387f2822ed9c2233e1d49619d301`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:03:33 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:03:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:03:35 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:03:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:03:35 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:03:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:03:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:03:59 GMT
RUN boot
# Tue, 04 Jul 2023 04:03:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3d40bd43d5fd5578d52b821d800d9245b2c75c4719bd86ef77c02cb13aa774`  
		Last Modified: Tue, 04 Jul 2023 04:13:44 GMT  
		Size: 198.5 MB (198549452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11757fd6308238a81bf9f9088a2abed885cf209da2e5e11dc06ba28280dbbc55`  
		Last Modified: Tue, 04 Jul 2023 04:13:30 GMT  
		Size: 1.1 MB (1077527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ef43953551c015e96c319d8537d06d635cc0448c71eb49c0b6fdf7096595db`  
		Last Modified: Tue, 04 Jul 2023 04:13:34 GMT  
		Size: 58.8 MB (58820622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3aff149d3316a892567650274609c31ddaf6720812dd93338a76af42da712b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285272405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb696eded0ae655d0e9273f8777643ecc6563252f0e17efd55b78dd4c439889`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:42:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:42:25 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 04:42:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 04:42:25 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:42:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 04:42:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 04:42:30 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 04:42:48 GMT
RUN boot
# Fri, 16 Jun 2023 04:42:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9957a538c0553b3c09b4c375828e78554437139b0fe6baa7bfccbd3ef8874cd4`  
		Last Modified: Fri, 16 Jun 2023 04:54:11 GMT  
		Size: 1.1 MB (1064852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d35d340fb752b33a5dc7e132e8810404d3a827ec64331102dc99c4a19a68db`  
		Last Modified: Fri, 16 Jun 2023 04:54:14 GMT  
		Size: 58.8 MB (58820531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
