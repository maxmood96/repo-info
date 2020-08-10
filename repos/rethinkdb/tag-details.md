<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4.0`](#rethinkdb240)
-	[`rethinkdb:2.4.0-buster-slim`](#rethinkdb240-buster-slim)
-	[`rethinkdb:2.4.0-centos`](#rethinkdb240-centos)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
