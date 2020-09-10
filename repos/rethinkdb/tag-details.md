<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4.0`](#rethinkdb240)
-	[`rethinkdb:2.4.0-buster-slim`](#rethinkdb240-buster-slim)
-	[`rethinkdb:2.4.0-centos`](#rethinkdb240-centos)
-	[`rethinkdb:2.4.1`](#rethinkdb241)
-	[`rethinkdb:2.4.1-buster-slim`](#rethinkdb241-buster-slim)
-	[`rethinkdb:2.4.1-centos`](#rethinkdb241-centos)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:da7da457859eefd200cc5535e0d1a74aaeb6733031a54b4a174f761d20e8e312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:aa50702fb9e0aa61bac16d86258a5c6de9430b6ad04b308cf46c7689af8d6c1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3e553e3e4c4dfbf67c506a76d7d412f4afa726b4cb6bbf9723dd1df99ca23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:55 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Thu, 10 Sep 2020 19:12:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:12:04 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:12:04 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:12:04 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:12:04 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700b2e569c2b4d3e0f298572da29d13a33031d5e188feed19170464f0153d2b4`  
		Last Modified: Thu, 10 Sep 2020 19:12:35 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532f61770b19a72b3ffee8c0685ad264d515eb521f32fc00aaf1e9e6d0069bf3`  
		Last Modified: Thu, 10 Sep 2020 19:12:38 GMT  
		Size: 18.0 MB (17992138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9043b6a3643fcf38c611b44ef92870a440e7783cb3620bb2ac58af0bf8893a7`  
		Last Modified: Thu, 10 Sep 2020 19:12:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:da7da457859eefd200cc5535e0d1a74aaeb6733031a54b4a174f761d20e8e312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:aa50702fb9e0aa61bac16d86258a5c6de9430b6ad04b308cf46c7689af8d6c1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3e553e3e4c4dfbf67c506a76d7d412f4afa726b4cb6bbf9723dd1df99ca23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:55 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Thu, 10 Sep 2020 19:12:03 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:12:04 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:12:04 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:12:04 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:12:04 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700b2e569c2b4d3e0f298572da29d13a33031d5e188feed19170464f0153d2b4`  
		Last Modified: Thu, 10 Sep 2020 19:12:35 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532f61770b19a72b3ffee8c0685ad264d515eb521f32fc00aaf1e9e6d0069bf3`  
		Last Modified: Thu, 10 Sep 2020 19:12:38 GMT  
		Size: 18.0 MB (17992138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9043b6a3643fcf38c611b44ef92870a440e7783cb3620bb2ac58af0bf8893a7`  
		Last Modified: Thu, 10 Sep 2020 19:12:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:115347ac348bbd0c47964b9d4752eee50a939ef89800bfa8c913b57155c84bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b75b236e0d67b1d8c7f7d3800179cabd1ec330719a7d51c9155fce82fd4231eb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97239408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4c32f9f785547d2206f4d058e96229d571c31d6a714d32570dbf672ce015ed`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Mon, 10 Aug 2020 19:00:22 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Mon, 10 Aug 2020 19:00:23 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:36 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:36 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:37 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692940a286c0d3f1beadabb7a212a6e1678d9c0e303ac94a5bf35eb3734cadb2`  
		Last Modified: Fri, 14 Aug 2020 21:14:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ff4bec25e8a9c3995aa160e716057e6833426bc14c40925c0c9153efa3758`  
		Last Modified: Fri, 14 Aug 2020 21:14:29 GMT  
		Size: 22.4 MB (22370928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be9a2117906713867ccadcfe5b95b109d1b8f5788bb2fed8736ddcae099972b`  
		Last Modified: Fri, 14 Aug 2020 21:14:24 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:e6368957b48390016a8e429ac8ed1567ddb824df9cd482e743a1c445dcc2bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4be1aa0c1b69433b4bb3e7b6b1ae6ab1472a53992c04300f3faf2dc118563c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be342c08b0b7599764d49a408016c1e7d91e37818fcf3b1b6403ae909c98c2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:11:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:35 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 10 Sep 2020 19:11:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Thu, 10 Sep 2020 19:11:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:11:44 GMT
VOLUME [/data]
# Thu, 10 Sep 2020 19:11:44 GMT
WORKDIR /data
# Thu, 10 Sep 2020 19:11:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 10 Sep 2020 19:11:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a131c9a760cc01fd01b1bc0cbc1ee8a96a49f6c1101d7ba959c253df811546`  
		Last Modified: Thu, 10 Sep 2020 19:12:24 GMT  
		Size: 6.7 MB (6669146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a05642715b9d5d0da410c179378178fd8e8c785b0b0c17fbc57237404eed1`  
		Last Modified: Thu, 10 Sep 2020 19:12:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194b4fffc2ede18d90c83a173ac387cd7a1cbf7949e556494b8d2d1aa2c5cae`  
		Last Modified: Thu, 10 Sep 2020 19:12:26 GMT  
		Size: 18.0 MB (17990662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33d3c8a9da758fb504730266e4e13d31537fd8fe976d98f1f801842a1e8163`  
		Last Modified: Thu, 10 Sep 2020 19:12:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
