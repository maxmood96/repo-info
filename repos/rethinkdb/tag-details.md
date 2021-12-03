<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2.4.1`](#rethinkdb241)
-	[`rethinkdb:2.4.1-buster-slim`](#rethinkdb241-buster-slim)
-	[`rethinkdb:2.4.1-centos`](#rethinkdb241-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:d791d3a973a0f596441d5d9ebc394ecd2783e78591c84d90a5f35f01a735958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5d107c365fb6bb88856cf8576f1ea02358832149f0414c23c2301b55d46e49a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126fdd90251808ba019b7b1969217564fd2bc38055584c034c3bfed4b412d6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 03:45:59 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 03 Dec 2021 03:46:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 03 Dec 2021 03:46:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 03:46:18 GMT
VOLUME [/data]
# Fri, 03 Dec 2021 03:46:18 GMT
WORKDIR /data
# Fri, 03 Dec 2021 03:46:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 03 Dec 2021 03:46:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14358a6fa48651796b12a46712690dfc747d989660d0c101e7d92d1d78134903`  
		Last Modified: Fri, 03 Dec 2021 03:46:44 GMT  
		Size: 6.7 MB (6691041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53565ca8ebd24d12231eea3a22dfdb2e9b62608057634947ae2aa22576f1a420`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0eb01bb1d629344bc229d2ed2eee029e4514ba97ab41305abe7784051ff21`  
		Last Modified: Fri, 03 Dec 2021 03:46:46 GMT  
		Size: 18.0 MB (17991491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545a92af626178003556b438b33c5a77d04345eac8b13774fb9ce70c5f62fb1`  
		Last Modified: Fri, 03 Dec 2021 03:46:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
