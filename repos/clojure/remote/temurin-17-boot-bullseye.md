## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:8876de3b279022c5e614223358a7ba5e46a8f210ddc38c18e3ed9d3bf871e718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4f0e4fdf9b902ebb101670763fa9248645baf028871444be37ede142f80065a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261166369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acab1f83f9f8850bd0129d62062aed8940079207cbf147d7a919a4cfef09988`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:23:40 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:23:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:23:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:23:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:23:42 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:23:47 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:23:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:23:48 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:24:05 GMT
RUN boot
# Tue, 12 Mar 2024 06:24:05 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:24:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:24:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0a6dff1d086a6e22a033f3e8e82ecebda2cf307ef106d9c945377612642e65`  
		Last Modified: Tue, 12 Mar 2024 06:41:11 GMT  
		Size: 144.9 MB (144893135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749c08c7440727ae62c3b2d0dbec9a1a6b7cf00c8dc664dd3e603f2fc1c7ecda`  
		Last Modified: Tue, 12 Mar 2024 06:40:59 GMT  
		Size: 2.4 MB (2367238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a838ac9124cfcb3e1ae1437f5fe73672b6777b0f2c9d5ad7a1e45c87e6d9a4c`  
		Last Modified: Tue, 12 Mar 2024 06:41:03 GMT  
		Size: 58.8 MB (58820627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af95e85e50425e1e1bb938f018f166897e2eb51eae5b56dc778bfb29a07c42ea`  
		Last Modified: Tue, 12 Mar 2024 06:40:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0fff1c2d017c6ec6ce353013b7b2e4cb907ed1df57d34268e4cecd10b41d9f07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258619611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7571c8421ca196be5051c64f8090a64e1e360016097993435be49fc1393de419`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:39:59 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:40:02 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:40:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:40:03 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:40:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:40:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:40:08 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:40:23 GMT
RUN boot
# Thu, 28 Mar 2024 02:40:23 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:40:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:40:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fcbeb5850480786ffe08e1502f043ad8bc5d2f3b44ca90dbf17efaa841dacb`  
		Last Modified: Thu, 28 Mar 2024 02:54:18 GMT  
		Size: 143.7 MB (143720923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454020489f7256bfc6faa582ba534813aa003dcec54ebbf721aa481078e4ff75`  
		Last Modified: Thu, 28 Mar 2024 02:54:09 GMT  
		Size: 2.4 MB (2355854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710a9b3d1aec8738d650ca2c8860514eca0b87e99b06224fa9c2379d2a526e73`  
		Last Modified: Thu, 28 Mar 2024 02:54:12 GMT  
		Size: 58.8 MB (58820334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29f7079631e1f5ab74e2eadfc0185cea41ebe3eb59709f27f0502465d05016e`  
		Last Modified: Thu, 28 Mar 2024 02:54:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
