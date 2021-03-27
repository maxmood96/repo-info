<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2.4.0`](#rethinkdb240)
-	[`rethinkdb:2.4.0-buster-slim`](#rethinkdb240-buster-slim)
-	[`rethinkdb:2.4.0-centos`](#rethinkdb240-centos)
-	[`rethinkdb:2.4.1`](#rethinkdb241)
-	[`rethinkdb:2.4.1-buster-slim`](#rethinkdb241-buster-slim)
-	[`rethinkdb:2.4.1-centos`](#rethinkdb241-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:9f5357cff0fa42f273b710e9f0a07097aab2eea71a77546fbbb7d56606f731f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bd0b5ce550f8d1e614bb5f6941cff9c64592fd1f06edde46d377e2c5d0a5676c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51786917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0811d048d80b08578c1e0f1fcc3efd0bd91d58ea6f5c829a1f4ee6f78f60fbef`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:19 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:19 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Sat, 27 Mar 2021 09:10:26 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:27 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:27 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:27 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:27 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d7b1e9744b3d163a183cedd3be0163ac3f4bc93bad8223e9142080291ba44`  
		Last Modified: Sat, 27 Mar 2021 09:11:28 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0fdef6f22a57dc039de07bff022a7d00c9c223e16674c9d68b034d9158ed86`  
		Last Modified: Sat, 27 Mar 2021 09:11:31 GMT  
		Size: 18.0 MB (17992891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c7be3dda9f3a3dac3e0e6b9941b182f748a6ba6242cb87e56715fa9c36bbb`  
		Last Modified: Sat, 27 Mar 2021 09:11:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:9f5357cff0fa42f273b710e9f0a07097aab2eea71a77546fbbb7d56606f731f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bd0b5ce550f8d1e614bb5f6941cff9c64592fd1f06edde46d377e2c5d0a5676c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51786917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0811d048d80b08578c1e0f1fcc3efd0bd91d58ea6f5c829a1f4ee6f78f60fbef`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:19 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:19 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Sat, 27 Mar 2021 09:10:26 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:27 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:27 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:27 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:27 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d7b1e9744b3d163a183cedd3be0163ac3f4bc93bad8223e9142080291ba44`  
		Last Modified: Sat, 27 Mar 2021 09:11:28 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0fdef6f22a57dc039de07bff022a7d00c9c223e16674c9d68b034d9158ed86`  
		Last Modified: Sat, 27 Mar 2021 09:11:31 GMT  
		Size: 18.0 MB (17992891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c7be3dda9f3a3dac3e0e6b9941b182f748a6ba6242cb87e56715fa9c36bbb`  
		Last Modified: Sat, 27 Mar 2021 09:11:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:11d9649e49b7e3b68d5d28e3e3959b055a6f7639bab3bc810e8afe96c6e7cc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:17689662917e7af14d2bebf46cd6890ee8badf9b74e8e8b1480ec0b6bde5a29a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97512200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f93c64f13e16520ee2f13c350b04b364d79f12de5f07eb0ab11357643807bf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Fri, 12 Mar 2021 22:06:51 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:59 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:59 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:07:00 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:07:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:07:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25076e20c46678ae755ba6afa36d6d81841dc318bbf67e12e1dc65a61830d747`  
		Last Modified: Fri, 12 Mar 2021 22:08:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a6c1b31a4042d1cd7786c6f48d8c3d4f0c4694af26eef0a12a818bfb31e040`  
		Last Modified: Fri, 12 Mar 2021 22:08:32 GMT  
		Size: 22.3 MB (22329806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b305cc56442aaa917ad4c80c57d1d01db071a009e92c3a8f5129445a25b4eb`  
		Last Modified: Fri, 12 Mar 2021 22:08:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
