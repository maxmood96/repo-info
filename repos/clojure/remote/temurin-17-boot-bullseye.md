## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:f6b4d3fb6d281c3db494c1a04ad38f8740acbb28592123ce6c14cde29ae6db5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:84c4a962fec9b208792d6e207d49315991b48c101a5c87001136a55c5a17797d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308815726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcb5f35cace5787bbc2ba2b606fdc5a63e348294972d424abf83ad3098183af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:10:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:08:38 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:08:40 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Apr 2023 20:08:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Apr 2023 20:08:40 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:08:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Apr 2023 20:08:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Apr 2023 20:08:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Apr 2023 20:09:03 GMT
RUN boot
# Wed, 26 Apr 2023 20:09:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Apr 2023 20:09:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Apr 2023 20:09:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e363e191094639c858d95dc4482d74ded984d3d69a9dc0e9278ea1712a1c3b51`  
		Last Modified: Wed, 26 Apr 2023 20:24:02 GMT  
		Size: 192.6 MB (192580410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53de5e74f321f4bd28bece1c35b577d1d18fbff53e50cbc17e0fb33189d0b5d7`  
		Last Modified: Wed, 26 Apr 2023 20:23:49 GMT  
		Size: 2.4 MB (2361739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d633b3657664ef54bc6ebb18d265417ccfc025ae317cb20266af26ee709c95`  
		Last Modified: Wed, 26 Apr 2023 20:23:52 GMT  
		Size: 58.8 MB (58820442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c8a532960a09074c6f7d7bdcf762acedca73d4147092674251074c0df2f265`  
		Last Modified: Wed, 26 Apr 2023 20:23:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:961829c966f3772d8998541564a16cfa205e2020af55e543060d7bc51bc16e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306252448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3806c51cc54c9cc1c752882b06119b0baf146aa827a982bd6c5d21e0ccc50476`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:48:34 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:48:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:48:38 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:48:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:48:38 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:48:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:48:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:48:43 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:49:00 GMT
RUN boot
# Wed, 03 May 2023 17:49:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:49:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:49:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e3dfe953384be82597fea580dc9ef9ebb8b53e65fc436e07311295d7e9202`  
		Last Modified: Wed, 03 May 2023 17:56:22 GMT  
		Size: 191.4 MB (191387699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd4b1a528a6756262ae18bfebc7321d523a29039035a4fec5b98ee7e7cac436`  
		Last Modified: Wed, 03 May 2023 17:56:11 GMT  
		Size: 2.4 MB (2351082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaedb0f1cc218bde23edc38fa6de75c51f70bb89d07c5ff1e5052f5a6670725c`  
		Last Modified: Wed, 03 May 2023 17:56:14 GMT  
		Size: 58.8 MB (58820564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d9619a6ec17c14d3cb3801d792cf4b1820ddb3bd4b19af06c36f9a52c6646`  
		Last Modified: Wed, 03 May 2023 17:56:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
