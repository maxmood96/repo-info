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
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
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
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
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
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
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
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
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
$ docker pull rethinkdb@sha256:31061dd0c395d6e88701050e89b7e3d9eee191dc186990f613d8a71bff250838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3c265b32d178d42194771f9c49d3feda08d3a4d6116814faca328f8c13f0fef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51858189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8a9f603aa5542a0df85d42ee47d3ee849410ad70edb58c78dc6cc3ae6874d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:10:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:35 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 29 Mar 2022 19:10:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Tue, 29 Mar 2022 19:10:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:10:42 GMT
VOLUME [/data]
# Tue, 29 Mar 2022 19:10:42 GMT
WORKDIR /data
# Tue, 29 Mar 2022 19:10:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 29 Mar 2022 19:10:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf52dfe6d4d0218d7c974ac17298120ebf4ed047912b22f1af4bf8443f3ad40`  
		Last Modified: Tue, 29 Mar 2022 19:11:04 GMT  
		Size: 6.7 MB (6698378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd16857942488df1db7bca8587a75749b1be8af01a82a22a358283ed46018e`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8efbffddaf4b2ad5379ec42009adef150c2c0b10340c916a5779388646d78`  
		Last Modified: Tue, 29 Mar 2022 19:11:06 GMT  
		Size: 18.0 MB (18005104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec8294e9f970dce2184866b7b5d7a599cde1240ce12acbde6c881dbd9ee8aa`  
		Last Modified: Tue, 29 Mar 2022 19:11:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
