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
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
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
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
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
$ docker pull rethinkdb@sha256:e23b27b6e1ce71a419ceca02262375fb7666ba92aef892b6b32c966fccfac8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:35c024e0728df6610190639369f166883546014785f4a3883882f9a4fafbcc5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51825615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e2bbfe41be04469b1d92938b4885a2566c57bbe2594fed8044a7aa13d19bf4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:31 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:14:31 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 31 Mar 2021 14:14:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:44 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:44 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee1f717c488f1e40530fda0a2c5dc30e54cd054c1775e2c8f10eb21521982bf`  
		Last Modified: Wed, 31 Mar 2021 14:15:59 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301c5ba7acd523143b15ea44f870dadf81ee71605668b848da8245bc9f539492`  
		Last Modified: Wed, 31 Mar 2021 14:16:03 GMT  
		Size: 18.0 MB (17993055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b9bf14917cbbc80cedc78f28de757b95b437d4b8472192387b3f227f64e540`  
		Last Modified: Wed, 31 Mar 2021 14:16:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:e23b27b6e1ce71a419ceca02262375fb7666ba92aef892b6b32c966fccfac8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:35c024e0728df6610190639369f166883546014785f4a3883882f9a4fafbcc5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51825615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e2bbfe41be04469b1d92938b4885a2566c57bbe2594fed8044a7aa13d19bf4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:31 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:14:31 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 31 Mar 2021 14:14:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:44 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:44 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee1f717c488f1e40530fda0a2c5dc30e54cd054c1775e2c8f10eb21521982bf`  
		Last Modified: Wed, 31 Mar 2021 14:15:59 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301c5ba7acd523143b15ea44f870dadf81ee71605668b848da8245bc9f539492`  
		Last Modified: Wed, 31 Mar 2021 14:16:03 GMT  
		Size: 18.0 MB (17993055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b9bf14917cbbc80cedc78f28de757b95b437d4b8472192387b3f227f64e540`  
		Last Modified: Wed, 31 Mar 2021 14:16:00 GMT  
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
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
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
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
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
$ docker pull rethinkdb@sha256:554a2b467b1556059726fe7d62f8a2cca008eb64eaeb5861673258a73c739cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cabf63fde4d643496ffab1f6dc9bb78959de474e113d66a18c8159242c9ae081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51824412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b59e506c70d6da67ef147de8cba7caae7733de31fb34ba009263283b5a615f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:13:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:13:57 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 31 Mar 2021 14:13:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 31 Mar 2021 14:14:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:14:10 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 14:14:11 GMT
WORKDIR /data
# Wed, 31 Mar 2021 14:14:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 31 Mar 2021 14:14:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc94af7e248ceaf9cfa7a657a33b16ce7979bd9a41b655555df481d6133831fb`  
		Last Modified: Wed, 31 Mar 2021 14:15:20 GMT  
		Size: 6.7 MB (6690526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018edd07404efe1724066a56ed15fb20d62b0cc467996bb1f93a3679707026f`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3a558623e1d1e95553d89e65789a9892814bf5dc445a7881fd6766574a5fe9`  
		Last Modified: Wed, 31 Mar 2021 14:15:23 GMT  
		Size: 18.0 MB (17991854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b168ccc9f4d495a7a373b327b8a261c6fb6b586219b65723bf2aed2349be`  
		Last Modified: Wed, 31 Mar 2021 14:15:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
