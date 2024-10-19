<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `buildpack-deps`

-	[`buildpack-deps:20.04`](#buildpack-deps2004)
-	[`buildpack-deps:20.04-curl`](#buildpack-deps2004-curl)
-	[`buildpack-deps:20.04-scm`](#buildpack-deps2004-scm)
-	[`buildpack-deps:22.04`](#buildpack-deps2204)
-	[`buildpack-deps:22.04-curl`](#buildpack-deps2204-curl)
-	[`buildpack-deps:22.04-scm`](#buildpack-deps2204-scm)
-	[`buildpack-deps:24.04`](#buildpack-deps2404)
-	[`buildpack-deps:24.04-curl`](#buildpack-deps2404-curl)
-	[`buildpack-deps:24.04-scm`](#buildpack-deps2404-scm)
-	[`buildpack-deps:24.10`](#buildpack-deps2410)
-	[`buildpack-deps:24.10-curl`](#buildpack-deps2410-curl)
-	[`buildpack-deps:24.10-scm`](#buildpack-deps2410-scm)
-	[`buildpack-deps:bookworm`](#buildpack-depsbookworm)
-	[`buildpack-deps:bookworm-curl`](#buildpack-depsbookworm-curl)
-	[`buildpack-deps:bookworm-scm`](#buildpack-depsbookworm-scm)
-	[`buildpack-deps:bullseye`](#buildpack-depsbullseye)
-	[`buildpack-deps:bullseye-curl`](#buildpack-depsbullseye-curl)
-	[`buildpack-deps:bullseye-scm`](#buildpack-depsbullseye-scm)
-	[`buildpack-deps:curl`](#buildpack-depscurl)
-	[`buildpack-deps:focal`](#buildpack-depsfocal)
-	[`buildpack-deps:focal-curl`](#buildpack-depsfocal-curl)
-	[`buildpack-deps:focal-scm`](#buildpack-depsfocal-scm)
-	[`buildpack-deps:jammy`](#buildpack-depsjammy)
-	[`buildpack-deps:jammy-curl`](#buildpack-depsjammy-curl)
-	[`buildpack-deps:jammy-scm`](#buildpack-depsjammy-scm)
-	[`buildpack-deps:latest`](#buildpack-depslatest)
-	[`buildpack-deps:noble`](#buildpack-depsnoble)
-	[`buildpack-deps:noble-curl`](#buildpack-depsnoble-curl)
-	[`buildpack-deps:noble-scm`](#buildpack-depsnoble-scm)
-	[`buildpack-deps:oldstable`](#buildpack-depsoldstable)
-	[`buildpack-deps:oldstable-curl`](#buildpack-depsoldstable-curl)
-	[`buildpack-deps:oldstable-scm`](#buildpack-depsoldstable-scm)
-	[`buildpack-deps:oracular`](#buildpack-depsoracular)
-	[`buildpack-deps:oracular-curl`](#buildpack-depsoracular-curl)
-	[`buildpack-deps:oracular-scm`](#buildpack-depsoracular-scm)
-	[`buildpack-deps:scm`](#buildpack-depsscm)
-	[`buildpack-deps:sid`](#buildpack-depssid)
-	[`buildpack-deps:sid-curl`](#buildpack-depssid-curl)
-	[`buildpack-deps:sid-scm`](#buildpack-depssid-scm)
-	[`buildpack-deps:stable`](#buildpack-depsstable)
-	[`buildpack-deps:stable-curl`](#buildpack-depsstable-curl)
-	[`buildpack-deps:stable-scm`](#buildpack-depsstable-scm)
-	[`buildpack-deps:testing`](#buildpack-depstesting)
-	[`buildpack-deps:testing-curl`](#buildpack-depstesting-curl)
-	[`buildpack-deps:testing-scm`](#buildpack-depstesting-scm)
-	[`buildpack-deps:trixie`](#buildpack-depstrixie)
-	[`buildpack-deps:trixie-curl`](#buildpack-depstrixie-curl)
-	[`buildpack-deps:trixie-scm`](#buildpack-depstrixie-scm)
-	[`buildpack-deps:unstable`](#buildpack-depsunstable)
-	[`buildpack-deps:unstable-curl`](#buildpack-depsunstable-curl)
-	[`buildpack-deps:unstable-scm`](#buildpack-depsunstable-scm)

## `buildpack-deps:20.04`

```console
$ docker pull buildpack-deps@sha256:d241c010495cd2dda8ee338ca9e9d89dbe8581e382bd46eb1921b94dd36181a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:20.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9b3ebcc0b86e6ce78d24a0700d1678e1a7c57d528e5d38f8ccb3df6479db1663
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245810083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debaf07f39de1c2707459d96d82457876d881c277170856d4313ed46fb1bea5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 02:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 02:02:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3c174c6b504b85dc37643886585b2569b5cdafef538fba161e83e9b4778dda`  
		Last Modified: Wed, 16 Oct 2024 02:08:03 GMT  
		Size: 11.1 MB (11149363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972d7a9a684adcf6dd4006f62d85e169235f480e937357a7d824bae53c1caddb`  
		Last Modified: Wed, 16 Oct 2024 02:08:19 GMT  
		Size: 60.9 MB (60925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6611992d2777e1b35adb90562ca8d25aceff6628589464e896d87ab59f8b98c9`  
		Last Modified: Wed, 16 Oct 2024 02:08:45 GMT  
		Size: 145.2 MB (145150960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88b014d36a585fc80c03c18e81db498ea6a2cc8fe63f6b7970d50988fec1b4e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86181f7988f85f5bb0e8890430b79aeffb7e6799ea4f8b6d4d8b724c70807692`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85418fe461856e419c5868f0e9e1f96a4ed78b150102e641b5fe7857f36a3313`  
		Last Modified: Wed, 16 Oct 2024 01:27:55 GMT  
		Size: 55.9 MB (55883691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cca2489adff278a53195ce381982f82039209fff1b3e492c207cbd9ec073277`  
		Last Modified: Wed, 16 Oct 2024 01:28:21 GMT  
		Size: 122.0 MB (121980193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:495b6b4d58f94e94d1f22015d0d249c9649095a7d063b32c736fb2c916e42eef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496889ddbe9850404c3f52ea7b95ad2db7ab56a92d8207750b740ac4cb3f4b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:24:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39f9d5b8d7b30e36de2e9aeed0f6ae96330e08473b8c9f609ca57f6740ef24e`  
		Last Modified: Wed, 16 Oct 2024 01:30:06 GMT  
		Size: 61.1 MB (61064176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fc637cf2bf691076a7a288a69201040457239da81e7cfa38e752d8622d5e25`  
		Last Modified: Wed, 16 Oct 2024 01:30:27 GMT  
		Size: 136.8 MB (136833370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c0550be955c837b134542411a398204029bf53e6f9e0d51f27dcb45967c7ed9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269572199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cc7ca3bc451a92d9dfefa590dfafe32c7d5c7bab50dc881759093991b06d91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:51:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:55:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cea2472a450c114a5052b42d3fc38c28fdfc12a3ef4b6aae683f81aa37195d`  
		Last Modified: Wed, 16 Oct 2024 02:01:25 GMT  
		Size: 69.7 MB (69663815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b651cb541d90efde7531c763c124c010c282b207cdf55a59cd980b277c39b96`  
		Last Modified: Wed, 16 Oct 2024 02:01:57 GMT  
		Size: 153.6 MB (153629537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d6d8d22022ec56d91caa0428898729d39abe8195be409c90331dfb6292da3efb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226623100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004905e37a12a43dc78b13d068fa44565c443ce79ee355c0ef0651dcc2a9408d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:12:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f6200608896e11eb9c555f60321de8024fd186eda924fac7d707c8635deb6`  
		Last Modified: Wed, 16 Oct 2024 01:17:10 GMT  
		Size: 60.4 MB (60354635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0867c4ef82fe17632eb9e7d1f8cf34b68a638c5a885ec9075319dbaad450c7`  
		Last Modified: Wed, 16 Oct 2024 01:17:32 GMT  
		Size: 128.6 MB (128550532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:c10d80a6cef97f29cce9b4a9933edb1ae51bef72d1b229db872500654c55f7da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:20.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0422293bc781517a1205b2ba6dff7ba236217c9327f8af92e264ba52f93484b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38658092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90edfc157d0d40a2b2be22d1471c22b1abd30fce2d83cc55b4f3927fd7a3f52a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c439405a1dd88c17c6ae4e1c05d5c4a282f8957203f506a1d3b8c0b018b66b3`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 11.1 MB (11147032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:116a19e525bb1d8197b26528a2b5ef7fedd9b8d08d42e8f0a74b5f58b28976fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef3471432bdf86cd7eed5ee88b82b6d4f8bfa3b8b7fdcce6c6319530cd28365`

```dockerfile
```

-	Layers:
	-	`sha256:304c699502debcf5c70a97fb9fb35a4238f59c74a383b028c33d0138d0244daa`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 3.1 MB (3053230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ad0bc1951b5669a88f7481c27f808527008c18d6b05fcf4e25e2ac39fadc42`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6d5af74c4c9c3fcc10fd966a3aba732b040df8e0f8b64579fe8709abf6828069
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34222511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6793273caf9681cfeeec22a2d20ae25d259ccb4b033642782a446675710937`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:981a354c335094f3746a3364ae7ed63fe12b58e4eb841b2f1d5fc66e3276f29d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38197604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13084ced7fb40b2e72f496978a2b6841e6ccdd0c97df7a2922f8ad2288d180ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5813c44733c05ac8f2e589a10fbb3dff6773488a51e8d2a6b0c19d78a3e2b2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46278847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d1a0327b1c6fabad97bf55eaf53ded9fa9052e73833b3cdd37dab0c60448a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cf51dfb6844a8168bb45516adac8fe583608d638eb19a4937ed76b1faf10f5eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33886994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0caf00bd51c4aba7d35a1cfb79ba0956d472c90f6b5ca1ae8db5959711e7e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:55:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:55:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:55:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:55:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:56:05 GMT
ADD file:f99ddac77e3940392223df513cab07fbc1fbae5269b21e7c49c63c99a7e47b14 in / 
# Fri, 11 Oct 2024 03:56:07 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:13:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd752079599d09732ebbf1df6f25eb9d82bba65ae8d0a5b9c9a50198e7b87bcf`  
		Last Modified: Wed, 16 Oct 2024 03:23:21 GMT  
		Size: 24.2 MB (24248406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795dc62932e4af3f391cb1dc8fa846d59ebed7d3c85ad038201d145e6368c75d`  
		Last Modified: Wed, 16 Oct 2024 03:23:11 GMT  
		Size: 9.6 MB (9638588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c5031c9f74e3eebfed6b04291ce3dddf756a7ec7b4ae99f6684662418bd0ec07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37717933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c51eb46351e70f1ffaf7c77701c0a457ec94962754b90d3c775cf57fdfe893`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:4320b97627d97a458a4cd9348b51f1671eb9410998415df3915b8379f89d083c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:20.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f327062623d74b25e110c9720f48a2c4cfde7258c2bf6ff73465d2aa0a57448b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100659123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d09ac9a103ecfb031c7d68d3a0eb82534b2ea5f924d251e07084bc29abf95d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 02:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3c174c6b504b85dc37643886585b2569b5cdafef538fba161e83e9b4778dda`  
		Last Modified: Wed, 16 Oct 2024 02:08:03 GMT  
		Size: 11.1 MB (11149363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972d7a9a684adcf6dd4006f62d85e169235f480e937357a7d824bae53c1caddb`  
		Last Modified: Wed, 16 Oct 2024 02:08:19 GMT  
		Size: 60.9 MB (60925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aa6c38d1c8b47f919623c61e4b1ed3755303d5308f3b7fc4aabe2ac3610ffc88
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90106202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7dc91eada8c5166d5338ac36c113b30ee455396979537e81b89d78147c38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85418fe461856e419c5868f0e9e1f96a4ed78b150102e641b5fe7857f36a3313`  
		Last Modified: Wed, 16 Oct 2024 01:27:55 GMT  
		Size: 55.9 MB (55883691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:961ecb6faef4c3c7fecddc09fd87de8fe914457e348c8d79a61948bf4fe60c48
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99261780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b49a58cd0cb1dd35c409ccba90f3fc69017f4b7857bcec31fed296231d3c28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39f9d5b8d7b30e36de2e9aeed0f6ae96330e08473b8c9f609ca57f6740ef24e`  
		Last Modified: Wed, 16 Oct 2024 01:30:06 GMT  
		Size: 61.1 MB (61064176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0726973e28d1af6b78ea1d6932dcd99e0f322f0842c32af042387b92243883a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115942662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dd0636a616868ba295cfcfcddf5a6c2e0874bd8aa8601a23135816608c86c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:51:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cea2472a450c114a5052b42d3fc38c28fdfc12a3ef4b6aae683f81aa37195d`  
		Last Modified: Wed, 16 Oct 2024 02:01:25 GMT  
		Size: 69.7 MB (69663815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78631683c7e021c9b83e5f6c59b82a784ec2ad419bfd6b2f85eea7721ca50356
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98072568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ea0f7d5580b3b0060c2bce75d80338579b73ccb93db238a866f0abf88f7d34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f6200608896e11eb9c555f60321de8024fd186eda924fac7d707c8635deb6`  
		Last Modified: Wed, 16 Oct 2024 01:17:10 GMT  
		Size: 60.4 MB (60354635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:9c1f5b3e9f425a09459e7c823cf9a1662cf93bde6a3c141c1a7d2cd5dd667a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:22.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c326e28c6c89f5f3dcffc84f4c9600328d09a833ad438cfff97f82604713457b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250113504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c58935b80a9003af58144e7f57501f94bfe801b3702cc3e1741cecf8a01abe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:43:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321cd5ae2a05dc61774ea917ff22fb166f1b67cd06921fed6f4270e0caf4c28`  
		Last Modified: Tue, 17 Sep 2024 00:51:03 GMT  
		Size: 7.1 MB (7091507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0473099c79c1b90b89fe006a5bd9596b9ece18ac24a399144f285ccf6c7d77`  
		Last Modified: Tue, 17 Sep 2024 00:51:19 GMT  
		Size: 39.5 MB (39469554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34ef741234642886403a8c4df20546c586b494892aef32c67b38744d708eb91`  
		Last Modified: Tue, 17 Sep 2024 00:51:47 GMT  
		Size: 173.1 MB (173112510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cacabfd612a657383015da3b566cc38ebd8d63e2b3f6173e2771cb625f5eede1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217350832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afbca593ecafee79c514fc783c161f17f3b2b62d80d148bbabe0c1bb2fa69a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:32:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f084e39677777a3c9198d380890db30c595eeb224db5b12fee6f43e975e333e5`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 42.2 MB (42247087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5428a7a155b8c4a2bddcefa0cb3cffa3343bb300965386df61df35ca415bef`  
		Last Modified: Tue, 17 Sep 2024 01:42:33 GMT  
		Size: 140.6 MB (140577512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d347c72fdb04979513c5bedb1d82366a94e80af9fbf0ab8e75c1b4faccf74ea2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241381156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fe605ca3566f74631040ea87601bdca43646561109e111cbf19c7845bc1ae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd83996b821ee5c0621feda52f2e1c48acc45c95fdbed9c47ac71c763ee53ab`  
		Last Modified: Tue, 17 Sep 2024 01:29:00 GMT  
		Size: 39.4 MB (39382970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e50e4827436e87a0777ab93c99b847eeda10ba41ba55dd724ba2cc6840a3bc`  
		Last Modified: Tue, 17 Sep 2024 01:29:24 GMT  
		Size: 166.6 MB (166567609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0749e42ed9e7d82deaeb34063735028d06e415fc5df5237ef15d068881a894f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271159362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf2d372bfa87e12926c336e3d7055d25082fe97548afc259ed97d70ee13f655`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3363e80d9b6d155f0ae139ce77aa32fd94df6eb46f50a3bec738d1033d8f32`  
		Last Modified: Tue, 17 Sep 2024 00:52:23 GMT  
		Size: 43.8 MB (43764044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc376bcd3849d1f0ea14fd75ec0bbed1615ddcf264fdaab646559938b61f729`  
		Last Modified: Tue, 17 Sep 2024 00:53:00 GMT  
		Size: 183.6 MB (183619620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c57d75bf05d4bab2e022d3e842430b445f90f49cc8ad6d8ef99c4c4339573266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274998466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40352b6e725bf98efdedaad84fcb7d82ed3d7afc5cf49388dc1301e69423b17a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:09:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8da1cbeb5ba78f9eb56920d49a58264a0e7f14bbbb546d6b818c307ca003982`  
		Last Modified: Tue, 17 Sep 2024 02:32:23 GMT  
		Size: 42.3 MB (42310711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d554bc49741eead5a08fa892cae07d2c98d5af01d2a3c5c8bc0b29b54abce41`  
		Last Modified: Tue, 17 Sep 2024 02:36:14 GMT  
		Size: 197.9 MB (197877479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:696292af1d26c3e8c085afefb22b79f16f3bbc7d8e9d65403f6bf33da393e0aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223812994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c7a372866a47e4d435a688a1067619591e80eee4a416b559330b48c878f69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:21:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200351c809009210c9ff3d95069658520c0808d693cf45463f14174972dffc8`  
		Last Modified: Tue, 17 Sep 2024 01:28:32 GMT  
		Size: 39.4 MB (39402519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdec65aff96ff434bc4106f0c66ab384f539df6dbafc567f21e7230089561faf`  
		Last Modified: Tue, 17 Sep 2024 01:28:56 GMT  
		Size: 148.8 MB (148767675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:ae4af6f3df25c1b472522b9e13b5f35ee4f65096876eb5fb508efcdad48f366b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:22.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e9e575bbf5fbd08b92fddfefa92a1f03825ef05ad773b4487eee6acfed264837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36638538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f765ea36fa4c46759dd690bb21cb8e45f32e1aa331cf9ad0da8b14816aa41ea3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad27316a38d3124ad8c0ef153c2a1fd356e6101cd2de78b49c0a1517f8e5f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a608399f965e1ef663c83205965174b05b375eba24e149c27e9cab4aeb91d`

```dockerfile
```

-	Layers:
	-	`sha256:1abede6965aa4c2f6dc7a23f51f9c10eab34e628cee2f9817cc259b2558d4d18`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 3.1 MB (3052568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1388bf3300d1894b794c3a79d61de4d5106bdcc7c16afd59021479c3346dc8a5`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a386ceaced73908c3b2ec5209db77b79b89054708ed73a630f05692cb32988eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34526233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5055a79c33ff49f2b7a9ea7bb980a1773c71b1d1ebc3e1fc9ec5daca7291b0d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:af723939f6a825e45913abe8955cab448bdfd8936a39c16e659f91fcd144e3a4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35430577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e6b3dc27b4071b35d0cccbe9d23dcb58c89ed7a6c74c5e178bd33234868d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fed7336e23d888337e23d27695e23b4629e6acc4864524291cbe911bb70bbb1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f50214c19651adb2c75be6a4d53624f0afa8be5e3011001a1930327b1e7e125`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:88ac494669975d9a648dc4f0217bf60e63aece135e9702b453b4d55b2296560e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be795c3e0e66e0ce4e2ee4d9b69c50ee968f836b15e16315c18f2b22c613d30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c578d3cc73855731ab4024c9120b974dc71bed918cb787254c69a305c21f0509
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35642800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da860bf0b99a8d35b13a4d49f791813c8d6aa4335cc2c25235b0ccb01de1cdec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:3347f2dfd51fd5a989d0efef1e408248aeb86cbe84193727b2b3d785b0486c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:22.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3bb7d3ba4a80fd483a455822fce478f604dd7827f989977aa93e7766673c3813
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77000994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd888b4f921a3f2e51866a336cc5ed86111ec15ec8549bf15961b9518fd27f86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321cd5ae2a05dc61774ea917ff22fb166f1b67cd06921fed6f4270e0caf4c28`  
		Last Modified: Tue, 17 Sep 2024 00:51:03 GMT  
		Size: 7.1 MB (7091507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0473099c79c1b90b89fe006a5bd9596b9ece18ac24a399144f285ccf6c7d77`  
		Last Modified: Tue, 17 Sep 2024 00:51:19 GMT  
		Size: 39.5 MB (39469554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ca89d3c84aac26f46e6bb0cdeaab9f13a9e6ef1232c9f88d738920468cee04c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3865fc6395b60b13dcf7604154e8af62468ec80630d7e29c3d8fa721f79324`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f084e39677777a3c9198d380890db30c595eeb224db5b12fee6f43e975e333e5`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 42.2 MB (42247087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:34b279fc4700c4c672e2f22e3280bae0cb0c280f525b541c37ca65d60825ee44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74813547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704307d21ad72ec302a4cc79016a0bf4a76c059c059bed698eb499cb6235066`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd83996b821ee5c0621feda52f2e1c48acc45c95fdbed9c47ac71c763ee53ab`  
		Last Modified: Tue, 17 Sep 2024 01:29:00 GMT  
		Size: 39.4 MB (39382970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1b8326726907980331fce56e29898f8fa15de30f322f5a2acd9f53783f8a9988
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87539742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee69e7ca45d862356910e271c2350fdd3b4e2c808aa97078e0189a2c53a3fed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3363e80d9b6d155f0ae139ce77aa32fd94df6eb46f50a3bec738d1033d8f32`  
		Last Modified: Tue, 17 Sep 2024 00:52:23 GMT  
		Size: 43.8 MB (43764044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:543266395b2597cfe93dfa4c7296684c535b15b50cb1ac4571918f69ee613316
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77120987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2661a6202957a6278bc4f96ae15f34541d0e2a163f56b6d81d87b8831f4f07b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8da1cbeb5ba78f9eb56920d49a58264a0e7f14bbbb546d6b818c307ca003982`  
		Last Modified: Tue, 17 Sep 2024 02:32:23 GMT  
		Size: 42.3 MB (42310711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee2acc822f0c058c87d4ef405f40716f7a0c2f268e4f43d66b4f709e2358f9ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75045319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c98d55db1472725ecfd27f682daeb79ae243193ac474e45aa974d502e56786`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200351c809009210c9ff3d95069658520c0808d693cf45463f14174972dffc8`  
		Last Modified: Tue, 17 Sep 2024 01:28:32 GMT  
		Size: 39.4 MB (39402519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:e8a9695d1d33b833cb4b09240e2c82a974ac41e6e8a82453fe77fb00730a5438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2643b4f2b82e8660bc0fdb8b391a60eb11a35461482d70d589caec7699207ac7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281087023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95e358ddbec82a0acfa688fa0dab9ba24e70fd73892cdc8d3f17de957f69018`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:07:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:802008e7f7617aa11266de164e757a6c8d7bb57ed4c972cf7e9f519dd0a21708`  
		Last Modified: Fri, 11 Oct 2024 09:51:09 GMT  
		Size: 30.6 MB (30610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce655b4c36ffd598797e82b3de3b049b04e79dbe27a847746f19cff42809f`  
		Last Modified: Wed, 16 Oct 2024 02:08:56 GMT  
		Size: 13.6 MB (13617894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36bf0492511d9dffc772e3618c5b2bce4c68245d25303931ad3fb85f3a6664c`  
		Last Modified: Wed, 16 Oct 2024 02:09:12 GMT  
		Size: 45.5 MB (45477297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63b34e199646383ec856bcaaa87784a4a45bce0e45b0284a7ca6d9707cef5e3`  
		Last Modified: Wed, 16 Oct 2024 02:09:43 GMT  
		Size: 191.4 MB (191380913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:713612cf63766ebb404e1a52a360fad7d397e21e3088d7b2a28ae74ba98da8ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241159665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da6778e238916247540e12782a664d323959de709bc94752f0d93d82ab3f4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:26:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c34db50907d073cf30d59433a5b4eae93a48fa52ede9ea3b913d0b753160ad`  
		Last Modified: Wed, 16 Oct 2024 01:28:49 GMT  
		Size: 49.0 MB (49028067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9916eb9191a57d65bee2b4f5544d08a9333e77bd43d114bd7be0aef2f69d116a`  
		Last Modified: Wed, 16 Oct 2024 01:29:17 GMT  
		Size: 151.6 MB (151621597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd255d45021e1cb092029d8623aef734733eddc32df3d3ba726eee7b49b2c8b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272159540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9859a96b988c661253c86126913ff807df44d99d7a5bf6511149514acd3b4fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b150961a20a0a06d6f810da85fa0f3e06e5942258e8d0f0ba7003e35f0fd02c5`  
		Last Modified: Wed, 16 Oct 2024 01:30:50 GMT  
		Size: 45.4 MB (45437380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419b5ae2bff4a1f7d611cfb936194e3d1699d162f16e2eb77ad3ddb981955824`  
		Last Modified: Wed, 16 Oct 2024 01:31:16 GMT  
		Size: 183.3 MB (183316090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c35798f4fce8f05eb7b8b497b5bdd619911732b04c7910a7f79d682524226324
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (300035872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da444111c347f5ad8acac23cbf5b3c98da7376b9b2b2c94fdf24925267cdcff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:57:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:00:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0b2b4d7e49ecab28973a1234e450767a55095ee5c46d9f6c5fda68a69d661f`  
		Last Modified: Wed, 16 Oct 2024 02:02:26 GMT  
		Size: 50.6 MB (50640454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1d065d6fd2e30971f802b752296ba5fc11ede3de6293dd006fb41bc2033fc4`  
		Last Modified: Wed, 16 Oct 2024 02:03:03 GMT  
		Size: 197.9 MB (197892979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:47a9ab4d22aa3bcc739d4282379cb397b0327dbe6055fbd0eb0792f52a9cb683
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331525136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90912f0b1b0b7da842a3f82ab73ff906bb40e95a7c269f9a78de04cd34b9790`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:21:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f7e1c8a9b4315a0ed15211421dba0019460f8a9083a212fa9fc751b5b81ec`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 53.9 MB (53939762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb2cc5f475f6ffd6d2efcc2334f54424e21e8704d54421d728b5bda8bbbfa23`  
		Last Modified: Wed, 16 Oct 2024 03:29:15 GMT  
		Size: 231.3 MB (231317673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d7470c586a514500739e65974b9a741e69ffafb92a3b28407b0a040b39042ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263237303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69d9df99fc5e4ab57f4fae574f5a15dfcf4fa579f47eaf33681abb2aa603e3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fe4420f7cc31e2e71a763e82cb5891ae4caf5f1904fbbe4513bb4cd423b516`  
		Last Modified: Wed, 16 Oct 2024 01:17:57 GMT  
		Size: 47.1 MB (47062541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971618b64005ee48e116c11ae3ec0d5fa0d62337b5252397597a384957f30154`  
		Last Modified: Wed, 16 Oct 2024 01:18:28 GMT  
		Size: 170.5 MB (170537217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:f2d116246e8e7845086d6c22e86a1b515bb9a42ef4e5fc34c6086c1c26f3834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:69a53f84746bd2372529e6294f001436f888e30870daf61281a69619b86057ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43367069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303bd2f189e17d8fbd2e62d67886dec77343f278c3c75cd273d299207c7b73a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0dff7df9d3a560fec4504795a8a76af7930b39ab2547e3ad5d56ae1246b7712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33382ecb57f630cddd0121e9581f247c374c0a13913cca08bc2ae9cf658ed9c8`

```dockerfile
```

-	Layers:
	-	`sha256:aae0f7d55899e7c0940b7b61d432d39e39e21cf565b7228a0eeba668dd220f63`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 2.5 MB (2460121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e5735a561089783c9f33d6a1c22c03d2914ddba32944dc3804408ca6f390f8`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9995076e2ae03b6f7a5b629e92c450245417849689d7cd49027eb652b67234d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40510001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e11aa0f6de1216a0ae7b41f4f9465a1d8750da4e073acd2ae2f62973d2d8d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6f5b67c405039f1cfd90f84c4af33431b848b7e5eedaf251a4499023bdeba4c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43406070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfb8b039c3cea45d5ea12f16c94c0a2926c998ec0c929368e66dfd9e0e5541a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:379ceb731b62e12334fb047ca39097cec13a0b1632dd6c1bb95ea02baa9cbc63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51502439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951036260e8de92532ed3f7de0131a75dd2509aacab1161fc3cd7588986f0967`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3f506d51d6119ce3ce143329a218e38cc9289d8771091be1858a95c8e8514694
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46267701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea764b821c3369419fd9f1e8af98d221f2c979549bd85a03112564680665fdd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60af0affbaabfa59a92d426e00c53b7736298ab01f0c19661d1f95ad89db8a83
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45637545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e84832735dbbb9016a6bcd6bfb982637edc98cfd427f79d3fbfc94d5f71607`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:945e4ecb1aa4514c81deda03c703cd80667b56f53a3a761be33a036ec04f4181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:74d825c93cdf67b18a81bd92b2d0dcc5ea410ffcf98aeb572b2e703a24fa2283
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89706110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9992f2715e5d4b38beb6ce736de50f3d64928eb3ede251bdf3d8193d161b3e5f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:802008e7f7617aa11266de164e757a6c8d7bb57ed4c972cf7e9f519dd0a21708`  
		Last Modified: Fri, 11 Oct 2024 09:51:09 GMT  
		Size: 30.6 MB (30610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce655b4c36ffd598797e82b3de3b049b04e79dbe27a847746f19cff42809f`  
		Last Modified: Wed, 16 Oct 2024 02:08:56 GMT  
		Size: 13.6 MB (13617894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36bf0492511d9dffc772e3618c5b2bce4c68245d25303931ad3fb85f3a6664c`  
		Last Modified: Wed, 16 Oct 2024 02:09:12 GMT  
		Size: 45.5 MB (45477297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a06d232a7e643f4daa3c698adada949fc17a0fd20f47b1debeb8504404577af0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89538068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a39be091951674a4cbb94634063aca7bf984a766831b1fe21c8ad39c1b6b27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c34db50907d073cf30d59433a5b4eae93a48fa52ede9ea3b913d0b753160ad`  
		Last Modified: Wed, 16 Oct 2024 01:28:49 GMT  
		Size: 49.0 MB (49028067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6936451af0ed0a91229fc21e2c2c429ed854077e5b6360fae94e8089dea36fbd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88843450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9ddea909fdbb18cd569092953e76b7a61efb90a9c6aed2db4c7e8ff835c81f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b150961a20a0a06d6f810da85fa0f3e06e5942258e8d0f0ba7003e35f0fd02c5`  
		Last Modified: Wed, 16 Oct 2024 01:30:50 GMT  
		Size: 45.4 MB (45437380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3038197fed25007eda3256f4b2a57b81d6e897193c650a3809533a5b713f6b9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102142893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f197312de325f9248d1193327d98608528ff57eebaa5475f93ffa70840537d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:57:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0b2b4d7e49ecab28973a1234e450767a55095ee5c46d9f6c5fda68a69d661f`  
		Last Modified: Wed, 16 Oct 2024 02:02:26 GMT  
		Size: 50.6 MB (50640454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58bfee3b37ade385bd6d4489243657d8d601d1e5acac4ba402f472cd02c7236e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100207463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed1ee396bd81d04e194c94f7be101f93dfa563fd21a6f0ff9b34aecfc8fd3d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f7e1c8a9b4315a0ed15211421dba0019460f8a9083a212fa9fc751b5b81ec`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 53.9 MB (53939762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:670d048ac22ccac1fed74cfb5714c7e94b6258c1efc866c41da1395b3a26b83a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92700086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66fe8c0be99d7249a1f123ad94ec058fcd4204c0c34167e176e2edebcbe287a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fe4420f7cc31e2e71a763e82cb5891ae4caf5f1904fbbe4513bb4cd423b516`  
		Last Modified: Wed, 16 Oct 2024 01:17:57 GMT  
		Size: 47.1 MB (47062541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10`

```console
$ docker pull buildpack-deps@sha256:5590362c96c705460f483f556a2d0837fded373fa3569a60c07d684a148b436f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.10` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:688a8d17441926d680c64d52a17ba261b73b29bd6955bedb3ae74a10c8716154
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287552644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6447aa6b1e22be7b61d8470d3398317b8705fc464924d411b8156ecd6057f40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:15 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:18 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Wed, 09 Oct 2024 15:42:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:45:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:48:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43ed7ac192d3f50e551118286d2a59c5cdf9ae247515319b137995d2d91c1857`  
		Last Modified: Thu, 10 Oct 2024 06:10:56 GMT  
		Size: 31.5 MB (31497006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebe8581de16e2d108a8b8b443bb95f82e5cad32c8f55539cb51fdde9b3436ca`  
		Last Modified: Fri, 11 Oct 2024 23:49:36 GMT  
		Size: 15.4 MB (15351852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd7d65218420548fcafac6b160a3d5aa59ecc023e7dc66b84b5bc87977eed4`  
		Last Modified: Fri, 11 Oct 2024 23:49:52 GMT  
		Size: 46.6 MB (46552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00338c9ed1170da053bb792bbac38340426de9df9e9b33bc25b0145812151182`  
		Last Modified: Fri, 11 Oct 2024 23:50:24 GMT  
		Size: 194.2 MB (194151652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:183ff55827bdffbd19e81d560907a07cbd8380d60f74bc70a57265edbb659927
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249689229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2b05eb94afe2d9f97e104b90aaacc17449044623b553b406ccb96822857a12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:41:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:44:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504d197ab129fb5bf6269a181811d7443fd358b01cf3d0cdbfbf1f7e94a778f`  
		Last Modified: Sat, 12 Oct 2024 00:46:05 GMT  
		Size: 49.5 MB (49527237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2e428a54e779d37be7f87db612976720765d94283996921ad943a495bf729`  
		Last Modified: Sat, 12 Oct 2024 00:46:34 GMT  
		Size: 157.7 MB (157703878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2fd75582deee680615c3b70cbdd5ac956126d09379bcf537ff0d4b5b656de838
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281353475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9191d37723b6c0372f40a06bcccdf93aa4a45f0358e7123aaf6c93703c1c7de8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ffa9891ee7f3191d73f9178aa9a6cf0571e9f85014da289756abf79e90d4fe`  
		Last Modified: Sat, 12 Oct 2024 00:08:53 GMT  
		Size: 46.5 MB (46481307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1003351ad394f136be5f70383549702edeefff5c3ed4d81730a00e936a8fb10`  
		Last Modified: Sat, 12 Oct 2024 00:09:19 GMT  
		Size: 188.4 MB (188355990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b70c65c43d980c1b41ebe36a2126d8c70856f30cef5b7987202e836d76950d68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303024216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ca3def268ac1175bac2d3cf5c33c7a4c812c79d36658645315c82e562a9fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:46:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080368c5e29f148040c44902a5c8ab4b32ec2f0ad63b12f764de4230a80ef737`  
		Last Modified: Fri, 11 Oct 2024 23:48:29 GMT  
		Size: 51.8 MB (51822495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd100af345e4d68ed2ef702d8e378cce86158c1173a29884475e29a3e55a2`  
		Last Modified: Fri, 11 Oct 2024 23:49:06 GMT  
		Size: 197.8 MB (197784051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9e15f8c24d6c90d02fdca80fec7999e7fc16cae1d9b1c15b76919544ce7039b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71077a13e9477b604f394e11dda03dfdf6545214675a73d35f44970d51de4496`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:21:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7cdd9669889c44132ee8d3640a1da628cf56156b39012dbe64ca81599329f0`  
		Last Modified: Sat, 12 Oct 2024 08:29:10 GMT  
		Size: 54.7 MB (54677266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e6827872bc7b33fc8f425500eda0f9a7c630a6ff574ee369076eed769eddb`  
		Last Modified: Sat, 12 Oct 2024 08:34:30 GMT  
		Size: 276.3 MB (276314931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c2ff9fe0ccb48def463608838a0f7bd03444d5004277c2e12d56b7c456cee2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266544571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d8e737d4389dd93d0c17d005a20d2a5786fb05dd66bfb8348d501dd5bc223`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187f132b69cfccea48cca74390b7916df3cce52677c59ff2df716bc3e9c8e5`  
		Last Modified: Sat, 12 Oct 2024 00:19:33 GMT  
		Size: 47.9 MB (47893672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419866cbc9cd0dd6fbc3dd57960aca4d55d2f875b27b9ea37493d4712702131`  
		Last Modified: Sat, 12 Oct 2024 00:19:59 GMT  
		Size: 170.3 MB (170301344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-curl`

```console
$ docker pull buildpack-deps@sha256:03f80bb571a97f04cf6f6ce70cc27455bea50491907b2b311b5df89ec5c89623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.10-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c8064ce954a2d9c90bd2e16fdd31c7c0b20e66720232e562b71c781f6c00bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45957871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7b838a1e6a2498c0f2b75d67c8db81136efdc82a162f30a7585633d1d465a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:734f143b619a054aeaf675404b5a8b6bf169fef11b9e111e8a691436743a0b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d2b611b8af5dbe471921a51a30ed516be558eeaf85c1466481a13d6640a4ae`

```dockerfile
```

-	Layers:
	-	`sha256:04d1691c1daa2c8f7f4ed5fbb5bcfaa1d228a7b3502a02d4d0c606c8e2a69420`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 2.5 MB (2458653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470d7dbf100349d28fe574b0fc0e6eb056c846f0a7430a28ea4919e451ed1b6b`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5cceb2f547cb52fc3342e32fef41d79dd9a16dd8b9eccb8cc68d586752442712
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42458114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67665e512286002cbd3225e6ac838a3288fd31c2555234586ba4330b5621f93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d026840c1f2c42096cdb088df4b14a7c9c852a36f2d035828d99c7b74ad528c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46516178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdcdec574fcb50d0bf5119678c2bc0dea93736af2dfe682c13957abdf5a1314`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:817662eada8897a66e5dc015628c6f86e2f389162ec27464b08111d35facb2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53417670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459d95a79091922cb35dccd5f8acb872291a6183b2b9d44b661fc36ec2f16826`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d077992b788a9af765b5bd9cc8dfbfdfa4148a8f57a536e79b1c900ff703e118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71e2496c145fd637f68a99d79840efa4114692affcd6e12fa47c4173263fa86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41a996db9213db8294e64f1a4ec828a25b048b6f37748fc974fae24e9ef2da57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48349555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571e0eacd2affb23496465cae630c9165b919bc6913371f3468b298362990bdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-scm`

```console
$ docker pull buildpack-deps@sha256:de9f26fe6ce60095c25974c25874f6e8d5c75a11fe0fcc43bf9ff74a9a75cbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.10-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5c248dde37c72ac3abdab19a986369ae0b337bed09ccfbcbffcf66b2582f3ee5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93400992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26fda0f0406676c24cd39cbaf57090832888fbef6499c3731f7feb7f225e914`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:15 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:18 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Wed, 09 Oct 2024 15:42:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:45:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43ed7ac192d3f50e551118286d2a59c5cdf9ae247515319b137995d2d91c1857`  
		Last Modified: Thu, 10 Oct 2024 06:10:56 GMT  
		Size: 31.5 MB (31497006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebe8581de16e2d108a8b8b443bb95f82e5cad32c8f55539cb51fdde9b3436ca`  
		Last Modified: Fri, 11 Oct 2024 23:49:36 GMT  
		Size: 15.4 MB (15351852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd7d65218420548fcafac6b160a3d5aa59ecc023e7dc66b84b5bc87977eed4`  
		Last Modified: Fri, 11 Oct 2024 23:49:52 GMT  
		Size: 46.6 MB (46552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69f9082b0142c4f42e3a112957fc83d72b89b38fbb234fe5659e746d0070d22c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91985351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc6a0da45d1b7f338d9fa6bf0714944d9d132fa54dc02d52594df947cd148f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:41:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504d197ab129fb5bf6269a181811d7443fd358b01cf3d0cdbfbf1f7e94a778f`  
		Last Modified: Sat, 12 Oct 2024 00:46:05 GMT  
		Size: 49.5 MB (49527237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f1688b9daecc9916d1dbf1d42c2f392b04e4f5ca3ca02f0c185d2261963d5869
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92997485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975a3888f98975958159d11d7cf9fcf5128735180169e3025a8dbf1936d27c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ffa9891ee7f3191d73f9178aa9a6cf0571e9f85014da289756abf79e90d4fe`  
		Last Modified: Sat, 12 Oct 2024 00:08:53 GMT  
		Size: 46.5 MB (46481307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:256a8a2aa9efc3d54e483d9a501f7ccdb8256fedb44a7c086a4846bd113d448a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105240165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e09478d0dfe4e1b3652a6ec2abb7601543219a4f653e5e42ede46c3d333292d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080368c5e29f148040c44902a5c8ab4b32ec2f0ad63b12f764de4230a80ef737`  
		Last Modified: Fri, 11 Oct 2024 23:48:29 GMT  
		Size: 51.8 MB (51822495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4566c169ddd534c5c54766bd8fc75edef81eba31cb3723701737b6fc083cad98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103366511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc918e600c0ca7bf21d0e52d3d5499216d4ec0595915343725567971eae959f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7cdd9669889c44132ee8d3640a1da628cf56156b39012dbe64ca81599329f0`  
		Last Modified: Sat, 12 Oct 2024 08:29:10 GMT  
		Size: 54.7 MB (54677266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f80cfa969a2981aebb45fafdb780f05cacc35e483062eba3972b6f3fb609dac9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96243227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1253efef7f03ca83d90ff492afca75b21d9e78c33fb3ca808d5943e2f82ad124`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187f132b69cfccea48cca74390b7916df3cce52677c59ff2df716bc3e9c8e5`  
		Last Modified: Sat, 12 Oct 2024 00:19:33 GMT  
		Size: 47.9 MB (47893672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:c046095998963a7a48019c87e9bd44f112dad9e600c8cfd052942a2e05c84b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:42e2783ba3b0255f0c51a7e2140c959ce2b76c41edadcd86160ade6f2a0cd210
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349282342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4f1ee355f8fc26eca03b0e8d96f4de2b48e641ea4c2f3d53988bb238bcd8e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:17 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 17 Oct 2024 00:20:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:04:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:25b17e8aa430f3e5bcb80eb5bf8d037ec95ddd242aea4ec0f74d610061282790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316629383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c5935b372870d7f04491d61f1993c99057b2ad1f98130fcab6452319533806`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:24:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:27:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c114860f8d70d4b0766d6eb509df94ed04b6a417e0ad9060f9a9d43e84064ae`  
		Last Modified: Thu, 17 Oct 2024 01:35:20 GMT  
		Size: 22.7 MB (22729227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c96b0eadfdfa6388c6308313b6ff3f016dfa452d0521acc1979654342d6abf`  
		Last Modified: Thu, 17 Oct 2024 01:35:42 GMT  
		Size: 62.0 MB (61999097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614584ff99d2c7b6591b578a66d10c94c81692c6a8c18b8a42671dc8fc7ad543`  
		Last Modified: Thu, 17 Oct 2024 01:36:25 GMT  
		Size: 184.6 MB (184570538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9220348c2292a5c7836e61e5dcaced1895274a5fc67da8d9873bd3140bf89134
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301972566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c7123986773b7fb351e2663141d16472280b9d4938cb89a8abefaa75cf0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d133c6fb31d3251e78f2c641f7d145d5f5b2ab13265639c8eb02354c0ffe35d`  
		Last Modified: Thu, 17 Oct 2024 03:37:52 GMT  
		Size: 175.2 MB (175227696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f66285729903294ee7e6397f09e6e57a1c7b845f491a17236f379b66fca60bc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340197975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeedd65d53caa810d0605b471c43849f76115ad352b7c098195c75e586fe06e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac41aaa9ccd9258f7c6b8f1562698acdae4548533ae639ff6653baa08033c71c`  
		Last Modified: Thu, 17 Oct 2024 04:36:51 GMT  
		Size: 202.7 MB (202669297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1c21375b08b4d0f25f20769d2547d2948982c8e2744ea336a64d389f2a87c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351867123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c98997c4e35d7cb7e3a88082701de0bd4f2daa9ee328f9cdbb34e20318504e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ebe45cbbff83005bfa62fa86d2064e8ccedae2cd7617a6d60696a420bd1bb`  
		Last Modified: Sat, 19 Oct 2024 02:53:15 GMT  
		Size: 210.2 MB (210186933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34adb642fac5f95817489d8165bf13bf55504c9704e969f5d3c78af5f052ed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a43af330dd7cc88d66c01cbd66a2333691dd02459d83800710b92e3e526ad`

```dockerfile
```

-	Layers:
	-	`sha256:7c909413102d12d54aa31d8cc5582cbe0762e5a40d49bbf051d2cfced9df8ae8`  
		Last Modified: Sat, 19 Oct 2024 02:53:11 GMT  
		Size: 15.5 MB (15476264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854336bbcc82191d23e44fbe1fb86eed9659b15b27f56cc7343ed66df224eff6`  
		Last Modified: Sat, 19 Oct 2024 02:53:10 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eedf47cd0217818cf4687c2bed18ecec128b16af82475584ebbeabff390e5f70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326348772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71650f7afcc0ee2ce3640621c54788a7d5851b59ef46e25c54141eb87a7ea58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:08:45 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Thu, 17 Oct 2024 01:08:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:48:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb4cb3753c5260533ae9297767f8b73bc0cd6f1dc878635a173148920d80368`  
		Last Modified: Thu, 17 Oct 2024 02:08:35 GMT  
		Size: 23.6 MB (23647379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e244535d91d08a7c42eab7cd45ea82c43428356bc75a90c8d486507e9888f0a`  
		Last Modified: Thu, 17 Oct 2024 02:09:28 GMT  
		Size: 63.3 MB (63297195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8f8a184e3174b4b3b76091c95baf89a636e164f9c732b010464037c162209`  
		Last Modified: Thu, 17 Oct 2024 02:11:35 GMT  
		Size: 189.8 MB (189842579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bafc61e1014935dde758d5d8c2f2cf3614486ab7024e8c1dd51e5eca3d9a1e60
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363396234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa68f72feb2ed3326c5b70c46fc86e32731822125a51dc10faaca60d96896e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:44:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d27751f2c723de9cfb2cbb2775f1c16c1f3653cdff74eae652ff9cc1633eda6`  
		Last Modified: Thu, 17 Oct 2024 01:52:21 GMT  
		Size: 214.3 MB (214300830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22357b5316cabb794fe07c11c4af17599270f951b8c9e21430952eb1f022716b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318793259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6716f9f26b5e12b4faf3947ea48f9b157956dc7cab733983b5e315635eac4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:42:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77632955ee6981fa7ca39f104872912fb4579734ee466c2eb2d442ca4c8a29cd`  
		Last Modified: Thu, 17 Oct 2024 03:49:21 GMT  
		Size: 183.3 MB (183307845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:89f0653a0a912939914d7df4bfbf6b6759e1713ac7307b734d205628eb195879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f5bb9ad274f7483bca35b7ade28409ddc366a3030c721f8ec01945f49c1f1400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73606409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6595c5df915beb56b486d44173ffcd9c8778b221483592385d56eace9a801f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f0ef8013ba25f54dfd23730377c2d93f590a45df065a2fbd1f91b943b36a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c17604ff561b13d6f71ee7c0a751e0b1d183ffa185632d141c0ba72398ed3a8`

```dockerfile
```

-	Layers:
	-	`sha256:afafc89040020b7a28a31732e2dc724fbcf41e580d58b02b74e8b0b4a2872c90`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 4.4 MB (4365270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4400ed85ba89c4bbb3ecdd1deb3eec80325469a08196255657479cc4d709369d`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29e22265f8e27deff56e30507c4bf3c45395cf51cd0cb178b01a10d0e74fee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7708f0af4315775dde7d656b19d6d877ece75b21b2f7335d8bcba64cefecd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4af3bdf4e5d1217cfc39da2266dc0351e9da0d1cd982341b997f89ea78399711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9290411caaa63ac5ed8e0a3029f8c3819fbbc16a6f4487e2f8424d6bc5d62dd2`

```dockerfile
```

-	Layers:
	-	`sha256:09bac3dbe394bb359e9648ccd0cd52e4092634e941964afb8413c9256644626c`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 4.4 MB (4368785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66fbb3bdefadf96a90da6d4bba1633b49859fa6532385c149fde11810506952`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c662459553ad055a4708b89aa5566791ba9f6db440495230e423d3717ed80f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e198c6502a080d5a4c664099e8b9ff589ac930f16668d5f130cf883973bbaa81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cba624557f8771ff8e6f953c75df4617cfa8c60ca2b011736603d07c4444364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9976a29b32bbb9b5140ecd8b4bf572ea9cc6d74bd34b93452ba7cd5c03473689`

```dockerfile
```

-	Layers:
	-	`sha256:24a261958b30f61e4637a1276fecfd8dc488e904699a6f9c0198b7ff85717689`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 4.4 MB (4367566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6bc5453abd7e83a2ee028712e1c439a5056c837ebe26cafe5657b46bb64d60`  
		Last Modified: Sat, 19 Oct 2024 00:56:09 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b676273f23311ccc5244ff6e63155dad8b5bb55b6d82b8f4e8d33972ef6e4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa631a28a982643843676b9f863f4d093a30c8b4fb480687f9dd53bab255da5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a44f1891b371bcae4f11edff9fd8aba7516fce6c2ff75aa458027d07967d8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cbd7f1f078bdc9aecceee2b5a77d73e45b0bf9b977b377ddcf47db36b3e1b4`

```dockerfile
```

-	Layers:
	-	`sha256:579eb45b34cd6da0fb68f0f67d8357369dadbde36df878a8b285533dd9fb9385`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 4.4 MB (4365542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7295b715924a4334f4fbb9c240fcd002eea2c8913954669a52796ad9fa45891`  
		Last Modified: Sat, 19 Oct 2024 01:10:42 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4efd8cc6fecc767a4806aab581f19e51c45faa286f89478f3967e5eeff607d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75471772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2131351b74d10ef77e845cfcfcbd26ab0a63bb6cf71eb9d1b38b7a253694a7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8464dd421e7a13ca2df0a0ed389801a2de33aaa8ff036e0e0a6e3b59de523dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94482666a0f9222c4e2432930198f007ba125621aecbb5b0a20a303cf82f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:bd25bf9485ae7822635d94ac3ac93b79ed69aae815fe5d3237c28b028036df11`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 4.4 MB (4362326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daf96ddb27c922caa431414e6f3178b8a5546068f19f674e9e40d530b3a9207`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40a0ca2a9d801d94c209dd4e81179674356393b1bb85a7c778a3f4374809cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b37c7d352dda03ef9d6be2c8d635f31984a92699dab52f36b5d3f12c515f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fc9c2dd787c1afef1c1632c49d1eb5b563a6facb531dd8b470488959b3ab9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 KB (6798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4747016d2b84e54ffe37fd4cf0d9b6bb34a7055915405f718b1dd16b0a090478`

```dockerfile
```

-	Layers:
	-	`sha256:eff80f8d463471c1876e84ba06456595ac60a9fd7d52d23925ba9857a315e820`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 6.8 KB (6798 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:704d078e6f0512924e23fabc519c270c4337592544ac088b753a03beb2edca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae709f8a5a2c18f20fdfcc13765d33af7c929548193c66e87d682e2d4338628e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:802ada8d1fd6a69d696bd789b9e6ed88a9e51de5e365b475c2d0bb3e15964827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d70d877c0e5eb209272eaa51467fd68839cc0c02f90c896d0ef9848c923e5d`

```dockerfile
```

-	Layers:
	-	`sha256:b6e7a8cf77bf1496c9a858f7c7a6f5e188fe91072b7afb22d90ae72605902920`  
		Last Modified: Sat, 19 Oct 2024 00:56:53 GMT  
		Size: 4.4 MB (4369763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1ded31c90b6bb0502d04c6c8a2dd6581bfd17ac18f5381e46d9ad71ed29b0d`  
		Last Modified: Sat, 19 Oct 2024 00:56:52 GMT  
		Size: 7.0 KB (6997 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21adcc891214e1112da5648d6249bc00f6bf79e3e4f4877a81e94b9650c2abff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf3690d729d99a4c77c28f19d3e7ceb3e8a868a32d1fd17330077491fa06c6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b672735e07b6bfd358f69deeb922ae67580e9d16527ecebd87aebebf732dc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb7d494d53ee86cc3697683f361f7502649fb74eedbbf4aa682d707dc2b17a3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1dfd30ced67644e7b9d672f6c07044e4b073d0d5506e4c0fcce2d600a96042`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 4.4 MB (4364967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a34545ab0e16c7b338028391562e8fb28abcfdebbb1613eff8f60838579b1`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:b7b31cf258096b5047be55aa30dad94e2ceb052c8c9e10c00d35725b10ec1bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e413426d5ceb4bc8b8485584a2334f982af09c40a294c8bf8bf6cdaeeee9875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137996104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6a3fd709dc98777b4ee2dac0d91e0d775c501c5f754c2721afda51367884fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:267daf9a035387db438e0e46fd4b93300a407ab8d2a8a08471e53480601da952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b34fb506a8ed23e1d427f349569ab9a18e6805d6de10ec99ed6a589dd583cc`

```dockerfile
```

-	Layers:
	-	`sha256:9f092bdcc560f05d219daef70c3dbe1cbf5beb875614df187738facf640574ae`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 7.8 MB (7764370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305b58c6aa4607a016c86411aaec62620a8480a7db911cf2b1b620bc59033585`  
		Last Modified: Sat, 19 Oct 2024 02:06:35 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:065821ca01f5b46e546b666ebc542baa9cadd26c83971d920f718a4d04641532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132056978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c329746ec886de5abee981e2a8dad46f0a25ec5606516321a628ea9cec7098a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d8e5c6c3bd120c07665df831c223d98cd86db7ad072c55a7433e227d49b3d`  
		Last Modified: Sat, 19 Oct 2024 02:55:37 GMT  
		Size: 62.0 MB (61996882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:993bf84285db8ca4c11425d3a303adbe960660b326c4fe16d6692cff7d2cab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7175b75d18a4b7c149ef131238c169805dae0110254e68d196b78cef76713d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8b6c17ef335d13a13ac672b98127369486d26b77a478f85e6dda04d194d55425`  
		Last Modified: Sat, 19 Oct 2024 02:55:36 GMT  
		Size: 7.8 MB (7765924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1348c0de7b4712e505c350d0c2142d3801c2c26e7c23faa55c9ce197ddd624d2`  
		Last Modified: Sat, 19 Oct 2024 02:55:35 GMT  
		Size: 7.7 KB (7734 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eccb934d63bac8c068380c9805d9b43b7f336b4c18f3240641a37e90dca17cf3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126744870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e0a5ed5211488d49c46201bd0003329cdeac002c563154869325cec7f1e5c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:24ff51eac951beb8cae6eb10c9a6316b92ba535f6ce57b697816a2f90d9e35fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d53a93f46b21e92bf85f52aefd48305b7987e7037693f374d44cb5e8ce0324`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:273c4a697c5f46c260ff0dc5ce28da78d7895442714cfe2ae670c62596c94c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141680190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f891597f8aa0b920eab180791c23ad8f9ffc9da20a5a68b66b0c2a936320a4a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7c27a970016230430108f980988c338d4d1137a98cd2b936476020943ea3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0fde0a53d069f07ff292e0334b827638c5a995a20f008cb02dca195cc9b24f`

```dockerfile
```

-	Layers:
	-	`sha256:e43a3a69d39b1261a900b087590ce28109339ec7b0fb043a670c0683b9cc0a50`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.8 MB (7760446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f61feb336f32426818cb28c5c4aae9e6aeea748ea4612b3d85b14136f23d82a`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c927f08d08e798a2932be4e20dad881e66c13708cd3fd12432a15db03914f304
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149095404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a195c447ca2ab15bd44723fc52ceba6b8484d8f8e8b74bf23786dbff4233d1a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:96caeb2a156ac3e5a114582e769104d80579b8f79601b73c7f453b4d8c947bc0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849e1c7b1cd0aa3c234e84d733980139487f92521f08631a58f63d02eb0e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:25c99da22419b70f9ac9397db1c87a573939c884360ce11eb766635f2931e903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6fb1b551beeb414d904634652bd28a156fcd99b81d48f1f563a2137b4d66435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322637930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d2e2ff5e69fdb04ea12f2792b8e5a4c1d0e5540d7ca923b1c3e0ca980d5e76`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dcdbbe5c1d62201fcee2dd2ca8ca09ec165f840a8a7a9fe05e7875b49b468`  
		Last Modified: Sat, 19 Oct 2024 02:53:29 GMT  
		Size: 197.1 MB (197069718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec03d4652a03e963b3c0125d3d60275c0c1cf950c98fa03f69b85617d1f444df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5b52311e9c598f6e67ccbde69cff414afed1a62f0a580eb6ef7ac7581e44f`

```dockerfile
```

-	Layers:
	-	`sha256:a58854d3cfaddb475139d152911a8e319295947cb9e4d880b71f2359f6786973`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 15.1 MB (15097594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f19d6af261d1e6bfe9f8f4e9a6292e45a246ad6e9bac661e73d0706db7a455`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9620487d9a3dd979140faf498adb7797ad3ce6d3486906e1dca7293fded20bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283267265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a870836d352c022dc0b725162c10529ea61d91c79ce2aac4aa301362ddfd66d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:34 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Thu, 17 Oct 2024 03:03:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:30:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39efe447d42646f3185dd530992915f4ee5284d42835f09c0a8c04ba06ba134`  
		Last Modified: Thu, 17 Oct 2024 03:38:18 GMT  
		Size: 50.6 MB (50618781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102cf143efb57e0d7377d35f3f52584b742bbf4091d513fd71597ca2845e21d0`  
		Last Modified: Thu, 17 Oct 2024 03:38:49 GMT  
		Size: 167.5 MB (167526825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b25e42bc10765a3222a439524daa5942d5c6b6a2d5557d50a6bdc5d040fa7ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314298001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46fcaf6dce0b6e0a315dce9f0a57f58f729e94e5a348efcec8351fe4218db5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:32:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0134077e35514883cdc89f46185c7eae106a74a0895bfbc1494fdde44310f977`  
		Last Modified: Thu, 17 Oct 2024 04:37:14 GMT  
		Size: 54.8 MB (54834752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1f1670189accf143f4aa947a240b3dd83abfe6af77ebe02a7651953b171b5d`  
		Last Modified: Thu, 17 Oct 2024 04:37:38 GMT  
		Size: 190.0 MB (189978129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:35da12d82b0122d42f5bdfa6360d302249deaadd87cc7ceaf51e14bf64555596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328350614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690fe329d3a092d7f93dd6078a5993d7c2f79b49cf0b4b6df8f80a6bc3375ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668ade1ad6ecf9ecde05517f60eb0af8fbad048955aa9fa5125dfe9e07f656d7`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 200.0 MB (199977836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fde5e7bd54ba76c9a5a91073eed2d011f6a68186ba771799e49d857fd89f414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15096145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5034587ff849067841fd6614cbaa3735db9acb76a0bc5a91bb14193214ace858`

```dockerfile
```

-	Layers:
	-	`sha256:82c5aa200df2a044ae1a349683976749352850413f001243061e9bcaf2488761`  
		Last Modified: Sat, 19 Oct 2024 02:53:33 GMT  
		Size: 15.1 MB (15085935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2857c1dbbf9bffc7cb36818e082a24834e7d6117249c84160210df820841708`  
		Last Modified: Sat, 19 Oct 2024 02:53:32 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:498bf9195cd16d43171335249ed823b9c8f5cc4d4dc87423387e6ed7533febc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d3916e45c1b1919b65c5fcf324491e8d1b8c2380f96507ace92275a5723d318b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70842919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e9b58743a7381f5f53c8c6ed89dbf396fe86249f72b153da31e552319b0b28`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad90543a0cace80e4521c0c75ae897cd3bbb6852853f400beb3fed043465ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5490fdfd04a997fdf4839988fcca7e947362a72ef349b49747e39debf5a1e865`

```dockerfile
```

-	Layers:
	-	`sha256:c5efb53970567eaac415d819fedd7e79142f37beb0bb95d76686bed69e20bb95`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 4.5 MB (4492144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3f4bf535ae6901543c9781878d8215d7afa74196a9bdf1873b7512f6d18446`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce982925f7cb662229a416b8ad803c7a5ed65c69917a6fe3e519ac657ba2ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65119280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcde28c3186dce242f6150e5ebe0bb3c3a8f9fe6a7287a3cf88c06f85631668`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9811aa580423a2e552be714c14e210eacb5d77955466d3ca3381faccb47f5832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75437541a1b4d8578a4168a6c973fc1938cef6004aed71846971abe640ce1adb`

```dockerfile
```

-	Layers:
	-	`sha256:ee4e340b3a5aa96d9edd30cd59e56c6a84097292c754303d197005b000003d1e`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 4.5 MB (4493778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc400e038d817658fe4f5c569d165dfce2496c578f62facd784e7288a97c447b`  
		Last Modified: Sat, 19 Oct 2024 00:56:45 GMT  
		Size: 6.7 KB (6656 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ab97857735b9bb4ca0316c84af8cb47f468d79fbf7d69a7602a4a057be20d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69482684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5ace0446f1a3d88fd6d7eb94cc84129b0dc299b80045b5e26f87a3ce7b20b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c985a2a0b84bb74f11845a54a2cf9b51f2f79c056c15b4bd2e136676c9383502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0c728f5437aa596659b21909e26c3dc3ad3d1d64adb107edcf6d718397fc8`

```dockerfile
```

-	Layers:
	-	`sha256:6cfb03deb7abd3faa75a7f964fa9369e9644a2b85204515db2a447c862c83f36`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 4.5 MB (4491756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488572740765c205abccf12b5ac1f0f9f380f18333e681fb042fc29b61ce5b9a`  
		Last Modified: Sat, 19 Oct 2024 01:11:08 GMT  
		Size: 6.7 KB (6676 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fb117244a074d030af0177d95dfa02ae40a9dd404705ec11a8714d6de03266f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb4250e207301019763c2a652f7c0d6950982158eeea54d69191d031358628`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08b4591968723d4d0fdf75817cc1f2f6fbca81c6a5e3e32ce8551977603e00fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb7873e29a676043e203a9f966a180fa83afab781074edefcf1d757c1efeb5c`

```dockerfile
```

-	Layers:
	-	`sha256:7ceec0d5e1bcd10de39b1fab285826c265e8ae4449bc373c17ae99bffd7da1e5`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 4.5 MB (4488583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8a2025755a1ab2cc4010aed335945299dde3703a19af55f8126ca9ac074cd7`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 6.6 KB (6583 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:38e8bf2ca32551067ee504f09d30725145bae9290a848dbda17babae267c38f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f0485e10500024df9431d8de6763bdc6da543ca6ab1e5ab2057b421dcb7edaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125568212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51724573712708db097ecd36d4692d52fe503b6a5e588fa6d2f92d57448b75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86518255b538a594e8e2238131f87aa1d67981e1263e4c18db09e788a30e0211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8114d198645a070bb880f41004b7e18eb9b532cd04d152554c2198c33bedad58`

```dockerfile
```

-	Layers:
	-	`sha256:8119449007c140ad3218cd87f4c75621c38e919438ce0347d51fa76951bc74ed`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.7 MB (7720100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a0a9c5343eacf41f82ce1d610c6b28aacd5cce7e62805b6bfc9ab1dbb20dac`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6fb8dcf1b939160b597f606a99837dbd9e6b08a36e6cabb2d256645c9b1312f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115740440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9d27cbf62dbe2318150927b91f2d8046815c0477c72bfd27779197a5afd926`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:34 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Thu, 17 Oct 2024 03:03:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39efe447d42646f3185dd530992915f4ee5284d42835f09c0a8c04ba06ba134`  
		Last Modified: Thu, 17 Oct 2024 03:38:18 GMT  
		Size: 50.6 MB (50618781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d9929a8653d0de4548ba7e83976b23e404a4244ea7980582ff44948698faeb44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124319872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe2df2355dc642f0983dd1e359d38f267c0ad9c839b6448cbff86fc0f644854`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0134077e35514883cdc89f46185c7eae106a74a0895bfbc1494fdde44310f977`  
		Last Modified: Thu, 17 Oct 2024 04:37:14 GMT  
		Size: 54.8 MB (54834752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9890d2391771767d200b4cbf59d19803dc7325c67a668de520340c3585253ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128372778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfabefc5f8a6f86a4c1d0830952a6542af51cac814b2efcfecc61b068b812e6e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97f2982c47b11589dc67c23f4654b6f5ade92e8c507c09443e2500ca71371690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8bc9ab9f9ff20301bfe16816c4cefce0e403721ff906a1f90392f09c200edc`

```dockerfile
```

-	Layers:
	-	`sha256:fe45d08f635e7da0980c4e3a17abd1d69bd81cad7123343b7c0a8bedfdacd121`  
		Last Modified: Sat, 19 Oct 2024 02:06:28 GMT  
		Size: 7.7 MB (7715588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc67396d6c2b39edc8f2c0e27392aabce73e953884562fb7a86e6187cfa784d`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:89f0653a0a912939914d7df4bfbf6b6759e1713ac7307b734d205628eb195879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f5bb9ad274f7483bca35b7ade28409ddc366a3030c721f8ec01945f49c1f1400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73606409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6595c5df915beb56b486d44173ffcd9c8778b221483592385d56eace9a801f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f0ef8013ba25f54dfd23730377c2d93f590a45df065a2fbd1f91b943b36a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c17604ff561b13d6f71ee7c0a751e0b1d183ffa185632d141c0ba72398ed3a8`

```dockerfile
```

-	Layers:
	-	`sha256:afafc89040020b7a28a31732e2dc724fbcf41e580d58b02b74e8b0b4a2872c90`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 4.4 MB (4365270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4400ed85ba89c4bbb3ecdd1deb3eec80325469a08196255657479cc4d709369d`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29e22265f8e27deff56e30507c4bf3c45395cf51cd0cb178b01a10d0e74fee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7708f0af4315775dde7d656b19d6d877ece75b21b2f7335d8bcba64cefecd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4af3bdf4e5d1217cfc39da2266dc0351e9da0d1cd982341b997f89ea78399711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9290411caaa63ac5ed8e0a3029f8c3819fbbc16a6f4487e2f8424d6bc5d62dd2`

```dockerfile
```

-	Layers:
	-	`sha256:09bac3dbe394bb359e9648ccd0cd52e4092634e941964afb8413c9256644626c`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 4.4 MB (4368785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66fbb3bdefadf96a90da6d4bba1633b49859fa6532385c149fde11810506952`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c662459553ad055a4708b89aa5566791ba9f6db440495230e423d3717ed80f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e198c6502a080d5a4c664099e8b9ff589ac930f16668d5f130cf883973bbaa81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cba624557f8771ff8e6f953c75df4617cfa8c60ca2b011736603d07c4444364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9976a29b32bbb9b5140ecd8b4bf572ea9cc6d74bd34b93452ba7cd5c03473689`

```dockerfile
```

-	Layers:
	-	`sha256:24a261958b30f61e4637a1276fecfd8dc488e904699a6f9c0198b7ff85717689`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 4.4 MB (4367566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6bc5453abd7e83a2ee028712e1c439a5056c837ebe26cafe5657b46bb64d60`  
		Last Modified: Sat, 19 Oct 2024 00:56:09 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b676273f23311ccc5244ff6e63155dad8b5bb55b6d82b8f4e8d33972ef6e4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa631a28a982643843676b9f863f4d093a30c8b4fb480687f9dd53bab255da5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a44f1891b371bcae4f11edff9fd8aba7516fce6c2ff75aa458027d07967d8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cbd7f1f078bdc9aecceee2b5a77d73e45b0bf9b977b377ddcf47db36b3e1b4`

```dockerfile
```

-	Layers:
	-	`sha256:579eb45b34cd6da0fb68f0f67d8357369dadbde36df878a8b285533dd9fb9385`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 4.4 MB (4365542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7295b715924a4334f4fbb9c240fcd002eea2c8913954669a52796ad9fa45891`  
		Last Modified: Sat, 19 Oct 2024 01:10:42 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4efd8cc6fecc767a4806aab581f19e51c45faa286f89478f3967e5eeff607d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75471772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2131351b74d10ef77e845cfcfcbd26ab0a63bb6cf71eb9d1b38b7a253694a7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8464dd421e7a13ca2df0a0ed389801a2de33aaa8ff036e0e0a6e3b59de523dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94482666a0f9222c4e2432930198f007ba125621aecbb5b0a20a303cf82f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:bd25bf9485ae7822635d94ac3ac93b79ed69aae815fe5d3237c28b028036df11`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 4.4 MB (4362326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daf96ddb27c922caa431414e6f3178b8a5546068f19f674e9e40d530b3a9207`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40a0ca2a9d801d94c209dd4e81179674356393b1bb85a7c778a3f4374809cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b37c7d352dda03ef9d6be2c8d635f31984a92699dab52f36b5d3f12c515f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fc9c2dd787c1afef1c1632c49d1eb5b563a6facb531dd8b470488959b3ab9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 KB (6798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4747016d2b84e54ffe37fd4cf0d9b6bb34a7055915405f718b1dd16b0a090478`

```dockerfile
```

-	Layers:
	-	`sha256:eff80f8d463471c1876e84ba06456595ac60a9fd7d52d23925ba9857a315e820`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 6.8 KB (6798 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:704d078e6f0512924e23fabc519c270c4337592544ac088b753a03beb2edca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae709f8a5a2c18f20fdfcc13765d33af7c929548193c66e87d682e2d4338628e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:802ada8d1fd6a69d696bd789b9e6ed88a9e51de5e365b475c2d0bb3e15964827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d70d877c0e5eb209272eaa51467fd68839cc0c02f90c896d0ef9848c923e5d`

```dockerfile
```

-	Layers:
	-	`sha256:b6e7a8cf77bf1496c9a858f7c7a6f5e188fe91072b7afb22d90ae72605902920`  
		Last Modified: Sat, 19 Oct 2024 00:56:53 GMT  
		Size: 4.4 MB (4369763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1ded31c90b6bb0502d04c6c8a2dd6581bfd17ac18f5381e46d9ad71ed29b0d`  
		Last Modified: Sat, 19 Oct 2024 00:56:52 GMT  
		Size: 7.0 KB (6997 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21adcc891214e1112da5648d6249bc00f6bf79e3e4f4877a81e94b9650c2abff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf3690d729d99a4c77c28f19d3e7ceb3e8a868a32d1fd17330077491fa06c6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b672735e07b6bfd358f69deeb922ae67580e9d16527ecebd87aebebf732dc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb7d494d53ee86cc3697683f361f7502649fb74eedbbf4aa682d707dc2b17a3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1dfd30ced67644e7b9d672f6c07044e4b073d0d5506e4c0fcce2d600a96042`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 4.4 MB (4364967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a34545ab0e16c7b338028391562e8fb28abcfdebbb1613eff8f60838579b1`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:d241c010495cd2dda8ee338ca9e9d89dbe8581e382bd46eb1921b94dd36181a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9b3ebcc0b86e6ce78d24a0700d1678e1a7c57d528e5d38f8ccb3df6479db1663
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245810083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debaf07f39de1c2707459d96d82457876d881c277170856d4313ed46fb1bea5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 02:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 02:02:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3c174c6b504b85dc37643886585b2569b5cdafef538fba161e83e9b4778dda`  
		Last Modified: Wed, 16 Oct 2024 02:08:03 GMT  
		Size: 11.1 MB (11149363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972d7a9a684adcf6dd4006f62d85e169235f480e937357a7d824bae53c1caddb`  
		Last Modified: Wed, 16 Oct 2024 02:08:19 GMT  
		Size: 60.9 MB (60925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6611992d2777e1b35adb90562ca8d25aceff6628589464e896d87ab59f8b98c9`  
		Last Modified: Wed, 16 Oct 2024 02:08:45 GMT  
		Size: 145.2 MB (145150960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88b014d36a585fc80c03c18e81db498ea6a2cc8fe63f6b7970d50988fec1b4e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86181f7988f85f5bb0e8890430b79aeffb7e6799ea4f8b6d4d8b724c70807692`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85418fe461856e419c5868f0e9e1f96a4ed78b150102e641b5fe7857f36a3313`  
		Last Modified: Wed, 16 Oct 2024 01:27:55 GMT  
		Size: 55.9 MB (55883691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cca2489adff278a53195ce381982f82039209fff1b3e492c207cbd9ec073277`  
		Last Modified: Wed, 16 Oct 2024 01:28:21 GMT  
		Size: 122.0 MB (121980193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:495b6b4d58f94e94d1f22015d0d249c9649095a7d063b32c736fb2c916e42eef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496889ddbe9850404c3f52ea7b95ad2db7ab56a92d8207750b740ac4cb3f4b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:24:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39f9d5b8d7b30e36de2e9aeed0f6ae96330e08473b8c9f609ca57f6740ef24e`  
		Last Modified: Wed, 16 Oct 2024 01:30:06 GMT  
		Size: 61.1 MB (61064176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fc637cf2bf691076a7a288a69201040457239da81e7cfa38e752d8622d5e25`  
		Last Modified: Wed, 16 Oct 2024 01:30:27 GMT  
		Size: 136.8 MB (136833370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c0550be955c837b134542411a398204029bf53e6f9e0d51f27dcb45967c7ed9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269572199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cc7ca3bc451a92d9dfefa590dfafe32c7d5c7bab50dc881759093991b06d91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:51:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:55:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cea2472a450c114a5052b42d3fc38c28fdfc12a3ef4b6aae683f81aa37195d`  
		Last Modified: Wed, 16 Oct 2024 02:01:25 GMT  
		Size: 69.7 MB (69663815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b651cb541d90efde7531c763c124c010c282b207cdf55a59cd980b277c39b96`  
		Last Modified: Wed, 16 Oct 2024 02:01:57 GMT  
		Size: 153.6 MB (153629537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d6d8d22022ec56d91caa0428898729d39abe8195be409c90331dfb6292da3efb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226623100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004905e37a12a43dc78b13d068fa44565c443ce79ee355c0ef0651dcc2a9408d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:12:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f6200608896e11eb9c555f60321de8024fd186eda924fac7d707c8635deb6`  
		Last Modified: Wed, 16 Oct 2024 01:17:10 GMT  
		Size: 60.4 MB (60354635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0867c4ef82fe17632eb9e7d1f8cf34b68a638c5a885ec9075319dbaad450c7`  
		Last Modified: Wed, 16 Oct 2024 01:17:32 GMT  
		Size: 128.6 MB (128550532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:c10d80a6cef97f29cce9b4a9933edb1ae51bef72d1b229db872500654c55f7da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0422293bc781517a1205b2ba6dff7ba236217c9327f8af92e264ba52f93484b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38658092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90edfc157d0d40a2b2be22d1471c22b1abd30fce2d83cc55b4f3927fd7a3f52a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c439405a1dd88c17c6ae4e1c05d5c4a282f8957203f506a1d3b8c0b018b66b3`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 11.1 MB (11147032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:116a19e525bb1d8197b26528a2b5ef7fedd9b8d08d42e8f0a74b5f58b28976fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef3471432bdf86cd7eed5ee88b82b6d4f8bfa3b8b7fdcce6c6319530cd28365`

```dockerfile
```

-	Layers:
	-	`sha256:304c699502debcf5c70a97fb9fb35a4238f59c74a383b028c33d0138d0244daa`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 3.1 MB (3053230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ad0bc1951b5669a88f7481c27f808527008c18d6b05fcf4e25e2ac39fadc42`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6d5af74c4c9c3fcc10fd966a3aba732b040df8e0f8b64579fe8709abf6828069
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34222511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6793273caf9681cfeeec22a2d20ae25d259ccb4b033642782a446675710937`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:981a354c335094f3746a3364ae7ed63fe12b58e4eb841b2f1d5fc66e3276f29d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38197604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13084ced7fb40b2e72f496978a2b6841e6ccdd0c97df7a2922f8ad2288d180ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5813c44733c05ac8f2e589a10fbb3dff6773488a51e8d2a6b0c19d78a3e2b2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46278847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d1a0327b1c6fabad97bf55eaf53ded9fa9052e73833b3cdd37dab0c60448a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cf51dfb6844a8168bb45516adac8fe583608d638eb19a4937ed76b1faf10f5eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33886994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0caf00bd51c4aba7d35a1cfb79ba0956d472c90f6b5ca1ae8db5959711e7e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:55:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:55:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:55:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:55:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:56:05 GMT
ADD file:f99ddac77e3940392223df513cab07fbc1fbae5269b21e7c49c63c99a7e47b14 in / 
# Fri, 11 Oct 2024 03:56:07 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:13:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd752079599d09732ebbf1df6f25eb9d82bba65ae8d0a5b9c9a50198e7b87bcf`  
		Last Modified: Wed, 16 Oct 2024 03:23:21 GMT  
		Size: 24.2 MB (24248406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795dc62932e4af3f391cb1dc8fa846d59ebed7d3c85ad038201d145e6368c75d`  
		Last Modified: Wed, 16 Oct 2024 03:23:11 GMT  
		Size: 9.6 MB (9638588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c5031c9f74e3eebfed6b04291ce3dddf756a7ec7b4ae99f6684662418bd0ec07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37717933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c51eb46351e70f1ffaf7c77701c0a457ec94962754b90d3c775cf57fdfe893`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:f87fe7ec6e5046bdf6a347c939bb39dc564b05b05c7b7d989ab052d77929e672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:34d00f41b14c40e6903e630fb94b859f9e05c36b7016df768ccfa1791d797151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99583642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e735b8910a6f0ef6d4a756b8614bd1c6fa2d31394533387b293ca533eae4490`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c439405a1dd88c17c6ae4e1c05d5c4a282f8957203f506a1d3b8c0b018b66b3`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 11.1 MB (11147032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fed924c2a2b74fd07c670509feadf6fc8830b3356a2ad22a1066d9c45c02d`  
		Last Modified: Sat, 19 Oct 2024 02:52:27 GMT  
		Size: 60.9 MB (60925550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a367f3106529937f6d37be0ae11abc812d3e24785307e1385173da9994b8b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6680317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad62135b54e4b9715fb84ab88175f2b45bd6498a4d542e12d0ccacdd3ff1cad2`

```dockerfile
```

-	Layers:
	-	`sha256:222103d54b5ac8552ee50b42ecb802826506750cb0de3b1f27df69091e2249e8`  
		Last Modified: Sat, 19 Oct 2024 02:52:26 GMT  
		Size: 6.7 MB (6672935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f1f4ec088e4b6693c82001f201f75294ee1d693ede49bcfb6da307ec1cd5b`  
		Last Modified: Sat, 19 Oct 2024 02:52:26 GMT  
		Size: 7.4 KB (7382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aa6c38d1c8b47f919623c61e4b1ed3755303d5308f3b7fc4aabe2ac3610ffc88
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90106202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7dc91eada8c5166d5338ac36c113b30ee455396979537e81b89d78147c38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85418fe461856e419c5868f0e9e1f96a4ed78b150102e641b5fe7857f36a3313`  
		Last Modified: Wed, 16 Oct 2024 01:27:55 GMT  
		Size: 55.9 MB (55883691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:961ecb6faef4c3c7fecddc09fd87de8fe914457e348c8d79a61948bf4fe60c48
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99261780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b49a58cd0cb1dd35c409ccba90f3fc69017f4b7857bcec31fed296231d3c28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39f9d5b8d7b30e36de2e9aeed0f6ae96330e08473b8c9f609ca57f6740ef24e`  
		Last Modified: Wed, 16 Oct 2024 01:30:06 GMT  
		Size: 61.1 MB (61064176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0726973e28d1af6b78ea1d6932dcd99e0f322f0842c32af042387b92243883a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115942662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dd0636a616868ba295cfcfcddf5a6c2e0874bd8aa8601a23135816608c86c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:51:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cea2472a450c114a5052b42d3fc38c28fdfc12a3ef4b6aae683f81aa37195d`  
		Last Modified: Wed, 16 Oct 2024 02:01:25 GMT  
		Size: 69.7 MB (69663815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78631683c7e021c9b83e5f6c59b82a784ec2ad419bfd6b2f85eea7721ca50356
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98072568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ea0f7d5580b3b0060c2bce75d80338579b73ccb93db238a866f0abf88f7d34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f6200608896e11eb9c555f60321de8024fd186eda924fac7d707c8635deb6`  
		Last Modified: Wed, 16 Oct 2024 01:17:10 GMT  
		Size: 60.4 MB (60354635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:9c1f5b3e9f425a09459e7c823cf9a1662cf93bde6a3c141c1a7d2cd5dd667a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c326e28c6c89f5f3dcffc84f4c9600328d09a833ad438cfff97f82604713457b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250113504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c58935b80a9003af58144e7f57501f94bfe801b3702cc3e1741cecf8a01abe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:43:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321cd5ae2a05dc61774ea917ff22fb166f1b67cd06921fed6f4270e0caf4c28`  
		Last Modified: Tue, 17 Sep 2024 00:51:03 GMT  
		Size: 7.1 MB (7091507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0473099c79c1b90b89fe006a5bd9596b9ece18ac24a399144f285ccf6c7d77`  
		Last Modified: Tue, 17 Sep 2024 00:51:19 GMT  
		Size: 39.5 MB (39469554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34ef741234642886403a8c4df20546c586b494892aef32c67b38744d708eb91`  
		Last Modified: Tue, 17 Sep 2024 00:51:47 GMT  
		Size: 173.1 MB (173112510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cacabfd612a657383015da3b566cc38ebd8d63e2b3f6173e2771cb625f5eede1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217350832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afbca593ecafee79c514fc783c161f17f3b2b62d80d148bbabe0c1bb2fa69a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:32:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f084e39677777a3c9198d380890db30c595eeb224db5b12fee6f43e975e333e5`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 42.2 MB (42247087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5428a7a155b8c4a2bddcefa0cb3cffa3343bb300965386df61df35ca415bef`  
		Last Modified: Tue, 17 Sep 2024 01:42:33 GMT  
		Size: 140.6 MB (140577512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d347c72fdb04979513c5bedb1d82366a94e80af9fbf0ab8e75c1b4faccf74ea2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241381156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fe605ca3566f74631040ea87601bdca43646561109e111cbf19c7845bc1ae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd83996b821ee5c0621feda52f2e1c48acc45c95fdbed9c47ac71c763ee53ab`  
		Last Modified: Tue, 17 Sep 2024 01:29:00 GMT  
		Size: 39.4 MB (39382970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e50e4827436e87a0777ab93c99b847eeda10ba41ba55dd724ba2cc6840a3bc`  
		Last Modified: Tue, 17 Sep 2024 01:29:24 GMT  
		Size: 166.6 MB (166567609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0749e42ed9e7d82deaeb34063735028d06e415fc5df5237ef15d068881a894f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271159362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf2d372bfa87e12926c336e3d7055d25082fe97548afc259ed97d70ee13f655`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3363e80d9b6d155f0ae139ce77aa32fd94df6eb46f50a3bec738d1033d8f32`  
		Last Modified: Tue, 17 Sep 2024 00:52:23 GMT  
		Size: 43.8 MB (43764044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc376bcd3849d1f0ea14fd75ec0bbed1615ddcf264fdaab646559938b61f729`  
		Last Modified: Tue, 17 Sep 2024 00:53:00 GMT  
		Size: 183.6 MB (183619620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c57d75bf05d4bab2e022d3e842430b445f90f49cc8ad6d8ef99c4c4339573266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274998466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40352b6e725bf98efdedaad84fcb7d82ed3d7afc5cf49388dc1301e69423b17a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:09:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8da1cbeb5ba78f9eb56920d49a58264a0e7f14bbbb546d6b818c307ca003982`  
		Last Modified: Tue, 17 Sep 2024 02:32:23 GMT  
		Size: 42.3 MB (42310711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d554bc49741eead5a08fa892cae07d2c98d5af01d2a3c5c8bc0b29b54abce41`  
		Last Modified: Tue, 17 Sep 2024 02:36:14 GMT  
		Size: 197.9 MB (197877479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:696292af1d26c3e8c085afefb22b79f16f3bbc7d8e9d65403f6bf33da393e0aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223812994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c7a372866a47e4d435a688a1067619591e80eee4a416b559330b48c878f69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:21:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200351c809009210c9ff3d95069658520c0808d693cf45463f14174972dffc8`  
		Last Modified: Tue, 17 Sep 2024 01:28:32 GMT  
		Size: 39.4 MB (39402519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdec65aff96ff434bc4106f0c66ab384f539df6dbafc567f21e7230089561faf`  
		Last Modified: Tue, 17 Sep 2024 01:28:56 GMT  
		Size: 148.8 MB (148767675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:ae4af6f3df25c1b472522b9e13b5f35ee4f65096876eb5fb508efcdad48f366b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e9e575bbf5fbd08b92fddfefa92a1f03825ef05ad773b4487eee6acfed264837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36638538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f765ea36fa4c46759dd690bb21cb8e45f32e1aa331cf9ad0da8b14816aa41ea3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad27316a38d3124ad8c0ef153c2a1fd356e6101cd2de78b49c0a1517f8e5f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a608399f965e1ef663c83205965174b05b375eba24e149c27e9cab4aeb91d`

```dockerfile
```

-	Layers:
	-	`sha256:1abede6965aa4c2f6dc7a23f51f9c10eab34e628cee2f9817cc259b2558d4d18`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 3.1 MB (3052568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1388bf3300d1894b794c3a79d61de4d5106bdcc7c16afd59021479c3346dc8a5`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a386ceaced73908c3b2ec5209db77b79b89054708ed73a630f05692cb32988eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34526233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5055a79c33ff49f2b7a9ea7bb980a1773c71b1d1ebc3e1fc9ec5daca7291b0d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:af723939f6a825e45913abe8955cab448bdfd8936a39c16e659f91fcd144e3a4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35430577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e6b3dc27b4071b35d0cccbe9d23dcb58c89ed7a6c74c5e178bd33234868d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fed7336e23d888337e23d27695e23b4629e6acc4864524291cbe911bb70bbb1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f50214c19651adb2c75be6a4d53624f0afa8be5e3011001a1930327b1e7e125`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:88ac494669975d9a648dc4f0217bf60e63aece135e9702b453b4d55b2296560e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be795c3e0e66e0ce4e2ee4d9b69c50ee968f836b15e16315c18f2b22c613d30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c578d3cc73855731ab4024c9120b974dc71bed918cb787254c69a305c21f0509
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35642800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da860bf0b99a8d35b13a4d49f791813c8d6aa4335cc2c25235b0ccb01de1cdec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:d9534b688fb61c18964528c9d3c18d2934b61499dfd9416d2ea05e8142899841
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17942397e5fced3f8b300ac7c7eb615dff08e3bf4b25ff7d4fdf0e50dc0e3637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76107486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ee0b5a3fd03948f634e632da31c66362c3663e3c5dd9e1e0c262c2266ed67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9649a6c09e0ee6b937917264d660cd3c815e5ee060c6bc8b89795f658ce584`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 39.5 MB (39468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:754d2bec28ffc00a26e2f7a1354ed7ae0d3775ed7f8e8ef4d4d940cf534818f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aef2e9a39d9f88806281cb44ebdae0758f7e0875bb44eec230ab7b038d1f21`

```dockerfile
```

-	Layers:
	-	`sha256:3746959abc49b330e29be49c40d27e7319253b12cd58a2f8585e96ca7d34fa7c`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 5.6 MB (5609043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77b1e734b0869190432a877573774367e039f62d93c379d4dffcf3156b081a7`  
		Last Modified: Sat, 19 Oct 2024 02:52:48 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ca89d3c84aac26f46e6bb0cdeaab9f13a9e6ef1232c9f88d738920468cee04c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3865fc6395b60b13dcf7604154e8af62468ec80630d7e29c3d8fa721f79324`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f084e39677777a3c9198d380890db30c595eeb224db5b12fee6f43e975e333e5`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 42.2 MB (42247087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:34b279fc4700c4c672e2f22e3280bae0cb0c280f525b541c37ca65d60825ee44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74813547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704307d21ad72ec302a4cc79016a0bf4a76c059c059bed698eb499cb6235066`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd83996b821ee5c0621feda52f2e1c48acc45c95fdbed9c47ac71c763ee53ab`  
		Last Modified: Tue, 17 Sep 2024 01:29:00 GMT  
		Size: 39.4 MB (39382970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1b8326726907980331fce56e29898f8fa15de30f322f5a2acd9f53783f8a9988
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87539742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee69e7ca45d862356910e271c2350fdd3b4e2c808aa97078e0189a2c53a3fed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3363e80d9b6d155f0ae139ce77aa32fd94df6eb46f50a3bec738d1033d8f32`  
		Last Modified: Tue, 17 Sep 2024 00:52:23 GMT  
		Size: 43.8 MB (43764044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:543266395b2597cfe93dfa4c7296684c535b15b50cb1ac4571918f69ee613316
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77120987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2661a6202957a6278bc4f96ae15f34541d0e2a163f56b6d81d87b8831f4f07b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8da1cbeb5ba78f9eb56920d49a58264a0e7f14bbbb546d6b818c307ca003982`  
		Last Modified: Tue, 17 Sep 2024 02:32:23 GMT  
		Size: 42.3 MB (42310711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee2acc822f0c058c87d4ef405f40716f7a0c2f268e4f43d66b4f709e2358f9ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75045319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c98d55db1472725ecfd27f682daeb79ae243193ac474e45aa974d502e56786`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200351c809009210c9ff3d95069658520c0808d693cf45463f14174972dffc8`  
		Last Modified: Tue, 17 Sep 2024 01:28:32 GMT  
		Size: 39.4 MB (39402519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:34bc65ada587328fa2d981afe497617a5502afcd64358e3f24f5b58c77831e52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:66b399a0f86523f2395926abdfe951911afa50511cedc5d1a24f4fbea665e27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349266350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a847434443a8427f04e1557140428137a084fa9fb1dc789dd063478bf276fc79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1c7cfc347f5c86fc2678b58f6a8fb6c6003471405760532fc3240b9eb1b343`  
		Last Modified: Sat, 19 Oct 2024 02:53:19 GMT  
		Size: 211.3 MB (211270246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b84245017497eea4a96ce15840ff736602594d0e8caacf84ddcf1e6e75c89e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15508225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede7bdb92b398bd42c66bb41b29390d617a1b587e4801e9534c3420cf2d7aa33`

```dockerfile
```

-	Layers:
	-	`sha256:f3cba8bcc452cefedc461cca3685c5b6c37d514908d587d0e37481bc48ba50a0`  
		Last Modified: Sat, 19 Oct 2024 02:53:14 GMT  
		Size: 15.5 MB (15497685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece5456f1764c52cad682d0bc55c96cd82870bcf728a20da9c6dc65d508322b2`  
		Last Modified: Sat, 19 Oct 2024 02:53:13 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:25b17e8aa430f3e5bcb80eb5bf8d037ec95ddd242aea4ec0f74d610061282790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316629383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c5935b372870d7f04491d61f1993c99057b2ad1f98130fcab6452319533806`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:24:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:27:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c114860f8d70d4b0766d6eb509df94ed04b6a417e0ad9060f9a9d43e84064ae`  
		Last Modified: Thu, 17 Oct 2024 01:35:20 GMT  
		Size: 22.7 MB (22729227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c96b0eadfdfa6388c6308313b6ff3f016dfa452d0521acc1979654342d6abf`  
		Last Modified: Thu, 17 Oct 2024 01:35:42 GMT  
		Size: 62.0 MB (61999097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614584ff99d2c7b6591b578a66d10c94c81692c6a8c18b8a42671dc8fc7ad543`  
		Last Modified: Thu, 17 Oct 2024 01:36:25 GMT  
		Size: 184.6 MB (184570538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9220348c2292a5c7836e61e5dcaced1895274a5fc67da8d9873bd3140bf89134
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301972566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c7123986773b7fb351e2663141d16472280b9d4938cb89a8abefaa75cf0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d133c6fb31d3251e78f2c641f7d145d5f5b2ab13265639c8eb02354c0ffe35d`  
		Last Modified: Thu, 17 Oct 2024 03:37:52 GMT  
		Size: 175.2 MB (175227696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f66285729903294ee7e6397f09e6e57a1c7b845f491a17236f379b66fca60bc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340197975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeedd65d53caa810d0605b471c43849f76115ad352b7c098195c75e586fe06e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac41aaa9ccd9258f7c6b8f1562698acdae4548533ae639ff6653baa08033c71c`  
		Last Modified: Thu, 17 Oct 2024 04:36:51 GMT  
		Size: 202.7 MB (202669297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1c21375b08b4d0f25f20769d2547d2948982c8e2744ea336a64d389f2a87c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351867123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c98997c4e35d7cb7e3a88082701de0bd4f2daa9ee328f9cdbb34e20318504e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ebe45cbbff83005bfa62fa86d2064e8ccedae2cd7617a6d60696a420bd1bb`  
		Last Modified: Sat, 19 Oct 2024 02:53:15 GMT  
		Size: 210.2 MB (210186933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34adb642fac5f95817489d8165bf13bf55504c9704e969f5d3c78af5f052ed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a43af330dd7cc88d66c01cbd66a2333691dd02459d83800710b92e3e526ad`

```dockerfile
```

-	Layers:
	-	`sha256:7c909413102d12d54aa31d8cc5582cbe0762e5a40d49bbf051d2cfced9df8ae8`  
		Last Modified: Sat, 19 Oct 2024 02:53:11 GMT  
		Size: 15.5 MB (15476264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854336bbcc82191d23e44fbe1fb86eed9659b15b27f56cc7343ed66df224eff6`  
		Last Modified: Sat, 19 Oct 2024 02:53:10 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eedf47cd0217818cf4687c2bed18ecec128b16af82475584ebbeabff390e5f70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326348772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71650f7afcc0ee2ce3640621c54788a7d5851b59ef46e25c54141eb87a7ea58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:08:45 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Thu, 17 Oct 2024 01:08:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:48:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb4cb3753c5260533ae9297767f8b73bc0cd6f1dc878635a173148920d80368`  
		Last Modified: Thu, 17 Oct 2024 02:08:35 GMT  
		Size: 23.6 MB (23647379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e244535d91d08a7c42eab7cd45ea82c43428356bc75a90c8d486507e9888f0a`  
		Last Modified: Thu, 17 Oct 2024 02:09:28 GMT  
		Size: 63.3 MB (63297195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8f8a184e3174b4b3b76091c95baf89a636e164f9c732b010464037c162209`  
		Last Modified: Thu, 17 Oct 2024 02:11:35 GMT  
		Size: 189.8 MB (189842579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bafc61e1014935dde758d5d8c2f2cf3614486ab7024e8c1dd51e5eca3d9a1e60
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363396234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa68f72feb2ed3326c5b70c46fc86e32731822125a51dc10faaca60d96896e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:44:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d27751f2c723de9cfb2cbb2775f1c16c1f3653cdff74eae652ff9cc1633eda6`  
		Last Modified: Thu, 17 Oct 2024 01:52:21 GMT  
		Size: 214.3 MB (214300830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22357b5316cabb794fe07c11c4af17599270f951b8c9e21430952eb1f022716b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318793259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6716f9f26b5e12b4faf3947ea48f9b157956dc7cab733983b5e315635eac4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:42:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77632955ee6981fa7ca39f104872912fb4579734ee466c2eb2d442ca4c8a29cd`  
		Last Modified: Thu, 17 Oct 2024 03:49:21 GMT  
		Size: 183.3 MB (183307845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:e8a9695d1d33b833cb4b09240e2c82a974ac41e6e8a82453fe77fb00730a5438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2643b4f2b82e8660bc0fdb8b391a60eb11a35461482d70d589caec7699207ac7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281087023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95e358ddbec82a0acfa688fa0dab9ba24e70fd73892cdc8d3f17de957f69018`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:07:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:802008e7f7617aa11266de164e757a6c8d7bb57ed4c972cf7e9f519dd0a21708`  
		Last Modified: Fri, 11 Oct 2024 09:51:09 GMT  
		Size: 30.6 MB (30610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce655b4c36ffd598797e82b3de3b049b04e79dbe27a847746f19cff42809f`  
		Last Modified: Wed, 16 Oct 2024 02:08:56 GMT  
		Size: 13.6 MB (13617894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36bf0492511d9dffc772e3618c5b2bce4c68245d25303931ad3fb85f3a6664c`  
		Last Modified: Wed, 16 Oct 2024 02:09:12 GMT  
		Size: 45.5 MB (45477297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63b34e199646383ec856bcaaa87784a4a45bce0e45b0284a7ca6d9707cef5e3`  
		Last Modified: Wed, 16 Oct 2024 02:09:43 GMT  
		Size: 191.4 MB (191380913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:713612cf63766ebb404e1a52a360fad7d397e21e3088d7b2a28ae74ba98da8ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241159665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da6778e238916247540e12782a664d323959de709bc94752f0d93d82ab3f4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:26:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c34db50907d073cf30d59433a5b4eae93a48fa52ede9ea3b913d0b753160ad`  
		Last Modified: Wed, 16 Oct 2024 01:28:49 GMT  
		Size: 49.0 MB (49028067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9916eb9191a57d65bee2b4f5544d08a9333e77bd43d114bd7be0aef2f69d116a`  
		Last Modified: Wed, 16 Oct 2024 01:29:17 GMT  
		Size: 151.6 MB (151621597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd255d45021e1cb092029d8623aef734733eddc32df3d3ba726eee7b49b2c8b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272159540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9859a96b988c661253c86126913ff807df44d99d7a5bf6511149514acd3b4fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b150961a20a0a06d6f810da85fa0f3e06e5942258e8d0f0ba7003e35f0fd02c5`  
		Last Modified: Wed, 16 Oct 2024 01:30:50 GMT  
		Size: 45.4 MB (45437380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419b5ae2bff4a1f7d611cfb936194e3d1699d162f16e2eb77ad3ddb981955824`  
		Last Modified: Wed, 16 Oct 2024 01:31:16 GMT  
		Size: 183.3 MB (183316090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c35798f4fce8f05eb7b8b497b5bdd619911732b04c7910a7f79d682524226324
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (300035872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da444111c347f5ad8acac23cbf5b3c98da7376b9b2b2c94fdf24925267cdcff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:57:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 02:00:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0b2b4d7e49ecab28973a1234e450767a55095ee5c46d9f6c5fda68a69d661f`  
		Last Modified: Wed, 16 Oct 2024 02:02:26 GMT  
		Size: 50.6 MB (50640454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1d065d6fd2e30971f802b752296ba5fc11ede3de6293dd006fb41bc2033fc4`  
		Last Modified: Wed, 16 Oct 2024 02:03:03 GMT  
		Size: 197.9 MB (197892979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:47a9ab4d22aa3bcc739d4282379cb397b0327dbe6055fbd0eb0792f52a9cb683
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331525136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90912f0b1b0b7da842a3f82ab73ff906bb40e95a7c269f9a78de04cd34b9790`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:21:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f7e1c8a9b4315a0ed15211421dba0019460f8a9083a212fa9fc751b5b81ec`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 53.9 MB (53939762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb2cc5f475f6ffd6d2efcc2334f54424e21e8704d54421d728b5bda8bbbfa23`  
		Last Modified: Wed, 16 Oct 2024 03:29:15 GMT  
		Size: 231.3 MB (231317673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d7470c586a514500739e65974b9a741e69ffafb92a3b28407b0a040b39042ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263237303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69d9df99fc5e4ab57f4fae574f5a15dfcf4fa579f47eaf33681abb2aa603e3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fe4420f7cc31e2e71a763e82cb5891ae4caf5f1904fbbe4513bb4cd423b516`  
		Last Modified: Wed, 16 Oct 2024 01:17:57 GMT  
		Size: 47.1 MB (47062541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971618b64005ee48e116c11ae3ec0d5fa0d62337b5252397597a384957f30154`  
		Last Modified: Wed, 16 Oct 2024 01:18:28 GMT  
		Size: 170.5 MB (170537217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:f2d116246e8e7845086d6c22e86a1b515bb9a42ef4e5fc34c6086c1c26f3834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:69a53f84746bd2372529e6294f001436f888e30870daf61281a69619b86057ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43367069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303bd2f189e17d8fbd2e62d67886dec77343f278c3c75cd273d299207c7b73a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0dff7df9d3a560fec4504795a8a76af7930b39ab2547e3ad5d56ae1246b7712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33382ecb57f630cddd0121e9581f247c374c0a13913cca08bc2ae9cf658ed9c8`

```dockerfile
```

-	Layers:
	-	`sha256:aae0f7d55899e7c0940b7b61d432d39e39e21cf565b7228a0eeba668dd220f63`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 2.5 MB (2460121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e5735a561089783c9f33d6a1c22c03d2914ddba32944dc3804408ca6f390f8`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9995076e2ae03b6f7a5b629e92c450245417849689d7cd49027eb652b67234d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40510001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e11aa0f6de1216a0ae7b41f4f9465a1d8750da4e073acd2ae2f62973d2d8d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6f5b67c405039f1cfd90f84c4af33431b848b7e5eedaf251a4499023bdeba4c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43406070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfb8b039c3cea45d5ea12f16c94c0a2926c998ec0c929368e66dfd9e0e5541a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:379ceb731b62e12334fb047ca39097cec13a0b1632dd6c1bb95ea02baa9cbc63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51502439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951036260e8de92532ed3f7de0131a75dd2509aacab1161fc3cd7588986f0967`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3f506d51d6119ce3ce143329a218e38cc9289d8771091be1858a95c8e8514694
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46267701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea764b821c3369419fd9f1e8af98d221f2c979549bd85a03112564680665fdd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60af0affbaabfa59a92d426e00c53b7736298ab01f0c19661d1f95ad89db8a83
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45637545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e84832735dbbb9016a6bcd6bfb982637edc98cfd427f79d3fbfc94d5f71607`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:63dceb420dd1f35491eddb52c7aec1eaf6335e6bddc552aeee2eae211b3a7434
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8eab756f646b732a7dc889ae8b8edc6b7910c99a726dbfef4d55b84e097001c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88704738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc073b53d6ac3a55820ef7f37b3b01f8eab8d306c872ee6dd8cc8c3273bfb59a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2a09e9dc33036b61d80e379ffd5129d921c9af74fa05aac5fca717149fb56f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cebdd3000d8052a20f7ae88451c5cd8ccf95751b8cbbd1374dd8c343905396`

```dockerfile
```

-	Layers:
	-	`sha256:fb57808df518ee10975192da49d52cf1942c3a864b2a5633e74b8359dc522a03`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 5.1 MB (5076079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3045d24ebd20c1b16edafcb0f97642f4592eece82164dc9a906540d80177a4e`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a06d232a7e643f4daa3c698adada949fc17a0fd20f47b1debeb8504404577af0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89538068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a39be091951674a4cbb94634063aca7bf984a766831b1fe21c8ad39c1b6b27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c34db50907d073cf30d59433a5b4eae93a48fa52ede9ea3b913d0b753160ad`  
		Last Modified: Wed, 16 Oct 2024 01:28:49 GMT  
		Size: 49.0 MB (49028067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6936451af0ed0a91229fc21e2c2c429ed854077e5b6360fae94e8089dea36fbd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88843450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9ddea909fdbb18cd569092953e76b7a61efb90a9c6aed2db4c7e8ff835c81f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b150961a20a0a06d6f810da85fa0f3e06e5942258e8d0f0ba7003e35f0fd02c5`  
		Last Modified: Wed, 16 Oct 2024 01:30:50 GMT  
		Size: 45.4 MB (45437380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3038197fed25007eda3256f4b2a57b81d6e897193c650a3809533a5b713f6b9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102142893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f197312de325f9248d1193327d98608528ff57eebaa5475f93ffa70840537d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:57:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0b2b4d7e49ecab28973a1234e450767a55095ee5c46d9f6c5fda68a69d661f`  
		Last Modified: Wed, 16 Oct 2024 02:02:26 GMT  
		Size: 50.6 MB (50640454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58bfee3b37ade385bd6d4489243657d8d601d1e5acac4ba402f472cd02c7236e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100207463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed1ee396bd81d04e194c94f7be101f93dfa563fd21a6f0ff9b34aecfc8fd3d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f7e1c8a9b4315a0ed15211421dba0019460f8a9083a212fa9fc751b5b81ec`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 53.9 MB (53939762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:670d048ac22ccac1fed74cfb5714c7e94b6258c1efc866c41da1395b3a26b83a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92700086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66fe8c0be99d7249a1f123ad94ec058fcd4204c0c34167e176e2edebcbe287a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fe4420f7cc31e2e71a763e82cb5891ae4caf5f1904fbbe4513bb4cd423b516`  
		Last Modified: Wed, 16 Oct 2024 01:17:57 GMT  
		Size: 47.1 MB (47062541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:25c99da22419b70f9ac9397db1c87a573939c884360ce11eb766635f2931e903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6fb1b551beeb414d904634652bd28a156fcd99b81d48f1f563a2137b4d66435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322637930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d2e2ff5e69fdb04ea12f2792b8e5a4c1d0e5540d7ca923b1c3e0ca980d5e76`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dcdbbe5c1d62201fcee2dd2ca8ca09ec165f840a8a7a9fe05e7875b49b468`  
		Last Modified: Sat, 19 Oct 2024 02:53:29 GMT  
		Size: 197.1 MB (197069718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec03d4652a03e963b3c0125d3d60275c0c1cf950c98fa03f69b85617d1f444df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5b52311e9c598f6e67ccbde69cff414afed1a62f0a580eb6ef7ac7581e44f`

```dockerfile
```

-	Layers:
	-	`sha256:a58854d3cfaddb475139d152911a8e319295947cb9e4d880b71f2359f6786973`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 15.1 MB (15097594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f19d6af261d1e6bfe9f8f4e9a6292e45a246ad6e9bac661e73d0706db7a455`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9620487d9a3dd979140faf498adb7797ad3ce6d3486906e1dca7293fded20bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283267265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a870836d352c022dc0b725162c10529ea61d91c79ce2aac4aa301362ddfd66d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:34 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Thu, 17 Oct 2024 03:03:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:30:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39efe447d42646f3185dd530992915f4ee5284d42835f09c0a8c04ba06ba134`  
		Last Modified: Thu, 17 Oct 2024 03:38:18 GMT  
		Size: 50.6 MB (50618781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102cf143efb57e0d7377d35f3f52584b742bbf4091d513fd71597ca2845e21d0`  
		Last Modified: Thu, 17 Oct 2024 03:38:49 GMT  
		Size: 167.5 MB (167526825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b25e42bc10765a3222a439524daa5942d5c6b6a2d5557d50a6bdc5d040fa7ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314298001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46fcaf6dce0b6e0a315dce9f0a57f58f729e94e5a348efcec8351fe4218db5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:32:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0134077e35514883cdc89f46185c7eae106a74a0895bfbc1494fdde44310f977`  
		Last Modified: Thu, 17 Oct 2024 04:37:14 GMT  
		Size: 54.8 MB (54834752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1f1670189accf143f4aa947a240b3dd83abfe6af77ebe02a7651953b171b5d`  
		Last Modified: Thu, 17 Oct 2024 04:37:38 GMT  
		Size: 190.0 MB (189978129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:35da12d82b0122d42f5bdfa6360d302249deaadd87cc7ceaf51e14bf64555596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328350614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690fe329d3a092d7f93dd6078a5993d7c2f79b49cf0b4b6df8f80a6bc3375ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668ade1ad6ecf9ecde05517f60eb0af8fbad048955aa9fa5125dfe9e07f656d7`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 200.0 MB (199977836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fde5e7bd54ba76c9a5a91073eed2d011f6a68186ba771799e49d857fd89f414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15096145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5034587ff849067841fd6614cbaa3735db9acb76a0bc5a91bb14193214ace858`

```dockerfile
```

-	Layers:
	-	`sha256:82c5aa200df2a044ae1a349683976749352850413f001243061e9bcaf2488761`  
		Last Modified: Sat, 19 Oct 2024 02:53:33 GMT  
		Size: 15.1 MB (15085935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2857c1dbbf9bffc7cb36818e082a24834e7d6117249c84160210df820841708`  
		Last Modified: Sat, 19 Oct 2024 02:53:32 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:498bf9195cd16d43171335249ed823b9c8f5cc4d4dc87423387e6ed7533febc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d3916e45c1b1919b65c5fcf324491e8d1b8c2380f96507ace92275a5723d318b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70842919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e9b58743a7381f5f53c8c6ed89dbf396fe86249f72b153da31e552319b0b28`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad90543a0cace80e4521c0c75ae897cd3bbb6852853f400beb3fed043465ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5490fdfd04a997fdf4839988fcca7e947362a72ef349b49747e39debf5a1e865`

```dockerfile
```

-	Layers:
	-	`sha256:c5efb53970567eaac415d819fedd7e79142f37beb0bb95d76686bed69e20bb95`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 4.5 MB (4492144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3f4bf535ae6901543c9781878d8215d7afa74196a9bdf1873b7512f6d18446`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce982925f7cb662229a416b8ad803c7a5ed65c69917a6fe3e519ac657ba2ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65119280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcde28c3186dce242f6150e5ebe0bb3c3a8f9fe6a7287a3cf88c06f85631668`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9811aa580423a2e552be714c14e210eacb5d77955466d3ca3381faccb47f5832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75437541a1b4d8578a4168a6c973fc1938cef6004aed71846971abe640ce1adb`

```dockerfile
```

-	Layers:
	-	`sha256:ee4e340b3a5aa96d9edd30cd59e56c6a84097292c754303d197005b000003d1e`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 4.5 MB (4493778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc400e038d817658fe4f5c569d165dfce2496c578f62facd784e7288a97c447b`  
		Last Modified: Sat, 19 Oct 2024 00:56:45 GMT  
		Size: 6.7 KB (6656 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ab97857735b9bb4ca0316c84af8cb47f468d79fbf7d69a7602a4a057be20d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69482684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5ace0446f1a3d88fd6d7eb94cc84129b0dc299b80045b5e26f87a3ce7b20b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c985a2a0b84bb74f11845a54a2cf9b51f2f79c056c15b4bd2e136676c9383502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0c728f5437aa596659b21909e26c3dc3ad3d1d64adb107edcf6d718397fc8`

```dockerfile
```

-	Layers:
	-	`sha256:6cfb03deb7abd3faa75a7f964fa9369e9644a2b85204515db2a447c862c83f36`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 4.5 MB (4491756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488572740765c205abccf12b5ac1f0f9f380f18333e681fb042fc29b61ce5b9a`  
		Last Modified: Sat, 19 Oct 2024 01:11:08 GMT  
		Size: 6.7 KB (6676 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fb117244a074d030af0177d95dfa02ae40a9dd404705ec11a8714d6de03266f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb4250e207301019763c2a652f7c0d6950982158eeea54d69191d031358628`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08b4591968723d4d0fdf75817cc1f2f6fbca81c6a5e3e32ce8551977603e00fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb7873e29a676043e203a9f966a180fa83afab781074edefcf1d757c1efeb5c`

```dockerfile
```

-	Layers:
	-	`sha256:7ceec0d5e1bcd10de39b1fab285826c265e8ae4449bc373c17ae99bffd7da1e5`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 4.5 MB (4488583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8a2025755a1ab2cc4010aed335945299dde3703a19af55f8126ca9ac074cd7`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 6.6 KB (6583 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:38e8bf2ca32551067ee504f09d30725145bae9290a848dbda17babae267c38f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f0485e10500024df9431d8de6763bdc6da543ca6ab1e5ab2057b421dcb7edaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125568212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51724573712708db097ecd36d4692d52fe503b6a5e588fa6d2f92d57448b75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86518255b538a594e8e2238131f87aa1d67981e1263e4c18db09e788a30e0211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8114d198645a070bb880f41004b7e18eb9b532cd04d152554c2198c33bedad58`

```dockerfile
```

-	Layers:
	-	`sha256:8119449007c140ad3218cd87f4c75621c38e919438ce0347d51fa76951bc74ed`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.7 MB (7720100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a0a9c5343eacf41f82ce1d610c6b28aacd5cce7e62805b6bfc9ab1dbb20dac`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6fb8dcf1b939160b597f606a99837dbd9e6b08a36e6cabb2d256645c9b1312f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115740440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9d27cbf62dbe2318150927b91f2d8046815c0477c72bfd27779197a5afd926`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:34 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Thu, 17 Oct 2024 03:03:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39efe447d42646f3185dd530992915f4ee5284d42835f09c0a8c04ba06ba134`  
		Last Modified: Thu, 17 Oct 2024 03:38:18 GMT  
		Size: 50.6 MB (50618781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d9929a8653d0de4548ba7e83976b23e404a4244ea7980582ff44948698faeb44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124319872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe2df2355dc642f0983dd1e359d38f267c0ad9c839b6448cbff86fc0f644854`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0134077e35514883cdc89f46185c7eae106a74a0895bfbc1494fdde44310f977`  
		Last Modified: Thu, 17 Oct 2024 04:37:14 GMT  
		Size: 54.8 MB (54834752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9890d2391771767d200b4cbf59d19803dc7325c67a668de520340c3585253ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128372778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfabefc5f8a6f86a4c1d0830952a6542af51cac814b2efcfecc61b068b812e6e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97f2982c47b11589dc67c23f4654b6f5ade92e8c507c09443e2500ca71371690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8bc9ab9f9ff20301bfe16816c4cefce0e403721ff906a1f90392f09c200edc`

```dockerfile
```

-	Layers:
	-	`sha256:fe45d08f635e7da0980c4e3a17abd1d69bd81cad7123343b7c0a8bedfdacd121`  
		Last Modified: Sat, 19 Oct 2024 02:06:28 GMT  
		Size: 7.7 MB (7715588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc67396d6c2b39edc8f2c0e27392aabce73e953884562fb7a86e6187cfa784d`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:5590362c96c705460f483f556a2d0837fded373fa3569a60c07d684a148b436f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:688a8d17441926d680c64d52a17ba261b73b29bd6955bedb3ae74a10c8716154
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287552644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6447aa6b1e22be7b61d8470d3398317b8705fc464924d411b8156ecd6057f40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:15 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:18 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Wed, 09 Oct 2024 15:42:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:45:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:48:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43ed7ac192d3f50e551118286d2a59c5cdf9ae247515319b137995d2d91c1857`  
		Last Modified: Thu, 10 Oct 2024 06:10:56 GMT  
		Size: 31.5 MB (31497006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebe8581de16e2d108a8b8b443bb95f82e5cad32c8f55539cb51fdde9b3436ca`  
		Last Modified: Fri, 11 Oct 2024 23:49:36 GMT  
		Size: 15.4 MB (15351852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd7d65218420548fcafac6b160a3d5aa59ecc023e7dc66b84b5bc87977eed4`  
		Last Modified: Fri, 11 Oct 2024 23:49:52 GMT  
		Size: 46.6 MB (46552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00338c9ed1170da053bb792bbac38340426de9df9e9b33bc25b0145812151182`  
		Last Modified: Fri, 11 Oct 2024 23:50:24 GMT  
		Size: 194.2 MB (194151652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:183ff55827bdffbd19e81d560907a07cbd8380d60f74bc70a57265edbb659927
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249689229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2b05eb94afe2d9f97e104b90aaacc17449044623b553b406ccb96822857a12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:41:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:44:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504d197ab129fb5bf6269a181811d7443fd358b01cf3d0cdbfbf1f7e94a778f`  
		Last Modified: Sat, 12 Oct 2024 00:46:05 GMT  
		Size: 49.5 MB (49527237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2e428a54e779d37be7f87db612976720765d94283996921ad943a495bf729`  
		Last Modified: Sat, 12 Oct 2024 00:46:34 GMT  
		Size: 157.7 MB (157703878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2fd75582deee680615c3b70cbdd5ac956126d09379bcf537ff0d4b5b656de838
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281353475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9191d37723b6c0372f40a06bcccdf93aa4a45f0358e7123aaf6c93703c1c7de8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ffa9891ee7f3191d73f9178aa9a6cf0571e9f85014da289756abf79e90d4fe`  
		Last Modified: Sat, 12 Oct 2024 00:08:53 GMT  
		Size: 46.5 MB (46481307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1003351ad394f136be5f70383549702edeefff5c3ed4d81730a00e936a8fb10`  
		Last Modified: Sat, 12 Oct 2024 00:09:19 GMT  
		Size: 188.4 MB (188355990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b70c65c43d980c1b41ebe36a2126d8c70856f30cef5b7987202e836d76950d68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303024216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ca3def268ac1175bac2d3cf5c33c7a4c812c79d36658645315c82e562a9fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:46:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080368c5e29f148040c44902a5c8ab4b32ec2f0ad63b12f764de4230a80ef737`  
		Last Modified: Fri, 11 Oct 2024 23:48:29 GMT  
		Size: 51.8 MB (51822495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd100af345e4d68ed2ef702d8e378cce86158c1173a29884475e29a3e55a2`  
		Last Modified: Fri, 11 Oct 2024 23:49:06 GMT  
		Size: 197.8 MB (197784051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9e15f8c24d6c90d02fdca80fec7999e7fc16cae1d9b1c15b76919544ce7039b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71077a13e9477b604f394e11dda03dfdf6545214675a73d35f44970d51de4496`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:21:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7cdd9669889c44132ee8d3640a1da628cf56156b39012dbe64ca81599329f0`  
		Last Modified: Sat, 12 Oct 2024 08:29:10 GMT  
		Size: 54.7 MB (54677266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e6827872bc7b33fc8f425500eda0f9a7c630a6ff574ee369076eed769eddb`  
		Last Modified: Sat, 12 Oct 2024 08:34:30 GMT  
		Size: 276.3 MB (276314931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c2ff9fe0ccb48def463608838a0f7bd03444d5004277c2e12d56b7c456cee2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266544571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d8e737d4389dd93d0c17d005a20d2a5786fb05dd66bfb8348d501dd5bc223`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187f132b69cfccea48cca74390b7916df3cce52677c59ff2df716bc3e9c8e5`  
		Last Modified: Sat, 12 Oct 2024 00:19:33 GMT  
		Size: 47.9 MB (47893672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419866cbc9cd0dd6fbc3dd57960aca4d55d2f875b27b9ea37493d4712702131`  
		Last Modified: Sat, 12 Oct 2024 00:19:59 GMT  
		Size: 170.3 MB (170301344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:03f80bb571a97f04cf6f6ce70cc27455bea50491907b2b311b5df89ec5c89623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c8064ce954a2d9c90bd2e16fdd31c7c0b20e66720232e562b71c781f6c00bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45957871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7b838a1e6a2498c0f2b75d67c8db81136efdc82a162f30a7585633d1d465a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:734f143b619a054aeaf675404b5a8b6bf169fef11b9e111e8a691436743a0b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d2b611b8af5dbe471921a51a30ed516be558eeaf85c1466481a13d6640a4ae`

```dockerfile
```

-	Layers:
	-	`sha256:04d1691c1daa2c8f7f4ed5fbb5bcfaa1d228a7b3502a02d4d0c606c8e2a69420`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 2.5 MB (2458653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470d7dbf100349d28fe574b0fc0e6eb056c846f0a7430a28ea4919e451ed1b6b`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5cceb2f547cb52fc3342e32fef41d79dd9a16dd8b9eccb8cc68d586752442712
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42458114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67665e512286002cbd3225e6ac838a3288fd31c2555234586ba4330b5621f93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d026840c1f2c42096cdb088df4b14a7c9c852a36f2d035828d99c7b74ad528c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46516178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdcdec574fcb50d0bf5119678c2bc0dea93736af2dfe682c13957abdf5a1314`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:817662eada8897a66e5dc015628c6f86e2f389162ec27464b08111d35facb2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53417670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459d95a79091922cb35dccd5f8acb872291a6183b2b9d44b661fc36ec2f16826`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d077992b788a9af765b5bd9cc8dfbfdfa4148a8f57a536e79b1c900ff703e118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71e2496c145fd637f68a99d79840efa4114692affcd6e12fa47c4173263fa86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41a996db9213db8294e64f1a4ec828a25b048b6f37748fc974fae24e9ef2da57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48349555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571e0eacd2affb23496465cae630c9165b919bc6913371f3468b298362990bdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:592c7ff14c1fe47455b75265eef6936f6e9cb3d01bd5d9c0ca35ddbc9cda9338
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2e1a10606d94d1341f4291bfe145a175659c824965e8fd3865cf838d843ce4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92385945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113271dcab80bce9700ced13a5585c0c989e1b56647edc2486bdbf7e270ae92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e3606b1ecf3ff7025ba8e1ea5e42df37408b840635cb63b334f037e41989f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10503c61c856cf28d7a99d4c07c844f5c8055fc334e6a3789c4c5d7d52bcbf1`

```dockerfile
```

-	Layers:
	-	`sha256:78722da52930ac15ebf0a6bcfd0e1fe261a2746c127f81b162b628725a8bdabc`  
		Last Modified: Sat, 19 Oct 2024 02:52:38 GMT  
		Size: 5.1 MB (5090433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebf53812943cf5a8aa3587eeb1d7aa692dfc6b67872b34031c7959d49e6fbd2`  
		Last Modified: Sat, 19 Oct 2024 02:52:37 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69f9082b0142c4f42e3a112957fc83d72b89b38fbb234fe5659e746d0070d22c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91985351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc6a0da45d1b7f338d9fa6bf0714944d9d132fa54dc02d52594df947cd148f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:41:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504d197ab129fb5bf6269a181811d7443fd358b01cf3d0cdbfbf1f7e94a778f`  
		Last Modified: Sat, 12 Oct 2024 00:46:05 GMT  
		Size: 49.5 MB (49527237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f1688b9daecc9916d1dbf1d42c2f392b04e4f5ca3ca02f0c185d2261963d5869
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92997485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975a3888f98975958159d11d7cf9fcf5128735180169e3025a8dbf1936d27c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ffa9891ee7f3191d73f9178aa9a6cf0571e9f85014da289756abf79e90d4fe`  
		Last Modified: Sat, 12 Oct 2024 00:08:53 GMT  
		Size: 46.5 MB (46481307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:256a8a2aa9efc3d54e483d9a501f7ccdb8256fedb44a7c086a4846bd113d448a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105240165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e09478d0dfe4e1b3652a6ec2abb7601543219a4f653e5e42ede46c3d333292d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080368c5e29f148040c44902a5c8ab4b32ec2f0ad63b12f764de4230a80ef737`  
		Last Modified: Fri, 11 Oct 2024 23:48:29 GMT  
		Size: 51.8 MB (51822495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4566c169ddd534c5c54766bd8fc75edef81eba31cb3723701737b6fc083cad98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103366511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc918e600c0ca7bf21d0e52d3d5499216d4ec0595915343725567971eae959f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7cdd9669889c44132ee8d3640a1da628cf56156b39012dbe64ca81599329f0`  
		Last Modified: Sat, 12 Oct 2024 08:29:10 GMT  
		Size: 54.7 MB (54677266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f80cfa969a2981aebb45fafdb780f05cacc35e483062eba3972b6f3fb609dac9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96243227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1253efef7f03ca83d90ff492afca75b21d9e78c33fb3ca808d5943e2f82ad124`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187f132b69cfccea48cca74390b7916df3cce52677c59ff2df716bc3e9c8e5`  
		Last Modified: Sat, 12 Oct 2024 00:19:33 GMT  
		Size: 47.9 MB (47893672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:b7b31cf258096b5047be55aa30dad94e2ceb052c8c9e10c00d35725b10ec1bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e413426d5ceb4bc8b8485584a2334f982af09c40a294c8bf8bf6cdaeeee9875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137996104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6a3fd709dc98777b4ee2dac0d91e0d775c501c5f754c2721afda51367884fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:267daf9a035387db438e0e46fd4b93300a407ab8d2a8a08471e53480601da952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b34fb506a8ed23e1d427f349569ab9a18e6805d6de10ec99ed6a589dd583cc`

```dockerfile
```

-	Layers:
	-	`sha256:9f092bdcc560f05d219daef70c3dbe1cbf5beb875614df187738facf640574ae`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 7.8 MB (7764370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305b58c6aa4607a016c86411aaec62620a8480a7db911cf2b1b620bc59033585`  
		Last Modified: Sat, 19 Oct 2024 02:06:35 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:065821ca01f5b46e546b666ebc542baa9cadd26c83971d920f718a4d04641532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132056978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c329746ec886de5abee981e2a8dad46f0a25ec5606516321a628ea9cec7098a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d8e5c6c3bd120c07665df831c223d98cd86db7ad072c55a7433e227d49b3d`  
		Last Modified: Sat, 19 Oct 2024 02:55:37 GMT  
		Size: 62.0 MB (61996882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:993bf84285db8ca4c11425d3a303adbe960660b326c4fe16d6692cff7d2cab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7175b75d18a4b7c149ef131238c169805dae0110254e68d196b78cef76713d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8b6c17ef335d13a13ac672b98127369486d26b77a478f85e6dda04d194d55425`  
		Last Modified: Sat, 19 Oct 2024 02:55:36 GMT  
		Size: 7.8 MB (7765924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1348c0de7b4712e505c350d0c2142d3801c2c26e7c23faa55c9ce197ddd624d2`  
		Last Modified: Sat, 19 Oct 2024 02:55:35 GMT  
		Size: 7.7 KB (7734 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eccb934d63bac8c068380c9805d9b43b7f336b4c18f3240641a37e90dca17cf3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126744870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e0a5ed5211488d49c46201bd0003329cdeac002c563154869325cec7f1e5c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:24ff51eac951beb8cae6eb10c9a6316b92ba535f6ce57b697816a2f90d9e35fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d53a93f46b21e92bf85f52aefd48305b7987e7037693f374d44cb5e8ce0324`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:273c4a697c5f46c260ff0dc5ce28da78d7895442714cfe2ae670c62596c94c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141680190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f891597f8aa0b920eab180791c23ad8f9ffc9da20a5a68b66b0c2a936320a4a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7c27a970016230430108f980988c338d4d1137a98cd2b936476020943ea3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0fde0a53d069f07ff292e0334b827638c5a995a20f008cb02dca195cc9b24f`

```dockerfile
```

-	Layers:
	-	`sha256:e43a3a69d39b1261a900b087590ce28109339ec7b0fb043a670c0683b9cc0a50`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.8 MB (7760446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f61feb336f32426818cb28c5c4aae9e6aeea748ea4612b3d85b14136f23d82a`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c927f08d08e798a2932be4e20dad881e66c13708cd3fd12432a15db03914f304
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149095404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a195c447ca2ab15bd44723fc52ceba6b8484d8f8e8b74bf23786dbff4233d1a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:96caeb2a156ac3e5a114582e769104d80579b8f79601b73c7f453b4d8c947bc0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849e1c7b1cd0aa3c234e84d733980139487f92521f08631a58f63d02eb0e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:ed75310d8d7ed0c1dabd36cd5f4a5737ae852ed98e66def603616315f5e2a053
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e8a9bfddf607e07c59acad6b37e74a677f55b222264fff4086481b94f103248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368573290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608313d91b8bea5bfdaa7ae32f69dd84b19a7f528219c5ce18cd67955c1d10e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b881a2f1232350ec7e4aefdf5b77bf5210861f5960ef5f73da8c0d1966802d8`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 66.5 MB (66470763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86943b23dc3779237d892368b9a4c4fc090241e0fbaaada00b55b3055d2b3bc9`  
		Last Modified: Sat, 19 Oct 2024 02:53:08 GMT  
		Size: 228.3 MB (228271921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:406de61fc1deaa52ed02dda2f9335e5a3add1c139b419573cf5ce61aa0e5df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16623042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996b9f714262ed15f13040714584face383fd4a6b534fb51a47c89f857d30b03`

```dockerfile
```

-	Layers:
	-	`sha256:912cf800b3ff32bb074626dd668053449112fc6e0bda6515290514d72472b67f`  
		Last Modified: Sat, 19 Oct 2024 02:53:05 GMT  
		Size: 16.6 MB (16612866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccba7f94f8614c179b40098212350a18928af7d09ff485a475fb59ede87a07e`  
		Last Modified: Sat, 19 Oct 2024 02:53:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7e95232f4447716af74bd2907bedc9ab047b94e7bdb4cfc15cb1cf4492f4afb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336701350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e528f9913cf5ebdc3bfd2c5f1ae6fdca4debe882d4913b75fe13dd04460aedca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:41 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Thu, 17 Oct 2024 00:54:42 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:31:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b51e9513f401d905da66d3e959803693c1c78e3059a3fd54de6ad45f59179fa`  
		Last Modified: Thu, 17 Oct 2024 01:36:39 GMT  
		Size: 19.6 MB (19568932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52911f6537dc2fd850c0c63bf4aa3806ec9b40b64d351e34d00f5df0a1434fb6`  
		Last Modified: Thu, 17 Oct 2024 01:37:00 GMT  
		Size: 64.0 MB (63988084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb87602ce298bd118421d8a0f5456cad47ee48016fbe2aa008e1d427dbefcb0`  
		Last Modified: Thu, 17 Oct 2024 01:37:45 GMT  
		Size: 203.0 MB (202996746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:515c123d32c6aa7255a21ad574f394666fb16d3c565f24fa15b43dbcbb1182c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318104301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ee1ccf0154b3ec16d5f2b9555c44031d50cb756335a8bc0da6d1f3ad98246`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:34:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32490c623445d27e949376c8158021571cd8530fc358794dc7642b8bade85da`  
		Last Modified: Thu, 17 Oct 2024 03:39:18 GMT  
		Size: 61.5 MB (61463673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb9fde67196f11fd2b11fdc769e780383d757a9acd06f324a681d5a67d9f62`  
		Last Modified: Thu, 17 Oct 2024 03:39:55 GMT  
		Size: 190.1 MB (190052308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cae551d9dadb734a5c69ebeea30a565d17de285a771aef3133c80a56dd4098d6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (361995529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a63ceca4055cba5256307ce8eb7d05410d4ce178cdbbab2397ffa42a05af067`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd949d90425f27d9499ed62d5edc09c30effb2a25cacc5cdbcec475f72c714b`  
		Last Modified: Thu, 17 Oct 2024 04:37:48 GMT  
		Size: 20.2 MB (20199608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318bda2b7787f1d062cd74c8c3d67fb18e99d812d82717501702fb68c487f68`  
		Last Modified: Thu, 17 Oct 2024 04:38:02 GMT  
		Size: 66.6 MB (66556648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462feea23048f5379dbf36ebd591bca7bfe2e21ad6e6208a43952a5b97fe62e9`  
		Last Modified: Thu, 17 Oct 2024 04:38:30 GMT  
		Size: 221.6 MB (221609788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2586af5cbad80ef32c8987ed795e71f33f008118127d124c39f84dbed46b6b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.2 MB (373211235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c837d757dc27783ca87e9a16ccfd7676c7adbd00fed98d27616d3f6a128eb548`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29126a4a4aef17404bd71b479313e117a2f9ea628fcde52f725427fcf1c14fc`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 68.3 MB (68288819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4c0958eccba088614505337cf12f450adb63c3426aaabbf6f2e56318550eb2`  
		Last Modified: Sat, 19 Oct 2024 02:53:33 GMT  
		Size: 229.1 MB (229139287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72362d081c1bb8ae447bdca140fe2a9ff70d2754d3d9517a7dc02825a86b3101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16593424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb16d25ce0b74d32d0f00b676aa5ed31860af3eb2f992e62cff99c66b2f57b9`

```dockerfile
```

-	Layers:
	-	`sha256:3cc7643878c4a97b1d4c557d239ab4a5318d6bdb4f9efec20c5580b6184e9a7a`  
		Last Modified: Sat, 19 Oct 2024 02:53:28 GMT  
		Size: 16.6 MB (16583270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d99e8ed8a3e4a6aedcdab18d8a594b76680efaf4b6f36e723a7d3040ced62`  
		Last Modified: Sat, 19 Oct 2024 02:53:28 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e354256e268e95b4eb29793cf5442a60a571ebb0a9ea5333fa57af8d9e49758
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346019892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da56f0d01a64e286c3b8aed43478ed2441a3e37cdbe1e57f345af5e734ae1c96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:10:11 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Thu, 17 Oct 2024 01:10:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:59:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa54e7215b92f68792f1b978dc23df0d8344fea83727a4b5758d7a94f9713e`  
		Last Modified: Thu, 17 Oct 2024 02:11:58 GMT  
		Size: 20.9 MB (20886491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378bf47a6c5edfd4ad9a37322329896d2917b0b410c7f41449f823883f86102a`  
		Last Modified: Thu, 17 Oct 2024 02:12:49 GMT  
		Size: 65.3 MB (65299790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eee4379add186dfd518c292eb7926586afcdbd80524fb9da0627e98bee8333`  
		Last Modified: Thu, 17 Oct 2024 02:15:04 GMT  
		Size: 207.7 MB (207675712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:95f8dc6b9d534fb73f94dc2716623bf57a1930dd890d0db13e2ca8ca122dfd2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377765962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9bc7b533f4e3ec7e3a3429cf0c5995b27faf10b7fdb016559a4c7432dad9f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:47:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d006d9437ccf6825ce93da875340581aaede61b1bb556c25053444f5d60f2`  
		Last Modified: Thu, 17 Oct 2024 01:52:53 GMT  
		Size: 71.9 MB (71897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f60d866924718e5a834ee211294703f7ccaff0c50b423716b8bcbdbadf15ee`  
		Last Modified: Thu, 17 Oct 2024 01:53:31 GMT  
		Size: 226.7 MB (226746957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4219b43dc777d41d6f85d0c160677d87619eb13b75f3158cd5218abb7610f899
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.6 MB (449638935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cda9e1a8b19f0634dc0500a3dfb906412d655f75153f0909ff3ddaa1b30871`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:50:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cae9f617aba80ede947d89c8c1533181fbf6bbf33b4f52cd58a464daf4cadf`  
		Last Modified: Thu, 17 Oct 2024 01:55:15 GMT  
		Size: 65.8 MB (65759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4626b5f0a1b5e29bea40bdb350f939636cf2ba36351f5395f5d5c70852c7323`  
		Last Modified: Thu, 17 Oct 2024 02:00:59 GMT  
		Size: 312.3 MB (312291531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:375e8c731f4d01824b9332690c9bc0377345820ca71cc0b6daa0c1fc23f1d377
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343571564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3383977a925f9a62c1772339c9b74a27793502173fd36b4571b22d9a104dc16e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:44:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72407aa6b20ec8dd251f8d046dc6a90dc4762b5a40f3de1875d57e9707b2249`  
		Last Modified: Thu, 17 Oct 2024 03:49:29 GMT  
		Size: 21.6 MB (21639364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcc27b289c6aff3a3be7c20455e5a315df5f3865f769b958bcbc9fa8876cad`  
		Last Modified: Thu, 17 Oct 2024 03:49:43 GMT  
		Size: 67.6 MB (67570361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c8221625d4527cfc16993073388dd3031e9a3bebc65ac9e3d124ff4e8c28d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:12 GMT  
		Size: 201.5 MB (201509858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:09c665801f99b13aace18d0e534ca5fba8a95ccb9f491844b58d9a407a6681cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4969fc1482fe79df2f83454d450d1bb1a0bd65812c9965ae1acecbb37b03ccaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73830606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c95b99c5f7fcf27f8df865460d0bef48e4fe0499bbe6de82a9a812aabc372a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fda6398e5597471e4fe9a09bac438b822a76bfed6ac08368ef40b1e9ddea52e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e230e9497a2cbdf9af9438fc5a0ccb4b9846b644ac01b445504fbe028091fc11`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ea3fac8fffc480e851a74e960ed5d1e7f9b10adb718c0c389bb83bc052b6b`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 4.0 MB (4028672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c832042891b017cd09224285e67cb4bceed33f487315c2467b0339ebb7a651`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9fbe3208573220b4f9bc991ffbff5b241a40dc9207a1412852dc5e1dcfb848e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69716210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ee3aa87633d009b362e51572dc98a9cacd568e8c58399568da58bc7055fb22`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907cc8268897b865af11c617e0b6df9243de9b6a7c9d42c7a265f1e626be0e8`  
		Last Modified: Sat, 19 Oct 2024 00:55:48 GMT  
		Size: 19.6 MB (19568622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:704a4556dc0a7e5eada6cecd5287d4b85008c956b40b973ff74e5d10709940d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4038180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e52b0f8e26eb0efb788150f3213c247649ab0db37b9738559d888b15bcec526`

```dockerfile
```

-	Layers:
	-	`sha256:5c0bd3e2f79edb6da9625f1f9e47004acdf5cae6c326bd0785fe7cf585ac3400`  
		Last Modified: Sat, 19 Oct 2024 00:55:47 GMT  
		Size: 4.0 MB (4031537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4621ddefc20eb42391d2bdf32281c9b15abec3dc9d43bcbe5483b50017401b`  
		Last Modified: Sat, 19 Oct 2024 00:55:47 GMT  
		Size: 6.6 KB (6643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77c60cc265b95be3b104f0c8621b935379cee41049a173a232dc5ec430fd706c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66585055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80a481113f99d5a8cae3310407042e0a289b71236d59c1ed76c30c45339a239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa977a262dd181b45467b256087bca990abede89e133911524cdd68e44f417fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253aa76a9639b3e075a66b78d5e33f7d1c5029dd58b35967c686755f5c25c939`

```dockerfile
```

-	Layers:
	-	`sha256:88a067eab1dd02b5d086716eef3db36d32ebbb0f1c6015519cc361eb70246783`  
		Last Modified: Sat, 19 Oct 2024 00:57:31 GMT  
		Size: 4.0 MB (4030333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad857591c01e9afa58b31c832b0a59d253a0df59d62143775e95f07d9629f49a`  
		Last Modified: Sat, 19 Oct 2024 00:57:31 GMT  
		Size: 6.6 KB (6643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bc7f373af02269a239ab6419112615ca6690809a8d95bf7f43f1377dd2d6f476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73826100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08daf7da3e665395ab5a0d8cc1d5f760a074733172716e6fd4467fd79b96d66e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d70cfbc938d76d89a533bfb2fc5f1c306ff2beed08d6499de05ee55cdf580a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8716ecd1dfdc9cc5c59cec4b6019e1bfc0b6dc6055fc96fa508f5361182df192`

```dockerfile
```

-	Layers:
	-	`sha256:b591e9052a8f907be44d4656ffc3d018c55b54387630fff05f2d2fe1759dd869`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 4.0 MB (4029090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56316a4f7de5fa0299ba7bea33b33e2864d292edecf4a7905dd390fb3254c0de`  
		Last Modified: Sat, 19 Oct 2024 01:11:42 GMT  
		Size: 6.7 KB (6664 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01c063600551a346c195ff31d7934664465feb4d46a18371953fc30674669422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75783129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac719fac021c9c93427216a8e5a75372d2b1fc4bc2b30e006d6702885ef0db0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3940383fafe27fab3db6136b4524849d3a389a5ab50381c4b7077ed77cc81825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d1f1a9fde212e396e9203d732493e24f84b97ebd6e180174870254520a01f8`

```dockerfile
```

-	Layers:
	-	`sha256:e63b6a0dacd997549b8c0ebf2e2be3f0126dc1e541b72958354c090675d89fbb`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 4.0 MB (4025085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9bac0c42f3e32de80fbee483246d465199d456a4729a7ebfc077321f8618c9`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 6.6 KB (6571 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9ae3cee97b6b487b5d217ef86e5c40770bce1291c93921f4d8d77305d0db5352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73045522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4682cc57a81be3fff028130561f3c6eb09ea9654477dd9e698f799cadabf2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1882a78a33be52eda30fe2c75c6c6d9967f3fd85b20979f451f5c04dfeccde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 KB (6414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b736f996c2064246c296003a1cb4fcddbe3de476eb5b235d73b2a7809cee65`

```dockerfile
```

-	Layers:
	-	`sha256:06fd9bdf5e3ac76086b9540a8eefe0355daaa3d4beb72966f549ffa8f761c5b9`  
		Last Modified: Sat, 19 Oct 2024 00:58:27 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ccdc18d44f05da28c8219d90069f0d4eb9ee4316de834fbd642b3727c20d07a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79120885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c18cc132a9ec9d576c5f9b9c0490878f484b401f205c7de9ca5200fd8115402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f3cdfb0755564cd3c4456a7fa23e621d79e4f8f43bd8107c734f66d381334`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 21.9 MB (21944061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e717a437695f2a383aada0d5bb16603c9d9a4f27abf449da59f9f35a74fe4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e0b0e3c257dcd1365270fe00f03dbe0755fc39c63cf6a714f7595bea11985`

```dockerfile
```

-	Layers:
	-	`sha256:26a67519c427272540f33332e387d267a478d06ad577953e244f4ad7f64ab60c`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 4.0 MB (4032542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec11ed90a7198f124e1e507d4a9a67195e261591152ad27aff7a599b3377cb40`  
		Last Modified: Sat, 19 Oct 2024 00:57:48 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f2563b5986e1cbd6355ebaa519efbefd1ace7d95ec4dc05fb43d702a17656346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71586666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201578f73abedc744f4f2994cc04bf7653e03e6fc71c488b56b938fa6133682`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07e79f5072ea67bddca2130da2f9d315fd8222cd0609708a470e88dfa7353806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dcf549e44ce65cf2139914167a0d0f4b1a4302bf162cbab4d7642cccbbb69`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d1496ab905e4028f005f5a14166826563eecf34a3ccd9a6dd3ce4b9c1412c`  
		Last Modified: Sat, 19 Oct 2024 01:03:15 GMT  
		Size: 4.0 MB (4022143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d30c866b540503398d1018dd68b46d07f0f51532b55b00079c6208979ebb5f5`  
		Last Modified: Sat, 19 Oct 2024 01:03:14 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd2690414a6039d75b84c97bdaa113a12b72489d077a52b352aac6b045265d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74491620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290e9362d4f9db9760c8fc711ee0feb3425e972e82f673ff4917fe4a53e4cc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:372f3917080ed9eb9334f2c5f62c4d74cd82f0cb2530167d4024f63f3560fbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ad897ff0a89dc21885858a1e52dab7c9c8f5bb20638df51acb70d74756d2d9`

```dockerfile
```

-	Layers:
	-	`sha256:92a80cba733f641e49791d7770b207706dac2cc27956dcc0d0194f817f64b791`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 4.0 MB (4030243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8dcbcfacdd30256d369d06a17871979b477713f3b331489382dfe1f6da6133`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:98480a63588e0a05d8e2d525f5446b38da7aecc1af800401e54709066e389111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cefdabdf0dd3c0be2093674bd463a08706c6823b51ef5fc98e48ffc279c7b2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140301369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873827b625b63287b3afef0bf4cb27db9fad9dbd5c4d914199e2e3ad3886952d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b881a2f1232350ec7e4aefdf5b77bf5210861f5960ef5f73da8c0d1966802d8`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 66.5 MB (66470763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86827b548c07c2a481cae7d5aed48a4134e1de1c2408c43d0149d39d11eb5be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7597828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6b88eacd87f5f5f93b910719a867bece0a91123b33c13459cd08adfccd1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:511627375d7bd2a499e03c8cfffc6fba5567efd8d47aa35eb624b4dedfbeec23`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.6 MB (7590531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3af11e7fde68c3dcc1bcb722db1234981bee58c66281bb50a9ac93c213e05d`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1a0c5e363a8c8458928698c18a4a8e521685db479a3e4929571a9edf7be07e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133702859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecd7b81df49fc9583d1ed7d438d04c77a3510d7c84eff4854a7cbdb89fd0882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907cc8268897b865af11c617e0b6df9243de9b6a7c9d42c7a265f1e626be0e8`  
		Last Modified: Sat, 19 Oct 2024 00:55:48 GMT  
		Size: 19.6 MB (19568622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f2bedc6e003c8fcb6ddc00648906d674fc1d4c5b2e82a6680469e7f789b52`  
		Last Modified: Sat, 19 Oct 2024 02:56:49 GMT  
		Size: 64.0 MB (63986649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9369d4f874cc01265f2427f626d8649c9cdd3722f987f0d4b53aa17f58a1a519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6c6d1f54b094e28a0a046b11471758394539a5e24a2d8ac19ce9002a04517c`

```dockerfile
```

-	Layers:
	-	`sha256:40318f210768de3c2d4f236c08a46c811ed3d6b77f90eca2d352e046bbd4b523`  
		Last Modified: Sat, 19 Oct 2024 02:56:48 GMT  
		Size: 7.6 MB (7591440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894b2057d9859fb2183c0e57461992918a9882da2a000d88bfade69135b7fa9d`  
		Last Modified: Sat, 19 Oct 2024 02:56:47 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8aadefd3e343da4e9702c36796018961a379e983ab737f71f2f3211b60d7593a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128051993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e644e21ad23ef2338385f0c3e116bb4580648461d4de4ce2c03a6bf9154c9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32490c623445d27e949376c8158021571cd8530fc358794dc7642b8bade85da`  
		Last Modified: Thu, 17 Oct 2024 03:39:18 GMT  
		Size: 61.5 MB (61463673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86fb5cafcfd67c91f88f662be09d8efd8f81f8a44fd56b5eec7bb1cfeeadc222
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140385741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599d6e0616d8c9af6627283576f1f866128aa3124b23b7eb286cf69ba6ed97a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd949d90425f27d9499ed62d5edc09c30effb2a25cacc5cdbcec475f72c714b`  
		Last Modified: Thu, 17 Oct 2024 04:37:48 GMT  
		Size: 20.2 MB (20199608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318bda2b7787f1d062cd74c8c3d67fb18e99d812d82717501702fb68c487f68`  
		Last Modified: Thu, 17 Oct 2024 04:38:02 GMT  
		Size: 66.6 MB (66556648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9aaa755d266f547c1623a88949b4896927a675bb6fd3bd3783dddad9c2480671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144071948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aeaac6bc6c4ee0f59e06f93e4c2d110ad682bf40ec1764237e779701249494`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29126a4a4aef17404bd71b479313e117a2f9ea628fcde52f725427fcf1c14fc`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 68.3 MB (68288819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3eb3ece465260e3901ff62f2585ad45a0bfd5b6b634d72a26ed94741a1ae0ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7593234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a0a9bc4cbe59a31877f787277224df9ea7b136f550c13853d5ec0bfd917c8`

```dockerfile
```

-	Layers:
	-	`sha256:cc6abc65fedce21ea5c2f45dc7b45f01c13382ab72ecd3623e069de8d70500a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:40 GMT  
		Size: 7.6 MB (7585959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ddc7234c652467e21b26b6012685d27a4c664f836195c5ee43a6425eb01d17e`  
		Last Modified: Sat, 19 Oct 2024 02:06:40 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90e7b41bb44f0aabb12b036d985456deb388ccec89696004083da5b293198773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138325814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bf84c04011b93921d0604ae5f4b5ff157d7ce4141958a4446f7682abc63e18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0552c8f1cd92a1e8490dffddb1bdf464601603e6f79a1d72baa7fc8463fe5fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ddef53b5b2c40e1838553c952ea8f3401900b10956137e1528e15ff24bcbd`

```dockerfile
```

-	Layers:
	-	`sha256:793454691f682b72aa95b4fbab2aa8dfbd92025fc02eebcd17d82fb50e48bb05`  
		Last Modified: Sat, 19 Oct 2024 02:11:03 GMT  
		Size: 7.1 KB (7141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7288ab3e7e6db09def5b1cc544eb80aa04bd3ef646e07db6f8f6e7c120233aba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151019005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6b9491c5e468741c9c562c0c94e57dddb0d70870f444371ba0aaeac35377aa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d006d9437ccf6825ce93da875340581aaede61b1bb556c25053444f5d60f2`  
		Last Modified: Thu, 17 Oct 2024 01:52:53 GMT  
		Size: 71.9 MB (71897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f41963d04008c34614a5bb83c83566a25d5bdf9e3fd2c195645f296d411e795e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137347404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24da5a220498ee10a0349c6924b4f69cd9ccf123ff35dd6d905d518f132d6f97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cae9f617aba80ede947d89c8c1533181fbf6bbf33b4f52cd58a464daf4cadf`  
		Last Modified: Thu, 17 Oct 2024 01:55:15 GMT  
		Size: 65.8 MB (65759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:85a735d32e2fa43089bdb4f3c65714eb70eb4e91a2ae2ecab4f65c2f5b5b1f0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec962159d905018bf7a4dc6ea49aeca8aa53023ded7a6b21ac8fe3f824aeb1cb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72407aa6b20ec8dd251f8d046dc6a90dc4762b5a40f3de1875d57e9707b2249`  
		Last Modified: Thu, 17 Oct 2024 03:49:29 GMT  
		Size: 21.6 MB (21639364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcc27b289c6aff3a3be7c20455e5a315df5f3865f769b958bcbc9fa8876cad`  
		Last Modified: Thu, 17 Oct 2024 03:49:43 GMT  
		Size: 67.6 MB (67570361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:34bc65ada587328fa2d981afe497617a5502afcd64358e3f24f5b58c77831e52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:66b399a0f86523f2395926abdfe951911afa50511cedc5d1a24f4fbea665e27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349266350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a847434443a8427f04e1557140428137a084fa9fb1dc789dd063478bf276fc79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1c7cfc347f5c86fc2678b58f6a8fb6c6003471405760532fc3240b9eb1b343`  
		Last Modified: Sat, 19 Oct 2024 02:53:19 GMT  
		Size: 211.3 MB (211270246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b84245017497eea4a96ce15840ff736602594d0e8caacf84ddcf1e6e75c89e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15508225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede7bdb92b398bd42c66bb41b29390d617a1b587e4801e9534c3420cf2d7aa33`

```dockerfile
```

-	Layers:
	-	`sha256:f3cba8bcc452cefedc461cca3685c5b6c37d514908d587d0e37481bc48ba50a0`  
		Last Modified: Sat, 19 Oct 2024 02:53:14 GMT  
		Size: 15.5 MB (15497685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece5456f1764c52cad682d0bc55c96cd82870bcf728a20da9c6dc65d508322b2`  
		Last Modified: Sat, 19 Oct 2024 02:53:13 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:25b17e8aa430f3e5bcb80eb5bf8d037ec95ddd242aea4ec0f74d610061282790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316629383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c5935b372870d7f04491d61f1993c99057b2ad1f98130fcab6452319533806`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:24:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:27:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c114860f8d70d4b0766d6eb509df94ed04b6a417e0ad9060f9a9d43e84064ae`  
		Last Modified: Thu, 17 Oct 2024 01:35:20 GMT  
		Size: 22.7 MB (22729227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c96b0eadfdfa6388c6308313b6ff3f016dfa452d0521acc1979654342d6abf`  
		Last Modified: Thu, 17 Oct 2024 01:35:42 GMT  
		Size: 62.0 MB (61999097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614584ff99d2c7b6591b578a66d10c94c81692c6a8c18b8a42671dc8fc7ad543`  
		Last Modified: Thu, 17 Oct 2024 01:36:25 GMT  
		Size: 184.6 MB (184570538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9220348c2292a5c7836e61e5dcaced1895274a5fc67da8d9873bd3140bf89134
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301972566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c7123986773b7fb351e2663141d16472280b9d4938cb89a8abefaa75cf0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d133c6fb31d3251e78f2c641f7d145d5f5b2ab13265639c8eb02354c0ffe35d`  
		Last Modified: Thu, 17 Oct 2024 03:37:52 GMT  
		Size: 175.2 MB (175227696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f66285729903294ee7e6397f09e6e57a1c7b845f491a17236f379b66fca60bc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340197975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeedd65d53caa810d0605b471c43849f76115ad352b7c098195c75e586fe06e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac41aaa9ccd9258f7c6b8f1562698acdae4548533ae639ff6653baa08033c71c`  
		Last Modified: Thu, 17 Oct 2024 04:36:51 GMT  
		Size: 202.7 MB (202669297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1c21375b08b4d0f25f20769d2547d2948982c8e2744ea336a64d389f2a87c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351867123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c98997c4e35d7cb7e3a88082701de0bd4f2daa9ee328f9cdbb34e20318504e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ebe45cbbff83005bfa62fa86d2064e8ccedae2cd7617a6d60696a420bd1bb`  
		Last Modified: Sat, 19 Oct 2024 02:53:15 GMT  
		Size: 210.2 MB (210186933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34adb642fac5f95817489d8165bf13bf55504c9704e969f5d3c78af5f052ed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a43af330dd7cc88d66c01cbd66a2333691dd02459d83800710b92e3e526ad`

```dockerfile
```

-	Layers:
	-	`sha256:7c909413102d12d54aa31d8cc5582cbe0762e5a40d49bbf051d2cfced9df8ae8`  
		Last Modified: Sat, 19 Oct 2024 02:53:11 GMT  
		Size: 15.5 MB (15476264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854336bbcc82191d23e44fbe1fb86eed9659b15b27f56cc7343ed66df224eff6`  
		Last Modified: Sat, 19 Oct 2024 02:53:10 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eedf47cd0217818cf4687c2bed18ecec128b16af82475584ebbeabff390e5f70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326348772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71650f7afcc0ee2ce3640621c54788a7d5851b59ef46e25c54141eb87a7ea58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:08:45 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Thu, 17 Oct 2024 01:08:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:48:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb4cb3753c5260533ae9297767f8b73bc0cd6f1dc878635a173148920d80368`  
		Last Modified: Thu, 17 Oct 2024 02:08:35 GMT  
		Size: 23.6 MB (23647379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e244535d91d08a7c42eab7cd45ea82c43428356bc75a90c8d486507e9888f0a`  
		Last Modified: Thu, 17 Oct 2024 02:09:28 GMT  
		Size: 63.3 MB (63297195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8f8a184e3174b4b3b76091c95baf89a636e164f9c732b010464037c162209`  
		Last Modified: Thu, 17 Oct 2024 02:11:35 GMT  
		Size: 189.8 MB (189842579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bafc61e1014935dde758d5d8c2f2cf3614486ab7024e8c1dd51e5eca3d9a1e60
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363396234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa68f72feb2ed3326c5b70c46fc86e32731822125a51dc10faaca60d96896e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:44:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d27751f2c723de9cfb2cbb2775f1c16c1f3653cdff74eae652ff9cc1633eda6`  
		Last Modified: Thu, 17 Oct 2024 01:52:21 GMT  
		Size: 214.3 MB (214300830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22357b5316cabb794fe07c11c4af17599270f951b8c9e21430952eb1f022716b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318793259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6716f9f26b5e12b4faf3947ea48f9b157956dc7cab733983b5e315635eac4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:42:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77632955ee6981fa7ca39f104872912fb4579734ee466c2eb2d442ca4c8a29cd`  
		Last Modified: Thu, 17 Oct 2024 03:49:21 GMT  
		Size: 183.3 MB (183307845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:89f0653a0a912939914d7df4bfbf6b6759e1713ac7307b734d205628eb195879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f5bb9ad274f7483bca35b7ade28409ddc366a3030c721f8ec01945f49c1f1400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73606409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6595c5df915beb56b486d44173ffcd9c8778b221483592385d56eace9a801f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f0ef8013ba25f54dfd23730377c2d93f590a45df065a2fbd1f91b943b36a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c17604ff561b13d6f71ee7c0a751e0b1d183ffa185632d141c0ba72398ed3a8`

```dockerfile
```

-	Layers:
	-	`sha256:afafc89040020b7a28a31732e2dc724fbcf41e580d58b02b74e8b0b4a2872c90`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 4.4 MB (4365270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4400ed85ba89c4bbb3ecdd1deb3eec80325469a08196255657479cc4d709369d`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29e22265f8e27deff56e30507c4bf3c45395cf51cd0cb178b01a10d0e74fee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7708f0af4315775dde7d656b19d6d877ece75b21b2f7335d8bcba64cefecd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4af3bdf4e5d1217cfc39da2266dc0351e9da0d1cd982341b997f89ea78399711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9290411caaa63ac5ed8e0a3029f8c3819fbbc16a6f4487e2f8424d6bc5d62dd2`

```dockerfile
```

-	Layers:
	-	`sha256:09bac3dbe394bb359e9648ccd0cd52e4092634e941964afb8413c9256644626c`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 4.4 MB (4368785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66fbb3bdefadf96a90da6d4bba1633b49859fa6532385c149fde11810506952`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c662459553ad055a4708b89aa5566791ba9f6db440495230e423d3717ed80f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e198c6502a080d5a4c664099e8b9ff589ac930f16668d5f130cf883973bbaa81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cba624557f8771ff8e6f953c75df4617cfa8c60ca2b011736603d07c4444364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9976a29b32bbb9b5140ecd8b4bf572ea9cc6d74bd34b93452ba7cd5c03473689`

```dockerfile
```

-	Layers:
	-	`sha256:24a261958b30f61e4637a1276fecfd8dc488e904699a6f9c0198b7ff85717689`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 4.4 MB (4367566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6bc5453abd7e83a2ee028712e1c439a5056c837ebe26cafe5657b46bb64d60`  
		Last Modified: Sat, 19 Oct 2024 00:56:09 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b676273f23311ccc5244ff6e63155dad8b5bb55b6d82b8f4e8d33972ef6e4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa631a28a982643843676b9f863f4d093a30c8b4fb480687f9dd53bab255da5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a44f1891b371bcae4f11edff9fd8aba7516fce6c2ff75aa458027d07967d8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cbd7f1f078bdc9aecceee2b5a77d73e45b0bf9b977b377ddcf47db36b3e1b4`

```dockerfile
```

-	Layers:
	-	`sha256:579eb45b34cd6da0fb68f0f67d8357369dadbde36df878a8b285533dd9fb9385`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 4.4 MB (4365542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7295b715924a4334f4fbb9c240fcd002eea2c8913954669a52796ad9fa45891`  
		Last Modified: Sat, 19 Oct 2024 01:10:42 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4efd8cc6fecc767a4806aab581f19e51c45faa286f89478f3967e5eeff607d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75471772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2131351b74d10ef77e845cfcfcbd26ab0a63bb6cf71eb9d1b38b7a253694a7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8464dd421e7a13ca2df0a0ed389801a2de33aaa8ff036e0e0a6e3b59de523dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94482666a0f9222c4e2432930198f007ba125621aecbb5b0a20a303cf82f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:bd25bf9485ae7822635d94ac3ac93b79ed69aae815fe5d3237c28b028036df11`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 4.4 MB (4362326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daf96ddb27c922caa431414e6f3178b8a5546068f19f674e9e40d530b3a9207`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40a0ca2a9d801d94c209dd4e81179674356393b1bb85a7c778a3f4374809cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b37c7d352dda03ef9d6be2c8d635f31984a92699dab52f36b5d3f12c515f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fc9c2dd787c1afef1c1632c49d1eb5b563a6facb531dd8b470488959b3ab9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 KB (6798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4747016d2b84e54ffe37fd4cf0d9b6bb34a7055915405f718b1dd16b0a090478`

```dockerfile
```

-	Layers:
	-	`sha256:eff80f8d463471c1876e84ba06456595ac60a9fd7d52d23925ba9857a315e820`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 6.8 KB (6798 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:704d078e6f0512924e23fabc519c270c4337592544ac088b753a03beb2edca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae709f8a5a2c18f20fdfcc13765d33af7c929548193c66e87d682e2d4338628e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:802ada8d1fd6a69d696bd789b9e6ed88a9e51de5e365b475c2d0bb3e15964827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d70d877c0e5eb209272eaa51467fd68839cc0c02f90c896d0ef9848c923e5d`

```dockerfile
```

-	Layers:
	-	`sha256:b6e7a8cf77bf1496c9a858f7c7a6f5e188fe91072b7afb22d90ae72605902920`  
		Last Modified: Sat, 19 Oct 2024 00:56:53 GMT  
		Size: 4.4 MB (4369763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1ded31c90b6bb0502d04c6c8a2dd6581bfd17ac18f5381e46d9ad71ed29b0d`  
		Last Modified: Sat, 19 Oct 2024 00:56:52 GMT  
		Size: 7.0 KB (6997 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21adcc891214e1112da5648d6249bc00f6bf79e3e4f4877a81e94b9650c2abff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf3690d729d99a4c77c28f19d3e7ceb3e8a868a32d1fd17330077491fa06c6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b672735e07b6bfd358f69deeb922ae67580e9d16527ecebd87aebebf732dc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb7d494d53ee86cc3697683f361f7502649fb74eedbbf4aa682d707dc2b17a3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1dfd30ced67644e7b9d672f6c07044e4b073d0d5506e4c0fcce2d600a96042`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 4.4 MB (4364967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a34545ab0e16c7b338028391562e8fb28abcfdebbb1613eff8f60838579b1`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:b7b31cf258096b5047be55aa30dad94e2ceb052c8c9e10c00d35725b10ec1bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e413426d5ceb4bc8b8485584a2334f982af09c40a294c8bf8bf6cdaeeee9875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137996104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6a3fd709dc98777b4ee2dac0d91e0d775c501c5f754c2721afda51367884fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:267daf9a035387db438e0e46fd4b93300a407ab8d2a8a08471e53480601da952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b34fb506a8ed23e1d427f349569ab9a18e6805d6de10ec99ed6a589dd583cc`

```dockerfile
```

-	Layers:
	-	`sha256:9f092bdcc560f05d219daef70c3dbe1cbf5beb875614df187738facf640574ae`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 7.8 MB (7764370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305b58c6aa4607a016c86411aaec62620a8480a7db911cf2b1b620bc59033585`  
		Last Modified: Sat, 19 Oct 2024 02:06:35 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:065821ca01f5b46e546b666ebc542baa9cadd26c83971d920f718a4d04641532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132056978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c329746ec886de5abee981e2a8dad46f0a25ec5606516321a628ea9cec7098a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d8e5c6c3bd120c07665df831c223d98cd86db7ad072c55a7433e227d49b3d`  
		Last Modified: Sat, 19 Oct 2024 02:55:37 GMT  
		Size: 62.0 MB (61996882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:993bf84285db8ca4c11425d3a303adbe960660b326c4fe16d6692cff7d2cab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7175b75d18a4b7c149ef131238c169805dae0110254e68d196b78cef76713d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8b6c17ef335d13a13ac672b98127369486d26b77a478f85e6dda04d194d55425`  
		Last Modified: Sat, 19 Oct 2024 02:55:36 GMT  
		Size: 7.8 MB (7765924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1348c0de7b4712e505c350d0c2142d3801c2c26e7c23faa55c9ce197ddd624d2`  
		Last Modified: Sat, 19 Oct 2024 02:55:35 GMT  
		Size: 7.7 KB (7734 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eccb934d63bac8c068380c9805d9b43b7f336b4c18f3240641a37e90dca17cf3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126744870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e0a5ed5211488d49c46201bd0003329cdeac002c563154869325cec7f1e5c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:24ff51eac951beb8cae6eb10c9a6316b92ba535f6ce57b697816a2f90d9e35fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d53a93f46b21e92bf85f52aefd48305b7987e7037693f374d44cb5e8ce0324`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:273c4a697c5f46c260ff0dc5ce28da78d7895442714cfe2ae670c62596c94c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141680190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f891597f8aa0b920eab180791c23ad8f9ffc9da20a5a68b66b0c2a936320a4a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7c27a970016230430108f980988c338d4d1137a98cd2b936476020943ea3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0fde0a53d069f07ff292e0334b827638c5a995a20f008cb02dca195cc9b24f`

```dockerfile
```

-	Layers:
	-	`sha256:e43a3a69d39b1261a900b087590ce28109339ec7b0fb043a670c0683b9cc0a50`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.8 MB (7760446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f61feb336f32426818cb28c5c4aae9e6aeea748ea4612b3d85b14136f23d82a`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c927f08d08e798a2932be4e20dad881e66c13708cd3fd12432a15db03914f304
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149095404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a195c447ca2ab15bd44723fc52ceba6b8484d8f8e8b74bf23786dbff4233d1a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:96caeb2a156ac3e5a114582e769104d80579b8f79601b73c7f453b4d8c947bc0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849e1c7b1cd0aa3c234e84d733980139487f92521f08631a58f63d02eb0e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:f9736689b5f3de513f841e1679ba4a4ac70d697d54a2d6ea41b26df57afc0404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0357130b032ae0c854db1dc21229137704ae206a83f05daf23ffc95712eecf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367984491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a39104e33d7cad4c9c9d85b3127205c321bf8353351b6730a4181a98e58027`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62683c6ad6022c8249b2258dcace69634541663e2eceb81fb4c1c2e36d49de26`  
		Last Modified: Sat, 19 Oct 2024 02:53:50 GMT  
		Size: 227.9 MB (227866497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49b2368a3f95d6e910307e3c9f69f87deb7c2d3354b778e2874705c3bb4d5ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16507570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0df43ec87be3e27a39b4d13c738ef559f245755c425d593b205930559792820`

```dockerfile
```

-	Layers:
	-	`sha256:92f3ef1413b81322d8f5ea466d1cc9afec312eb414214d83c7c9cba360fa6bf1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 16.5 MB (16497377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee48f91490aa5f9944f1624c3f85bbc3f0562946751903e3d5c114b1e114b1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dfb638ac11b12fef8510bcd4e28a26e5f4098a2d1414b6b5718ceca4300ca23a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336055761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164af35a4a2654f15149ebbe020f83269d27a6e0fccba1b295239d7a0590c776`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:33:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881241cc914c17be2c506105e054bfcf46ca5dc3a2c61b399fb49563a725f97c`  
		Last Modified: Thu, 17 Oct 2024 01:37:57 GMT  
		Size: 19.6 MB (19644443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cc8728e864cc21d996b1238d79456f457c2d6f8c5d26d74916564e44abbe5b`  
		Last Modified: Thu, 17 Oct 2024 01:38:20 GMT  
		Size: 63.7 MB (63741533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08102b561e7767bc425138ba99beed9786e26ab88c0b070d2835c1c29a5044`  
		Last Modified: Thu, 17 Oct 2024 01:39:04 GMT  
		Size: 202.5 MB (202523688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:54125fe0eca21864407bcc5465626b7b25012068ec1cd2387efb6bc127ebad95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317481868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c0a305057a0e790d5004feb9ec9b00b36af5f837395a3d959ca76d7ce6614`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:36:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b14885f9520938c577e16ecdfccbd10cf46510a9c0149d0d479ccd879d93d6`  
		Last Modified: Thu, 17 Oct 2024 03:40:06 GMT  
		Size: 19.0 MB (18974054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebaaebd3fa818b1b4bafe8e7f26090da3811fd6c155b2f7f73dc8875a3a905`  
		Last Modified: Thu, 17 Oct 2024 03:40:26 GMT  
		Size: 61.2 MB (61233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884e2f9eb216cf208e6169a9d6d8edb9392a7ce4982869962011c53fb6f91d88`  
		Last Modified: Thu, 17 Oct 2024 03:40:58 GMT  
		Size: 189.6 MB (189614810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4a38f49d0091a4e29280f14a38096f5f1099c0cf22ede3cd23325ba805631f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361333988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f530ebd9306ef5feceda1fb5383ad5d2ac5f7a5a1461680639651f171a94057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:35:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc979a58041d0ca8e5deac6b7852b9a756f65c5fde4ed5a01b9ab02ba82ff2a8`  
		Last Modified: Thu, 17 Oct 2024 04:38:39 GMT  
		Size: 20.4 MB (20385295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f53239df6d74ac78e3ea17ce45a2e39dfce24b675fc31f8f4d6cf9bb4b4e1`  
		Last Modified: Thu, 17 Oct 2024 04:38:53 GMT  
		Size: 66.3 MB (66305737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7481d379b4107b6f999b57394ad368f476ac3b244f21a8fd4fcdbb47e6854b5`  
		Last Modified: Thu, 17 Oct 2024 04:39:21 GMT  
		Size: 221.0 MB (221043231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee56890ed8d6f91cba4394aa3f5083c5123400202ab7d096522a85a831f612f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.6 MB (372586202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcecdf46d089364cbde632cfb8e3b506ec37ff689e40ba870fd8b365626314c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9067ce74b0ad44714f9fcdde6e1e80ccc5ea632bd70cc38760f160485b65493`  
		Last Modified: Sat, 19 Oct 2024 02:53:44 GMT  
		Size: 228.7 MB (228713750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2795e01efc42f3f6e6dec027b25de27f203b53cb39ba0bf807d31e1d8fda2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16477955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8734bfa35aa50645b7863013835b368e0353dcea699cb346e1e1c5a7d046a558`

```dockerfile
```

-	Layers:
	-	`sha256:f840f39bb756f2de1a67ce2157b37a9f49eb73423510632741ce767af0764190`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 16.5 MB (16467785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de718ffef3484dc52d3236b9e93a9bbcfb9884f51c7d9cde604bc6d4b99c1d2`  
		Last Modified: Sat, 19 Oct 2024 02:53:38 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:25eab8db5e0fac52c8246295fd5f054b693548c5b4c48cf3140a9f06be463754
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345215162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d84b1e19fc528971a6245468bd3defca3f2af877b4d5c6a6f34dd718ad316`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:57 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Thu, 17 Oct 2024 01:14:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:07:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3136c2a952f0ce80aeca2b6928afe3f03863f57c7fa1a03ebd2f7c0be5923c8`  
		Last Modified: Thu, 17 Oct 2024 02:15:26 GMT  
		Size: 21.0 MB (20965665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8f48a50ba530f6de6ffd4fea12c7a1881ea25592c7713fae880299f80511d7`  
		Last Modified: Thu, 17 Oct 2024 02:16:17 GMT  
		Size: 65.1 MB (65075286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918b279067b0d9d3b75423dc4f7c0ec8f715830135aff70d1d449bac131e76a`  
		Last Modified: Thu, 17 Oct 2024 02:18:32 GMT  
		Size: 207.0 MB (207045743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c1c38533b14a5bfa7c72de8bc53e0f27ba26f26081f394f36c3df35723273da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13637603f1051994f2585a17e7ff16d6ba6ddb533434905b593d7b7e5c41fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:50:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2644f355ce42082bdc3b0fffe0d7e95a4d8ecfcb7944e76a2d5fdfa12edfaef9`  
		Last Modified: Thu, 17 Oct 2024 01:54:41 GMT  
		Size: 226.2 MB (226153671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff2315a159e26c773bde3e416a35ce0ed9d4879c4a50de17da0589c3b92a54e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342774272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a95637bec4073de581503c4ecea9334cfc150932106b7843177ddf1f4e0649`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:46:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49835389a5b3be307cfcaee824ac271d1c990968ebef582d739387fe8cd1a5`  
		Last Modified: Thu, 17 Oct 2024 03:50:19 GMT  
		Size: 21.7 MB (21658714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0166b7d6671ccc810cbc6335bc33f3a6c82e87668bb0dee7a3abc097ff3d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:34 GMT  
		Size: 67.3 MB (67337716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b8b77d7a85513a728feea2661f7073ec071f3c4b10f104596ac74c52221ccb`  
		Last Modified: Thu, 17 Oct 2024 03:51:06 GMT  
		Size: 201.0 MB (200968998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:7ecfffb1978afc408d8922a2e925c0da92adc84b7056993542afd3abead40ac9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:13ba48a39e49ad4224206ef4111573c78c0dbdd3c59b6ed2ce33737540e73a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73881838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab6e767aaa3846e228d2aaa6322419c5ed05783a2ab2b8f2fcce6aa4677bbe9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7409253a7e847b804d94b25e8565c1d10d179a6c537b4940e549f023d069f220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4038664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eed7b5961637c56866ae20d8cff4952694da18a469583f39a3b396db743420`

```dockerfile
```

-	Layers:
	-	`sha256:df34962ff2adfadfb55dd3289bb365a8d5331a60aff73679e94e4d75cfb53837`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 4.0 MB (4032049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8013d519a714465b0d90a32a711f90e63c306560be9921dde04a140667f8791e`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 6.6 KB (6615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:44587876a59180032936457314b2babd35d42606989255948cfcbcea3cadbf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69789535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfb39f99b8fda7147b1af2b874fac0256a3f8bdc89a2461e7e834a9d9f962d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5571697784adcbe29d963579310eec564ff21e0a1805050b884b9a866946b3`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 19.6 MB (19643438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e07e94399d23d6880f9eeb46bde8eae9a8fb1902b4d038f0603f5639cedfe64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4041585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a54131ae3fdcc04aa19834ce0d53ae4fd85c07c3e94903fe1e121254fb6362c`

```dockerfile
```

-	Layers:
	-	`sha256:c78e4644705e96e9cdf51310f0552e40528eadc188306b088a21a182973b4acf`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 4.0 MB (4034915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa4c72da9c23809a987c7fa8b040114bcc0701afc2ef98ca972a928d34fbd6a`  
		Last Modified: Sat, 19 Oct 2024 00:56:33 GMT  
		Size: 6.7 KB (6670 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d180725042f2a2ab49c7c1fc447b08346fb410e8ccd2b39bc09bb2659897fb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aa632581817d68db4b843ad2aa9212467fb669c2e00b7a7d088070fda64f10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0470a2043ec3f25f0ea4f3cb171bf6eb63e84dd5756b6bf5428f806acaf5dfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97995b1fa73615aadd85b6c368ad28025d05668f1b7b57284489e441b06335b3`

```dockerfile
```

-	Layers:
	-	`sha256:79ed41688f0e95b7523b86415bef63aa4e0dc77c85bcfcea2c6526035fa5de6d`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 4.0 MB (4033713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2b4c6aeb777eb4ce5f93ac05e1d77537a7e8902cb2591c2a91b517434fc58f`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 6.7 KB (6670 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a93ed2b7476c4b4c650d0a9e767323a8425d86600c581d1a5dac3a12efcbba72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73982198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ea30739a536e3ca9caafac54fa4ed6021ae0b7de4d14ce468c8447f4be04d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75b88c801460857ce4f252829edc9b947a6cc73b60e70899f3fbc468903fd61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdff6d26f35602884a10eb106d1fcef888490b5112225c1d15f36474069cd61`

```dockerfile
```

-	Layers:
	-	`sha256:d5fd34ed984463d07df79cc91b1d1c74f4bf811aaa1fb60164a1db5677985fb2`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 4.0 MB (4032468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af92e790d6db773e23efea622300f00befcf371d8ec6f379548da7163789749`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 6.7 KB (6690 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:284be1eb3a5d4e3ec0fbb6ccbffd2f544caa83a0688b8d3145968ec3d7fce25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75832050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e62c9fa74bd73c613b2d414de936d5e6dbbe1fc981bdfe073b58c2dcaa90d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97f662007de27c1016876c4327f065d1a6150b08b13fbb409ac8eb279066306a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e876d69c00182b52ac667f71d9f8cafc863d159d45d3b74e1b0a711d90abb7f1`

```dockerfile
```

-	Layers:
	-	`sha256:351253b273e4604b92f1388009c76fdf0ea8370f45e06e62972ad44d6fbcedfd`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 4.0 MB (4028460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418686a489e6b45aaf3a654aa8d9e9a643649b49cce15b58e8cc33e889e429c1`  
		Last Modified: Sat, 19 Oct 2024 00:55:04 GMT  
		Size: 6.6 KB (6595 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f834ebfbe3e95dd0a105cb4a810aaf3adc6c6391bf2680fe4c29be7a23b9281b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73095108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1941ea8fe9aa74da25cc9b80d0ac7be9bc5f367fa62c06d53ffebbea28d5c6a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:677a0de1f4921cb9e1a2a4c4e4672acb0db8ad7c31cf75cda470c9510bde06e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 KB (6440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53ebeafa5f6414326bb74bb26680e262cc9dfabad9e7bae6fd98d33e9435b8`

```dockerfile
```

-	Layers:
	-	`sha256:a067562384d90203b881d6bc281e38e7dc13db73587e1a6f680ee0df93128ad6`  
		Last Modified: Sat, 19 Oct 2024 01:01:29 GMT  
		Size: 6.4 KB (6440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:333a3246926edcdafcdb086c05e26cd8f6e47ba0652964d2be4d30ad95d33fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80441503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2a144cb176366e52828f4fa686b8276615b96c81728dc782a985f769b315f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5667fe15aa72deb415d8548705d0d2c925ac903348d2c609e965984d9c47957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add606c2a2dd6eefd6489f1cfee162f25d6a04391121d4b25476fa52c230804e`

```dockerfile
```

-	Layers:
	-	`sha256:ddbfe5c9a08ff9950faed8f84c34aef3b9f0e80b32022611b962f3ddf2fd4334`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 4.0 MB (4035924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f686912dedd73eebfe8b75f1e82f2e525ceeebc2915692f915949ee62c4642a`  
		Last Modified: Sat, 19 Oct 2024 00:58:54 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24dcbbd0e2ee32d1dba9e2e5844af10d131703be2f58837fd22aa7f1f036bf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71667113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bd6b050755f4e2f11dc7120e640aa938167574228c3e901d4ae13e0d782f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9afe98cafb187775506b46e655b83f4d919ff657d9c24036a88a37c7e186b3`  
		Last Modified: Sat, 19 Oct 2024 01:06:46 GMT  
		Size: 20.1 MB (20137929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2125c80eac7fb61dee0bf4629df8ac0785422e6e4c56f8f15ff090b697e76324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49637a86d8c0ceaf270f6bc7ded55e1afba9aee8479567a486af0a1a9b906b`

```dockerfile
```

-	Layers:
	-	`sha256:a45cc8e562fd303037be29b476fa881a7ec77fd72466df42383dc6c612c2088f`  
		Last Modified: Sat, 19 Oct 2024 01:06:44 GMT  
		Size: 4.0 MB (4024707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9bb89a3de98c2ea298a2ff66fa98c5e299403e1665068622932e7b890ab2b`  
		Last Modified: Sat, 19 Oct 2024 01:06:43 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75197af0953909f02c53f06d7e40d6a7e65c221dbb2c0a42fdc262c5b4a80e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74465032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b15816e014bf9d61c00cb9093592a90a5369f9dd284b359d92e9dfc789413`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cdcdb6c4c742b0560c3cd9217a2794dd3d3f6f343b591149399564df9735cdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cfec82e6efabe5ecf20d815273ee2628d6a0dd1e64df1c881f7e1748c51ea1`

```dockerfile
```

-	Layers:
	-	`sha256:3af77f9d57d4a2973c5d311064cd302187c63a5d2d2d4ca220a47d8a197bf8ac`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 4.0 MB (4033619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e2450e5fbba047105865ee8ea4145e5355d4459c0397033c277fd63d2ae0336`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:6774ea1a783f4f0ae05bd6cf7773de625ea972be3425df3518e08457ca8093bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:585656e13819d78a14d2e7038d5589af3eb6ee746bd30c82af2f8f043cb6aa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140117994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3148837dc0db0a85a6b1d6b04ea41f0888a3c7bf61c285769d5ae575e85ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ea20d5bba8eeb2e736601c4ce114c361ac3fd03f83fef30075d024149db987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e878cfa426f7d6f801ecbbd4da423790a35e9bb7f34a8518dceca0b05684c7f`

```dockerfile
```

-	Layers:
	-	`sha256:716f9e78031d3606e499bc4442ab01887e9daa138a84cd6040598b8b55e62485`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 7.5 MB (7485854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b2b2da54ba360e1746e997c125c6c346c80274f7fa7c490be56551d6f15d1f`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d37244e77642358ecbd8e02f932a2b902759f4e78f883342dd90c58bbbe8d718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133522236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c554071c074e0f5662cb4bfd4cfcded5ab8352625767fff7ca547532bd761ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5571697784adcbe29d963579310eec564ff21e0a1805050b884b9a866946b3`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 19.6 MB (19643438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e345c83b2739677a81bb65e8b14bcf4b74047ea7c75729f3715016f0c7c8e4f7`  
		Last Modified: Sat, 19 Oct 2024 02:57:55 GMT  
		Size: 63.7 MB (63732701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00d18a1cb21b84828374be7fe1569f0476ca91ce608c97e03e32e76273476c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e31d4e7fafe882a373e7a7298f5ea1647b1dbad6b13ce047d5cad2aedc3856`

```dockerfile
```

-	Layers:
	-	`sha256:20ca6cafe1bb36aec82c18a4b5ccdd308f9b10df0fa623351c59a932487d23de`  
		Last Modified: Sat, 19 Oct 2024 02:57:54 GMT  
		Size: 7.5 MB (7486766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c289e55fa61eb9c6049628f33edc91f1f20e240525f00e07e32498727c00d77`  
		Last Modified: Sat, 19 Oct 2024 02:57:53 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7066697a91a60d58795b2dd1699ae8b9951013f80a080391f83686cebb637d54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127867058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf8200bc2a2bc7388ab86d683b382038f7813763c843e631c234a14bd75d738`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b14885f9520938c577e16ecdfccbd10cf46510a9c0149d0d479ccd879d93d6`  
		Last Modified: Thu, 17 Oct 2024 03:40:06 GMT  
		Size: 19.0 MB (18974054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebaaebd3fa818b1b4bafe8e7f26090da3811fd6c155b2f7f73dc8875a3a905`  
		Last Modified: Thu, 17 Oct 2024 03:40:26 GMT  
		Size: 61.2 MB (61233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c91745059177b9c9ad8fb87b88908d8b89088446c5f8218182e1b847016d5859
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140290757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9abd2ff50f4249f751e5e2c3ba9e16c83bcdde940957f0a880f1786823d540`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc979a58041d0ca8e5deac6b7852b9a756f65c5fde4ed5a01b9ab02ba82ff2a8`  
		Last Modified: Thu, 17 Oct 2024 04:38:39 GMT  
		Size: 20.4 MB (20385295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f53239df6d74ac78e3ea17ce45a2e39dfce24b675fc31f8f4d6cf9bb4b4e1`  
		Last Modified: Thu, 17 Oct 2024 04:38:53 GMT  
		Size: 66.3 MB (66305737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:618815a42dba3ef78d1bb1de67f7ec2120dfdaad4720867753833cf4630f498e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143872452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e030da0121eee0eeab55546bdd08ca40bf003cf82e576562069a02c56e0e8dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9008ac0613d41a0c2c395978561fe3ab8e18ff11ef7a1e577f10639da50b0e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3243a0416ab3c6b119ec1cf4e4e94ebdf31c3c374bc98f9b50e32fe11750e5`

```dockerfile
```

-	Layers:
	-	`sha256:7200b6a54740017d2b112c3bdeb08ad5b7011927790105fe36431b2f1e85f597`  
		Last Modified: Sat, 19 Oct 2024 02:06:43 GMT  
		Size: 7.5 MB (7481278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e262c25f641beedd8d9a8f58c64c13dd27c10bf508ee4c52904493950f448c`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:78d50bdb37e5bb8ce65015b943145de8356d61c7bf9ac0d2b70b5bb19d61592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138151112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c40a1f4ab862506927452bfc655b5b498b376a47d0ebbd5c7fe468eb7a88db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81190818ed7d83b0f92ee66dc853e7c6f22b9535d8e52f4f00fcfdc4354973ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f37bae74959741f2259d72bed0704bd028bbb2ff4414f68912774344bbdbf3c`

```dockerfile
```

-	Layers:
	-	`sha256:c02dd3eab5f5e9db4c0f38c6e763e61d6cf4e72819705f3060c07ec5c7819c76`  
		Last Modified: Sat, 19 Oct 2024 02:14:21 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:416d68c7a6ea996450091adfc2ad7659fe479b8592d3deb58962a40a976088ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152071022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a632aee26b4b1f0c77d9eea17429ff8bd4d62ccfc6a7c47e2034dda6e1ffa5f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4092e136e316706611e3fe5fa99da9c6cabe42ae013f7299d619ad4f8b8a3552
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141805274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b6c9ff4c72451df23ef7ace56e7a671b1e27f39121b289a02c061aa4ac6b1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49835389a5b3be307cfcaee824ac271d1c990968ebef582d739387fe8cd1a5`  
		Last Modified: Thu, 17 Oct 2024 03:50:19 GMT  
		Size: 21.7 MB (21658714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0166b7d6671ccc810cbc6335bc33f3a6c82e87668bb0dee7a3abc097ff3d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:34 GMT  
		Size: 67.3 MB (67337716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:f9736689b5f3de513f841e1679ba4a4ac70d697d54a2d6ea41b26df57afc0404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0357130b032ae0c854db1dc21229137704ae206a83f05daf23ffc95712eecf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367984491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a39104e33d7cad4c9c9d85b3127205c321bf8353351b6730a4181a98e58027`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62683c6ad6022c8249b2258dcace69634541663e2eceb81fb4c1c2e36d49de26`  
		Last Modified: Sat, 19 Oct 2024 02:53:50 GMT  
		Size: 227.9 MB (227866497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49b2368a3f95d6e910307e3c9f69f87deb7c2d3354b778e2874705c3bb4d5ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16507570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0df43ec87be3e27a39b4d13c738ef559f245755c425d593b205930559792820`

```dockerfile
```

-	Layers:
	-	`sha256:92f3ef1413b81322d8f5ea466d1cc9afec312eb414214d83c7c9cba360fa6bf1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 16.5 MB (16497377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee48f91490aa5f9944f1624c3f85bbc3f0562946751903e3d5c114b1e114b1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dfb638ac11b12fef8510bcd4e28a26e5f4098a2d1414b6b5718ceca4300ca23a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336055761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164af35a4a2654f15149ebbe020f83269d27a6e0fccba1b295239d7a0590c776`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:33:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881241cc914c17be2c506105e054bfcf46ca5dc3a2c61b399fb49563a725f97c`  
		Last Modified: Thu, 17 Oct 2024 01:37:57 GMT  
		Size: 19.6 MB (19644443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cc8728e864cc21d996b1238d79456f457c2d6f8c5d26d74916564e44abbe5b`  
		Last Modified: Thu, 17 Oct 2024 01:38:20 GMT  
		Size: 63.7 MB (63741533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08102b561e7767bc425138ba99beed9786e26ab88c0b070d2835c1c29a5044`  
		Last Modified: Thu, 17 Oct 2024 01:39:04 GMT  
		Size: 202.5 MB (202523688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:54125fe0eca21864407bcc5465626b7b25012068ec1cd2387efb6bc127ebad95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317481868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c0a305057a0e790d5004feb9ec9b00b36af5f837395a3d959ca76d7ce6614`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:36:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b14885f9520938c577e16ecdfccbd10cf46510a9c0149d0d479ccd879d93d6`  
		Last Modified: Thu, 17 Oct 2024 03:40:06 GMT  
		Size: 19.0 MB (18974054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebaaebd3fa818b1b4bafe8e7f26090da3811fd6c155b2f7f73dc8875a3a905`  
		Last Modified: Thu, 17 Oct 2024 03:40:26 GMT  
		Size: 61.2 MB (61233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884e2f9eb216cf208e6169a9d6d8edb9392a7ce4982869962011c53fb6f91d88`  
		Last Modified: Thu, 17 Oct 2024 03:40:58 GMT  
		Size: 189.6 MB (189614810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4a38f49d0091a4e29280f14a38096f5f1099c0cf22ede3cd23325ba805631f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361333988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f530ebd9306ef5feceda1fb5383ad5d2ac5f7a5a1461680639651f171a94057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:35:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc979a58041d0ca8e5deac6b7852b9a756f65c5fde4ed5a01b9ab02ba82ff2a8`  
		Last Modified: Thu, 17 Oct 2024 04:38:39 GMT  
		Size: 20.4 MB (20385295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f53239df6d74ac78e3ea17ce45a2e39dfce24b675fc31f8f4d6cf9bb4b4e1`  
		Last Modified: Thu, 17 Oct 2024 04:38:53 GMT  
		Size: 66.3 MB (66305737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7481d379b4107b6f999b57394ad368f476ac3b244f21a8fd4fcdbb47e6854b5`  
		Last Modified: Thu, 17 Oct 2024 04:39:21 GMT  
		Size: 221.0 MB (221043231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee56890ed8d6f91cba4394aa3f5083c5123400202ab7d096522a85a831f612f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.6 MB (372586202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcecdf46d089364cbde632cfb8e3b506ec37ff689e40ba870fd8b365626314c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9067ce74b0ad44714f9fcdde6e1e80ccc5ea632bd70cc38760f160485b65493`  
		Last Modified: Sat, 19 Oct 2024 02:53:44 GMT  
		Size: 228.7 MB (228713750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2795e01efc42f3f6e6dec027b25de27f203b53cb39ba0bf807d31e1d8fda2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16477955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8734bfa35aa50645b7863013835b368e0353dcea699cb346e1e1c5a7d046a558`

```dockerfile
```

-	Layers:
	-	`sha256:f840f39bb756f2de1a67ce2157b37a9f49eb73423510632741ce767af0764190`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 16.5 MB (16467785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de718ffef3484dc52d3236b9e93a9bbcfb9884f51c7d9cde604bc6d4b99c1d2`  
		Last Modified: Sat, 19 Oct 2024 02:53:38 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:25eab8db5e0fac52c8246295fd5f054b693548c5b4c48cf3140a9f06be463754
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345215162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d84b1e19fc528971a6245468bd3defca3f2af877b4d5c6a6f34dd718ad316`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:57 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Thu, 17 Oct 2024 01:14:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:07:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3136c2a952f0ce80aeca2b6928afe3f03863f57c7fa1a03ebd2f7c0be5923c8`  
		Last Modified: Thu, 17 Oct 2024 02:15:26 GMT  
		Size: 21.0 MB (20965665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8f48a50ba530f6de6ffd4fea12c7a1881ea25592c7713fae880299f80511d7`  
		Last Modified: Thu, 17 Oct 2024 02:16:17 GMT  
		Size: 65.1 MB (65075286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918b279067b0d9d3b75423dc4f7c0ec8f715830135aff70d1d449bac131e76a`  
		Last Modified: Thu, 17 Oct 2024 02:18:32 GMT  
		Size: 207.0 MB (207045743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c1c38533b14a5bfa7c72de8bc53e0f27ba26f26081f394f36c3df35723273da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13637603f1051994f2585a17e7ff16d6ba6ddb533434905b593d7b7e5c41fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:50:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2644f355ce42082bdc3b0fffe0d7e95a4d8ecfcb7944e76a2d5fdfa12edfaef9`  
		Last Modified: Thu, 17 Oct 2024 01:54:41 GMT  
		Size: 226.2 MB (226153671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff2315a159e26c773bde3e416a35ce0ed9d4879c4a50de17da0589c3b92a54e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342774272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a95637bec4073de581503c4ecea9334cfc150932106b7843177ddf1f4e0649`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:46:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49835389a5b3be307cfcaee824ac271d1c990968ebef582d739387fe8cd1a5`  
		Last Modified: Thu, 17 Oct 2024 03:50:19 GMT  
		Size: 21.7 MB (21658714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0166b7d6671ccc810cbc6335bc33f3a6c82e87668bb0dee7a3abc097ff3d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:34 GMT  
		Size: 67.3 MB (67337716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b8b77d7a85513a728feea2661f7073ec071f3c4b10f104596ac74c52221ccb`  
		Last Modified: Thu, 17 Oct 2024 03:51:06 GMT  
		Size: 201.0 MB (200968998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:7ecfffb1978afc408d8922a2e925c0da92adc84b7056993542afd3abead40ac9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:13ba48a39e49ad4224206ef4111573c78c0dbdd3c59b6ed2ce33737540e73a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73881838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab6e767aaa3846e228d2aaa6322419c5ed05783a2ab2b8f2fcce6aa4677bbe9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7409253a7e847b804d94b25e8565c1d10d179a6c537b4940e549f023d069f220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4038664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eed7b5961637c56866ae20d8cff4952694da18a469583f39a3b396db743420`

```dockerfile
```

-	Layers:
	-	`sha256:df34962ff2adfadfb55dd3289bb365a8d5331a60aff73679e94e4d75cfb53837`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 4.0 MB (4032049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8013d519a714465b0d90a32a711f90e63c306560be9921dde04a140667f8791e`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 6.6 KB (6615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:44587876a59180032936457314b2babd35d42606989255948cfcbcea3cadbf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69789535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfb39f99b8fda7147b1af2b874fac0256a3f8bdc89a2461e7e834a9d9f962d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5571697784adcbe29d963579310eec564ff21e0a1805050b884b9a866946b3`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 19.6 MB (19643438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e07e94399d23d6880f9eeb46bde8eae9a8fb1902b4d038f0603f5639cedfe64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4041585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a54131ae3fdcc04aa19834ce0d53ae4fd85c07c3e94903fe1e121254fb6362c`

```dockerfile
```

-	Layers:
	-	`sha256:c78e4644705e96e9cdf51310f0552e40528eadc188306b088a21a182973b4acf`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 4.0 MB (4034915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa4c72da9c23809a987c7fa8b040114bcc0701afc2ef98ca972a928d34fbd6a`  
		Last Modified: Sat, 19 Oct 2024 00:56:33 GMT  
		Size: 6.7 KB (6670 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d180725042f2a2ab49c7c1fc447b08346fb410e8ccd2b39bc09bb2659897fb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aa632581817d68db4b843ad2aa9212467fb669c2e00b7a7d088070fda64f10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0470a2043ec3f25f0ea4f3cb171bf6eb63e84dd5756b6bf5428f806acaf5dfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97995b1fa73615aadd85b6c368ad28025d05668f1b7b57284489e441b06335b3`

```dockerfile
```

-	Layers:
	-	`sha256:79ed41688f0e95b7523b86415bef63aa4e0dc77c85bcfcea2c6526035fa5de6d`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 4.0 MB (4033713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2b4c6aeb777eb4ce5f93ac05e1d77537a7e8902cb2591c2a91b517434fc58f`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 6.7 KB (6670 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a93ed2b7476c4b4c650d0a9e767323a8425d86600c581d1a5dac3a12efcbba72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73982198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ea30739a536e3ca9caafac54fa4ed6021ae0b7de4d14ce468c8447f4be04d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75b88c801460857ce4f252829edc9b947a6cc73b60e70899f3fbc468903fd61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdff6d26f35602884a10eb106d1fcef888490b5112225c1d15f36474069cd61`

```dockerfile
```

-	Layers:
	-	`sha256:d5fd34ed984463d07df79cc91b1d1c74f4bf811aaa1fb60164a1db5677985fb2`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 4.0 MB (4032468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af92e790d6db773e23efea622300f00befcf371d8ec6f379548da7163789749`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 6.7 KB (6690 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:284be1eb3a5d4e3ec0fbb6ccbffd2f544caa83a0688b8d3145968ec3d7fce25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75832050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e62c9fa74bd73c613b2d414de936d5e6dbbe1fc981bdfe073b58c2dcaa90d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97f662007de27c1016876c4327f065d1a6150b08b13fbb409ac8eb279066306a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e876d69c00182b52ac667f71d9f8cafc863d159d45d3b74e1b0a711d90abb7f1`

```dockerfile
```

-	Layers:
	-	`sha256:351253b273e4604b92f1388009c76fdf0ea8370f45e06e62972ad44d6fbcedfd`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 4.0 MB (4028460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418686a489e6b45aaf3a654aa8d9e9a643649b49cce15b58e8cc33e889e429c1`  
		Last Modified: Sat, 19 Oct 2024 00:55:04 GMT  
		Size: 6.6 KB (6595 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f834ebfbe3e95dd0a105cb4a810aaf3adc6c6391bf2680fe4c29be7a23b9281b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73095108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1941ea8fe9aa74da25cc9b80d0ac7be9bc5f367fa62c06d53ffebbea28d5c6a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:677a0de1f4921cb9e1a2a4c4e4672acb0db8ad7c31cf75cda470c9510bde06e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 KB (6440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53ebeafa5f6414326bb74bb26680e262cc9dfabad9e7bae6fd98d33e9435b8`

```dockerfile
```

-	Layers:
	-	`sha256:a067562384d90203b881d6bc281e38e7dc13db73587e1a6f680ee0df93128ad6`  
		Last Modified: Sat, 19 Oct 2024 01:01:29 GMT  
		Size: 6.4 KB (6440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:333a3246926edcdafcdb086c05e26cd8f6e47ba0652964d2be4d30ad95d33fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80441503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2a144cb176366e52828f4fa686b8276615b96c81728dc782a985f769b315f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5667fe15aa72deb415d8548705d0d2c925ac903348d2c609e965984d9c47957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add606c2a2dd6eefd6489f1cfee162f25d6a04391121d4b25476fa52c230804e`

```dockerfile
```

-	Layers:
	-	`sha256:ddbfe5c9a08ff9950faed8f84c34aef3b9f0e80b32022611b962f3ddf2fd4334`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 4.0 MB (4035924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f686912dedd73eebfe8b75f1e82f2e525ceeebc2915692f915949ee62c4642a`  
		Last Modified: Sat, 19 Oct 2024 00:58:54 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24dcbbd0e2ee32d1dba9e2e5844af10d131703be2f58837fd22aa7f1f036bf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71667113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bd6b050755f4e2f11dc7120e640aa938167574228c3e901d4ae13e0d782f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9afe98cafb187775506b46e655b83f4d919ff657d9c24036a88a37c7e186b3`  
		Last Modified: Sat, 19 Oct 2024 01:06:46 GMT  
		Size: 20.1 MB (20137929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2125c80eac7fb61dee0bf4629df8ac0785422e6e4c56f8f15ff090b697e76324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49637a86d8c0ceaf270f6bc7ded55e1afba9aee8479567a486af0a1a9b906b`

```dockerfile
```

-	Layers:
	-	`sha256:a45cc8e562fd303037be29b476fa881a7ec77fd72466df42383dc6c612c2088f`  
		Last Modified: Sat, 19 Oct 2024 01:06:44 GMT  
		Size: 4.0 MB (4024707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9bb89a3de98c2ea298a2ff66fa98c5e299403e1665068622932e7b890ab2b`  
		Last Modified: Sat, 19 Oct 2024 01:06:43 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75197af0953909f02c53f06d7e40d6a7e65c221dbb2c0a42fdc262c5b4a80e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74465032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b15816e014bf9d61c00cb9093592a90a5369f9dd284b359d92e9dfc789413`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cdcdb6c4c742b0560c3cd9217a2794dd3d3f6f343b591149399564df9735cdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cfec82e6efabe5ecf20d815273ee2628d6a0dd1e64df1c881f7e1748c51ea1`

```dockerfile
```

-	Layers:
	-	`sha256:3af77f9d57d4a2973c5d311064cd302187c63a5d2d2d4ca220a47d8a197bf8ac`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 4.0 MB (4033619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e2450e5fbba047105865ee8ea4145e5355d4459c0397033c277fd63d2ae0336`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:6774ea1a783f4f0ae05bd6cf7773de625ea972be3425df3518e08457ca8093bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:585656e13819d78a14d2e7038d5589af3eb6ee746bd30c82af2f8f043cb6aa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140117994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3148837dc0db0a85a6b1d6b04ea41f0888a3c7bf61c285769d5ae575e85ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ea20d5bba8eeb2e736601c4ce114c361ac3fd03f83fef30075d024149db987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e878cfa426f7d6f801ecbbd4da423790a35e9bb7f34a8518dceca0b05684c7f`

```dockerfile
```

-	Layers:
	-	`sha256:716f9e78031d3606e499bc4442ab01887e9daa138a84cd6040598b8b55e62485`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 7.5 MB (7485854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b2b2da54ba360e1746e997c125c6c346c80274f7fa7c490be56551d6f15d1f`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d37244e77642358ecbd8e02f932a2b902759f4e78f883342dd90c58bbbe8d718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133522236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c554071c074e0f5662cb4bfd4cfcded5ab8352625767fff7ca547532bd761ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5571697784adcbe29d963579310eec564ff21e0a1805050b884b9a866946b3`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 19.6 MB (19643438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e345c83b2739677a81bb65e8b14bcf4b74047ea7c75729f3715016f0c7c8e4f7`  
		Last Modified: Sat, 19 Oct 2024 02:57:55 GMT  
		Size: 63.7 MB (63732701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00d18a1cb21b84828374be7fe1569f0476ca91ce608c97e03e32e76273476c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e31d4e7fafe882a373e7a7298f5ea1647b1dbad6b13ce047d5cad2aedc3856`

```dockerfile
```

-	Layers:
	-	`sha256:20ca6cafe1bb36aec82c18a4b5ccdd308f9b10df0fa623351c59a932487d23de`  
		Last Modified: Sat, 19 Oct 2024 02:57:54 GMT  
		Size: 7.5 MB (7486766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c289e55fa61eb9c6049628f33edc91f1f20e240525f00e07e32498727c00d77`  
		Last Modified: Sat, 19 Oct 2024 02:57:53 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7066697a91a60d58795b2dd1699ae8b9951013f80a080391f83686cebb637d54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127867058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf8200bc2a2bc7388ab86d683b382038f7813763c843e631c234a14bd75d738`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b14885f9520938c577e16ecdfccbd10cf46510a9c0149d0d479ccd879d93d6`  
		Last Modified: Thu, 17 Oct 2024 03:40:06 GMT  
		Size: 19.0 MB (18974054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebaaebd3fa818b1b4bafe8e7f26090da3811fd6c155b2f7f73dc8875a3a905`  
		Last Modified: Thu, 17 Oct 2024 03:40:26 GMT  
		Size: 61.2 MB (61233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c91745059177b9c9ad8fb87b88908d8b89088446c5f8218182e1b847016d5859
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140290757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9abd2ff50f4249f751e5e2c3ba9e16c83bcdde940957f0a880f1786823d540`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc979a58041d0ca8e5deac6b7852b9a756f65c5fde4ed5a01b9ab02ba82ff2a8`  
		Last Modified: Thu, 17 Oct 2024 04:38:39 GMT  
		Size: 20.4 MB (20385295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f53239df6d74ac78e3ea17ce45a2e39dfce24b675fc31f8f4d6cf9bb4b4e1`  
		Last Modified: Thu, 17 Oct 2024 04:38:53 GMT  
		Size: 66.3 MB (66305737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:618815a42dba3ef78d1bb1de67f7ec2120dfdaad4720867753833cf4630f498e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143872452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e030da0121eee0eeab55546bdd08ca40bf003cf82e576562069a02c56e0e8dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9008ac0613d41a0c2c395978561fe3ab8e18ff11ef7a1e577f10639da50b0e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3243a0416ab3c6b119ec1cf4e4e94ebdf31c3c374bc98f9b50e32fe11750e5`

```dockerfile
```

-	Layers:
	-	`sha256:7200b6a54740017d2b112c3bdeb08ad5b7011927790105fe36431b2f1e85f597`  
		Last Modified: Sat, 19 Oct 2024 02:06:43 GMT  
		Size: 7.5 MB (7481278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e262c25f641beedd8d9a8f58c64c13dd27c10bf508ee4c52904493950f448c`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:78d50bdb37e5bb8ce65015b943145de8356d61c7bf9ac0d2b70b5bb19d61592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138151112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c40a1f4ab862506927452bfc655b5b498b376a47d0ebbd5c7fe468eb7a88db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81190818ed7d83b0f92ee66dc853e7c6f22b9535d8e52f4f00fcfdc4354973ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f37bae74959741f2259d72bed0704bd028bbb2ff4414f68912774344bbdbf3c`

```dockerfile
```

-	Layers:
	-	`sha256:c02dd3eab5f5e9db4c0f38c6e763e61d6cf4e72819705f3060c07ec5c7819c76`  
		Last Modified: Sat, 19 Oct 2024 02:14:21 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:416d68c7a6ea996450091adfc2ad7659fe479b8592d3deb58962a40a976088ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152071022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a632aee26b4b1f0c77d9eea17429ff8bd4d62ccfc6a7c47e2034dda6e1ffa5f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4092e136e316706611e3fe5fa99da9c6cabe42ae013f7299d619ad4f8b8a3552
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141805274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b6c9ff4c72451df23ef7ace56e7a671b1e27f39121b289a02c061aa4ac6b1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49835389a5b3be307cfcaee824ac271d1c990968ebef582d739387fe8cd1a5`  
		Last Modified: Thu, 17 Oct 2024 03:50:19 GMT  
		Size: 21.7 MB (21658714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0166b7d6671ccc810cbc6335bc33f3a6c82e87668bb0dee7a3abc097ff3d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:34 GMT  
		Size: 67.3 MB (67337716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:ed75310d8d7ed0c1dabd36cd5f4a5737ae852ed98e66def603616315f5e2a053
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e8a9bfddf607e07c59acad6b37e74a677f55b222264fff4086481b94f103248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368573290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608313d91b8bea5bfdaa7ae32f69dd84b19a7f528219c5ce18cd67955c1d10e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b881a2f1232350ec7e4aefdf5b77bf5210861f5960ef5f73da8c0d1966802d8`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 66.5 MB (66470763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86943b23dc3779237d892368b9a4c4fc090241e0fbaaada00b55b3055d2b3bc9`  
		Last Modified: Sat, 19 Oct 2024 02:53:08 GMT  
		Size: 228.3 MB (228271921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:406de61fc1deaa52ed02dda2f9335e5a3add1c139b419573cf5ce61aa0e5df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16623042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996b9f714262ed15f13040714584face383fd4a6b534fb51a47c89f857d30b03`

```dockerfile
```

-	Layers:
	-	`sha256:912cf800b3ff32bb074626dd668053449112fc6e0bda6515290514d72472b67f`  
		Last Modified: Sat, 19 Oct 2024 02:53:05 GMT  
		Size: 16.6 MB (16612866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccba7f94f8614c179b40098212350a18928af7d09ff485a475fb59ede87a07e`  
		Last Modified: Sat, 19 Oct 2024 02:53:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7e95232f4447716af74bd2907bedc9ab047b94e7bdb4cfc15cb1cf4492f4afb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336701350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e528f9913cf5ebdc3bfd2c5f1ae6fdca4debe882d4913b75fe13dd04460aedca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:41 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Thu, 17 Oct 2024 00:54:42 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:31:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b51e9513f401d905da66d3e959803693c1c78e3059a3fd54de6ad45f59179fa`  
		Last Modified: Thu, 17 Oct 2024 01:36:39 GMT  
		Size: 19.6 MB (19568932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52911f6537dc2fd850c0c63bf4aa3806ec9b40b64d351e34d00f5df0a1434fb6`  
		Last Modified: Thu, 17 Oct 2024 01:37:00 GMT  
		Size: 64.0 MB (63988084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb87602ce298bd118421d8a0f5456cad47ee48016fbe2aa008e1d427dbefcb0`  
		Last Modified: Thu, 17 Oct 2024 01:37:45 GMT  
		Size: 203.0 MB (202996746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:515c123d32c6aa7255a21ad574f394666fb16d3c565f24fa15b43dbcbb1182c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318104301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ee1ccf0154b3ec16d5f2b9555c44031d50cb756335a8bc0da6d1f3ad98246`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:34:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32490c623445d27e949376c8158021571cd8530fc358794dc7642b8bade85da`  
		Last Modified: Thu, 17 Oct 2024 03:39:18 GMT  
		Size: 61.5 MB (61463673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb9fde67196f11fd2b11fdc769e780383d757a9acd06f324a681d5a67d9f62`  
		Last Modified: Thu, 17 Oct 2024 03:39:55 GMT  
		Size: 190.1 MB (190052308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cae551d9dadb734a5c69ebeea30a565d17de285a771aef3133c80a56dd4098d6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (361995529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a63ceca4055cba5256307ce8eb7d05410d4ce178cdbbab2397ffa42a05af067`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd949d90425f27d9499ed62d5edc09c30effb2a25cacc5cdbcec475f72c714b`  
		Last Modified: Thu, 17 Oct 2024 04:37:48 GMT  
		Size: 20.2 MB (20199608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318bda2b7787f1d062cd74c8c3d67fb18e99d812d82717501702fb68c487f68`  
		Last Modified: Thu, 17 Oct 2024 04:38:02 GMT  
		Size: 66.6 MB (66556648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462feea23048f5379dbf36ebd591bca7bfe2e21ad6e6208a43952a5b97fe62e9`  
		Last Modified: Thu, 17 Oct 2024 04:38:30 GMT  
		Size: 221.6 MB (221609788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2586af5cbad80ef32c8987ed795e71f33f008118127d124c39f84dbed46b6b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.2 MB (373211235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c837d757dc27783ca87e9a16ccfd7676c7adbd00fed98d27616d3f6a128eb548`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29126a4a4aef17404bd71b479313e117a2f9ea628fcde52f725427fcf1c14fc`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 68.3 MB (68288819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4c0958eccba088614505337cf12f450adb63c3426aaabbf6f2e56318550eb2`  
		Last Modified: Sat, 19 Oct 2024 02:53:33 GMT  
		Size: 229.1 MB (229139287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72362d081c1bb8ae447bdca140fe2a9ff70d2754d3d9517a7dc02825a86b3101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16593424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb16d25ce0b74d32d0f00b676aa5ed31860af3eb2f992e62cff99c66b2f57b9`

```dockerfile
```

-	Layers:
	-	`sha256:3cc7643878c4a97b1d4c557d239ab4a5318d6bdb4f9efec20c5580b6184e9a7a`  
		Last Modified: Sat, 19 Oct 2024 02:53:28 GMT  
		Size: 16.6 MB (16583270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d99e8ed8a3e4a6aedcdab18d8a594b76680efaf4b6f36e723a7d3040ced62`  
		Last Modified: Sat, 19 Oct 2024 02:53:28 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e354256e268e95b4eb29793cf5442a60a571ebb0a9ea5333fa57af8d9e49758
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346019892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da56f0d01a64e286c3b8aed43478ed2441a3e37cdbe1e57f345af5e734ae1c96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:10:11 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Thu, 17 Oct 2024 01:10:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:59:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa54e7215b92f68792f1b978dc23df0d8344fea83727a4b5758d7a94f9713e`  
		Last Modified: Thu, 17 Oct 2024 02:11:58 GMT  
		Size: 20.9 MB (20886491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378bf47a6c5edfd4ad9a37322329896d2917b0b410c7f41449f823883f86102a`  
		Last Modified: Thu, 17 Oct 2024 02:12:49 GMT  
		Size: 65.3 MB (65299790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eee4379add186dfd518c292eb7926586afcdbd80524fb9da0627e98bee8333`  
		Last Modified: Thu, 17 Oct 2024 02:15:04 GMT  
		Size: 207.7 MB (207675712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:95f8dc6b9d534fb73f94dc2716623bf57a1930dd890d0db13e2ca8ca122dfd2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377765962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9bc7b533f4e3ec7e3a3429cf0c5995b27faf10b7fdb016559a4c7432dad9f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:47:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d006d9437ccf6825ce93da875340581aaede61b1bb556c25053444f5d60f2`  
		Last Modified: Thu, 17 Oct 2024 01:52:53 GMT  
		Size: 71.9 MB (71897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f60d866924718e5a834ee211294703f7ccaff0c50b423716b8bcbdbadf15ee`  
		Last Modified: Thu, 17 Oct 2024 01:53:31 GMT  
		Size: 226.7 MB (226746957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4219b43dc777d41d6f85d0c160677d87619eb13b75f3158cd5218abb7610f899
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.6 MB (449638935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cda9e1a8b19f0634dc0500a3dfb906412d655f75153f0909ff3ddaa1b30871`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:50:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cae9f617aba80ede947d89c8c1533181fbf6bbf33b4f52cd58a464daf4cadf`  
		Last Modified: Thu, 17 Oct 2024 01:55:15 GMT  
		Size: 65.8 MB (65759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4626b5f0a1b5e29bea40bdb350f939636cf2ba36351f5395f5d5c70852c7323`  
		Last Modified: Thu, 17 Oct 2024 02:00:59 GMT  
		Size: 312.3 MB (312291531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:375e8c731f4d01824b9332690c9bc0377345820ca71cc0b6daa0c1fc23f1d377
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343571564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3383977a925f9a62c1772339c9b74a27793502173fd36b4571b22d9a104dc16e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:44:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72407aa6b20ec8dd251f8d046dc6a90dc4762b5a40f3de1875d57e9707b2249`  
		Last Modified: Thu, 17 Oct 2024 03:49:29 GMT  
		Size: 21.6 MB (21639364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcc27b289c6aff3a3be7c20455e5a315df5f3865f769b958bcbc9fa8876cad`  
		Last Modified: Thu, 17 Oct 2024 03:49:43 GMT  
		Size: 67.6 MB (67570361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c8221625d4527cfc16993073388dd3031e9a3bebc65ac9e3d124ff4e8c28d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:12 GMT  
		Size: 201.5 MB (201509858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:09c665801f99b13aace18d0e534ca5fba8a95ccb9f491844b58d9a407a6681cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4969fc1482fe79df2f83454d450d1bb1a0bd65812c9965ae1acecbb37b03ccaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73830606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c95b99c5f7fcf27f8df865460d0bef48e4fe0499bbe6de82a9a812aabc372a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fda6398e5597471e4fe9a09bac438b822a76bfed6ac08368ef40b1e9ddea52e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e230e9497a2cbdf9af9438fc5a0ccb4b9846b644ac01b445504fbe028091fc11`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ea3fac8fffc480e851a74e960ed5d1e7f9b10adb718c0c389bb83bc052b6b`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 4.0 MB (4028672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c832042891b017cd09224285e67cb4bceed33f487315c2467b0339ebb7a651`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9fbe3208573220b4f9bc991ffbff5b241a40dc9207a1412852dc5e1dcfb848e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69716210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ee3aa87633d009b362e51572dc98a9cacd568e8c58399568da58bc7055fb22`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907cc8268897b865af11c617e0b6df9243de9b6a7c9d42c7a265f1e626be0e8`  
		Last Modified: Sat, 19 Oct 2024 00:55:48 GMT  
		Size: 19.6 MB (19568622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:704a4556dc0a7e5eada6cecd5287d4b85008c956b40b973ff74e5d10709940d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4038180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e52b0f8e26eb0efb788150f3213c247649ab0db37b9738559d888b15bcec526`

```dockerfile
```

-	Layers:
	-	`sha256:5c0bd3e2f79edb6da9625f1f9e47004acdf5cae6c326bd0785fe7cf585ac3400`  
		Last Modified: Sat, 19 Oct 2024 00:55:47 GMT  
		Size: 4.0 MB (4031537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4621ddefc20eb42391d2bdf32281c9b15abec3dc9d43bcbe5483b50017401b`  
		Last Modified: Sat, 19 Oct 2024 00:55:47 GMT  
		Size: 6.6 KB (6643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77c60cc265b95be3b104f0c8621b935379cee41049a173a232dc5ec430fd706c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66585055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80a481113f99d5a8cae3310407042e0a289b71236d59c1ed76c30c45339a239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa977a262dd181b45467b256087bca990abede89e133911524cdd68e44f417fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253aa76a9639b3e075a66b78d5e33f7d1c5029dd58b35967c686755f5c25c939`

```dockerfile
```

-	Layers:
	-	`sha256:88a067eab1dd02b5d086716eef3db36d32ebbb0f1c6015519cc361eb70246783`  
		Last Modified: Sat, 19 Oct 2024 00:57:31 GMT  
		Size: 4.0 MB (4030333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad857591c01e9afa58b31c832b0a59d253a0df59d62143775e95f07d9629f49a`  
		Last Modified: Sat, 19 Oct 2024 00:57:31 GMT  
		Size: 6.6 KB (6643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bc7f373af02269a239ab6419112615ca6690809a8d95bf7f43f1377dd2d6f476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73826100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08daf7da3e665395ab5a0d8cc1d5f760a074733172716e6fd4467fd79b96d66e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d70cfbc938d76d89a533bfb2fc5f1c306ff2beed08d6499de05ee55cdf580a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8716ecd1dfdc9cc5c59cec4b6019e1bfc0b6dc6055fc96fa508f5361182df192`

```dockerfile
```

-	Layers:
	-	`sha256:b591e9052a8f907be44d4656ffc3d018c55b54387630fff05f2d2fe1759dd869`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 4.0 MB (4029090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56316a4f7de5fa0299ba7bea33b33e2864d292edecf4a7905dd390fb3254c0de`  
		Last Modified: Sat, 19 Oct 2024 01:11:42 GMT  
		Size: 6.7 KB (6664 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01c063600551a346c195ff31d7934664465feb4d46a18371953fc30674669422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75783129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac719fac021c9c93427216a8e5a75372d2b1fc4bc2b30e006d6702885ef0db0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3940383fafe27fab3db6136b4524849d3a389a5ab50381c4b7077ed77cc81825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d1f1a9fde212e396e9203d732493e24f84b97ebd6e180174870254520a01f8`

```dockerfile
```

-	Layers:
	-	`sha256:e63b6a0dacd997549b8c0ebf2e2be3f0126dc1e541b72958354c090675d89fbb`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 4.0 MB (4025085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9bac0c42f3e32de80fbee483246d465199d456a4729a7ebfc077321f8618c9`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 6.6 KB (6571 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9ae3cee97b6b487b5d217ef86e5c40770bce1291c93921f4d8d77305d0db5352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73045522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4682cc57a81be3fff028130561f3c6eb09ea9654477dd9e698f799cadabf2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1882a78a33be52eda30fe2c75c6c6d9967f3fd85b20979f451f5c04dfeccde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 KB (6414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b736f996c2064246c296003a1cb4fcddbe3de476eb5b235d73b2a7809cee65`

```dockerfile
```

-	Layers:
	-	`sha256:06fd9bdf5e3ac76086b9540a8eefe0355daaa3d4beb72966f549ffa8f761c5b9`  
		Last Modified: Sat, 19 Oct 2024 00:58:27 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ccdc18d44f05da28c8219d90069f0d4eb9ee4316de834fbd642b3727c20d07a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79120885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c18cc132a9ec9d576c5f9b9c0490878f484b401f205c7de9ca5200fd8115402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f3cdfb0755564cd3c4456a7fa23e621d79e4f8f43bd8107c734f66d381334`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 21.9 MB (21944061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e717a437695f2a383aada0d5bb16603c9d9a4f27abf449da59f9f35a74fe4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e0b0e3c257dcd1365270fe00f03dbe0755fc39c63cf6a714f7595bea11985`

```dockerfile
```

-	Layers:
	-	`sha256:26a67519c427272540f33332e387d267a478d06ad577953e244f4ad7f64ab60c`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 4.0 MB (4032542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec11ed90a7198f124e1e507d4a9a67195e261591152ad27aff7a599b3377cb40`  
		Last Modified: Sat, 19 Oct 2024 00:57:48 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f2563b5986e1cbd6355ebaa519efbefd1ace7d95ec4dc05fb43d702a17656346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71586666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201578f73abedc744f4f2994cc04bf7653e03e6fc71c488b56b938fa6133682`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07e79f5072ea67bddca2130da2f9d315fd8222cd0609708a470e88dfa7353806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dcf549e44ce65cf2139914167a0d0f4b1a4302bf162cbab4d7642cccbbb69`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d1496ab905e4028f005f5a14166826563eecf34a3ccd9a6dd3ce4b9c1412c`  
		Last Modified: Sat, 19 Oct 2024 01:03:15 GMT  
		Size: 4.0 MB (4022143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d30c866b540503398d1018dd68b46d07f0f51532b55b00079c6208979ebb5f5`  
		Last Modified: Sat, 19 Oct 2024 01:03:14 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd2690414a6039d75b84c97bdaa113a12b72489d077a52b352aac6b045265d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74491620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290e9362d4f9db9760c8fc711ee0feb3425e972e82f673ff4917fe4a53e4cc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:372f3917080ed9eb9334f2c5f62c4d74cd82f0cb2530167d4024f63f3560fbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ad897ff0a89dc21885858a1e52dab7c9c8f5bb20638df51acb70d74756d2d9`

```dockerfile
```

-	Layers:
	-	`sha256:92a80cba733f641e49791d7770b207706dac2cc27956dcc0d0194f817f64b791`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 4.0 MB (4030243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8dcbcfacdd30256d369d06a17871979b477713f3b331489382dfe1f6da6133`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:98480a63588e0a05d8e2d525f5446b38da7aecc1af800401e54709066e389111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cefdabdf0dd3c0be2093674bd463a08706c6823b51ef5fc98e48ffc279c7b2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140301369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873827b625b63287b3afef0bf4cb27db9fad9dbd5c4d914199e2e3ad3886952d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b881a2f1232350ec7e4aefdf5b77bf5210861f5960ef5f73da8c0d1966802d8`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 66.5 MB (66470763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86827b548c07c2a481cae7d5aed48a4134e1de1c2408c43d0149d39d11eb5be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7597828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6b88eacd87f5f5f93b910719a867bece0a91123b33c13459cd08adfccd1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:511627375d7bd2a499e03c8cfffc6fba5567efd8d47aa35eb624b4dedfbeec23`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.6 MB (7590531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3af11e7fde68c3dcc1bcb722db1234981bee58c66281bb50a9ac93c213e05d`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1a0c5e363a8c8458928698c18a4a8e521685db479a3e4929571a9edf7be07e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133702859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecd7b81df49fc9583d1ed7d438d04c77a3510d7c84eff4854a7cbdb89fd0882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907cc8268897b865af11c617e0b6df9243de9b6a7c9d42c7a265f1e626be0e8`  
		Last Modified: Sat, 19 Oct 2024 00:55:48 GMT  
		Size: 19.6 MB (19568622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f2bedc6e003c8fcb6ddc00648906d674fc1d4c5b2e82a6680469e7f789b52`  
		Last Modified: Sat, 19 Oct 2024 02:56:49 GMT  
		Size: 64.0 MB (63986649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9369d4f874cc01265f2427f626d8649c9cdd3722f987f0d4b53aa17f58a1a519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6c6d1f54b094e28a0a046b11471758394539a5e24a2d8ac19ce9002a04517c`

```dockerfile
```

-	Layers:
	-	`sha256:40318f210768de3c2d4f236c08a46c811ed3d6b77f90eca2d352e046bbd4b523`  
		Last Modified: Sat, 19 Oct 2024 02:56:48 GMT  
		Size: 7.6 MB (7591440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894b2057d9859fb2183c0e57461992918a9882da2a000d88bfade69135b7fa9d`  
		Last Modified: Sat, 19 Oct 2024 02:56:47 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8aadefd3e343da4e9702c36796018961a379e983ab737f71f2f3211b60d7593a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128051993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e644e21ad23ef2338385f0c3e116bb4580648461d4de4ce2c03a6bf9154c9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32490c623445d27e949376c8158021571cd8530fc358794dc7642b8bade85da`  
		Last Modified: Thu, 17 Oct 2024 03:39:18 GMT  
		Size: 61.5 MB (61463673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86fb5cafcfd67c91f88f662be09d8efd8f81f8a44fd56b5eec7bb1cfeeadc222
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140385741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599d6e0616d8c9af6627283576f1f866128aa3124b23b7eb286cf69ba6ed97a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd949d90425f27d9499ed62d5edc09c30effb2a25cacc5cdbcec475f72c714b`  
		Last Modified: Thu, 17 Oct 2024 04:37:48 GMT  
		Size: 20.2 MB (20199608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318bda2b7787f1d062cd74c8c3d67fb18e99d812d82717501702fb68c487f68`  
		Last Modified: Thu, 17 Oct 2024 04:38:02 GMT  
		Size: 66.6 MB (66556648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9aaa755d266f547c1623a88949b4896927a675bb6fd3bd3783dddad9c2480671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144071948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aeaac6bc6c4ee0f59e06f93e4c2d110ad682bf40ec1764237e779701249494`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29126a4a4aef17404bd71b479313e117a2f9ea628fcde52f725427fcf1c14fc`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 68.3 MB (68288819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3eb3ece465260e3901ff62f2585ad45a0bfd5b6b634d72a26ed94741a1ae0ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7593234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a0a9bc4cbe59a31877f787277224df9ea7b136f550c13853d5ec0bfd917c8`

```dockerfile
```

-	Layers:
	-	`sha256:cc6abc65fedce21ea5c2f45dc7b45f01c13382ab72ecd3623e069de8d70500a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:40 GMT  
		Size: 7.6 MB (7585959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ddc7234c652467e21b26b6012685d27a4c664f836195c5ee43a6425eb01d17e`  
		Last Modified: Sat, 19 Oct 2024 02:06:40 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90e7b41bb44f0aabb12b036d985456deb388ccec89696004083da5b293198773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138325814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bf84c04011b93921d0604ae5f4b5ff157d7ce4141958a4446f7682abc63e18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0552c8f1cd92a1e8490dffddb1bdf464601603e6f79a1d72baa7fc8463fe5fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ddef53b5b2c40e1838553c952ea8f3401900b10956137e1528e15ff24bcbd`

```dockerfile
```

-	Layers:
	-	`sha256:793454691f682b72aa95b4fbab2aa8dfbd92025fc02eebcd17d82fb50e48bb05`  
		Last Modified: Sat, 19 Oct 2024 02:11:03 GMT  
		Size: 7.1 KB (7141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7288ab3e7e6db09def5b1cc544eb80aa04bd3ef646e07db6f8f6e7c120233aba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151019005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6b9491c5e468741c9c562c0c94e57dddb0d70870f444371ba0aaeac35377aa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d006d9437ccf6825ce93da875340581aaede61b1bb556c25053444f5d60f2`  
		Last Modified: Thu, 17 Oct 2024 01:52:53 GMT  
		Size: 71.9 MB (71897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f41963d04008c34614a5bb83c83566a25d5bdf9e3fd2c195645f296d411e795e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137347404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24da5a220498ee10a0349c6924b4f69cd9ccf123ff35dd6d905d518f132d6f97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cae9f617aba80ede947d89c8c1533181fbf6bbf33b4f52cd58a464daf4cadf`  
		Last Modified: Thu, 17 Oct 2024 01:55:15 GMT  
		Size: 65.8 MB (65759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:85a735d32e2fa43089bdb4f3c65714eb70eb4e91a2ae2ecab4f65c2f5b5b1f0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec962159d905018bf7a4dc6ea49aeca8aa53023ded7a6b21ac8fe3f824aeb1cb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72407aa6b20ec8dd251f8d046dc6a90dc4762b5a40f3de1875d57e9707b2249`  
		Last Modified: Thu, 17 Oct 2024 03:49:29 GMT  
		Size: 21.6 MB (21639364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcc27b289c6aff3a3be7c20455e5a315df5f3865f769b958bcbc9fa8876cad`  
		Last Modified: Thu, 17 Oct 2024 03:49:43 GMT  
		Size: 67.6 MB (67570361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
