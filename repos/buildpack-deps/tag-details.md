<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `buildpack-deps`

-	[`buildpack-deps:20.04`](#buildpack-deps2004)
-	[`buildpack-deps:20.04-curl`](#buildpack-deps2004-curl)
-	[`buildpack-deps:20.04-scm`](#buildpack-deps2004-scm)
-	[`buildpack-deps:22.04`](#buildpack-deps2204)
-	[`buildpack-deps:22.04-curl`](#buildpack-deps2204-curl)
-	[`buildpack-deps:22.04-scm`](#buildpack-deps2204-scm)
-	[`buildpack-deps:23.10`](#buildpack-deps2310)
-	[`buildpack-deps:23.10-curl`](#buildpack-deps2310-curl)
-	[`buildpack-deps:23.10-scm`](#buildpack-deps2310-scm)
-	[`buildpack-deps:24.04`](#buildpack-deps2404)
-	[`buildpack-deps:24.04-curl`](#buildpack-deps2404-curl)
-	[`buildpack-deps:24.04-scm`](#buildpack-deps2404-scm)
-	[`buildpack-deps:bookworm`](#buildpack-depsbookworm)
-	[`buildpack-deps:bookworm-curl`](#buildpack-depsbookworm-curl)
-	[`buildpack-deps:bookworm-scm`](#buildpack-depsbookworm-scm)
-	[`buildpack-deps:bullseye`](#buildpack-depsbullseye)
-	[`buildpack-deps:bullseye-curl`](#buildpack-depsbullseye-curl)
-	[`buildpack-deps:bullseye-scm`](#buildpack-depsbullseye-scm)
-	[`buildpack-deps:buster`](#buildpack-depsbuster)
-	[`buildpack-deps:buster-curl`](#buildpack-depsbuster-curl)
-	[`buildpack-deps:buster-scm`](#buildpack-depsbuster-scm)
-	[`buildpack-deps:curl`](#buildpack-depscurl)
-	[`buildpack-deps:focal`](#buildpack-depsfocal)
-	[`buildpack-deps:focal-curl`](#buildpack-depsfocal-curl)
-	[`buildpack-deps:focal-scm`](#buildpack-depsfocal-scm)
-	[`buildpack-deps:jammy`](#buildpack-depsjammy)
-	[`buildpack-deps:jammy-curl`](#buildpack-depsjammy-curl)
-	[`buildpack-deps:jammy-scm`](#buildpack-depsjammy-scm)
-	[`buildpack-deps:latest`](#buildpack-depslatest)
-	[`buildpack-deps:mantic`](#buildpack-depsmantic)
-	[`buildpack-deps:mantic-curl`](#buildpack-depsmantic-curl)
-	[`buildpack-deps:mantic-scm`](#buildpack-depsmantic-scm)
-	[`buildpack-deps:noble`](#buildpack-depsnoble)
-	[`buildpack-deps:noble-curl`](#buildpack-depsnoble-curl)
-	[`buildpack-deps:noble-scm`](#buildpack-depsnoble-scm)
-	[`buildpack-deps:oldoldstable`](#buildpack-depsoldoldstable)
-	[`buildpack-deps:oldoldstable-curl`](#buildpack-depsoldoldstable-curl)
-	[`buildpack-deps:oldoldstable-scm`](#buildpack-depsoldoldstable-scm)
-	[`buildpack-deps:oldstable`](#buildpack-depsoldstable)
-	[`buildpack-deps:oldstable-curl`](#buildpack-depsoldstable-curl)
-	[`buildpack-deps:oldstable-scm`](#buildpack-depsoldstable-scm)
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
$ docker pull buildpack-deps@sha256:57ada2cb624bc8a8b38a36551638108650241a494637ce7f22e9e11c3a1ec709
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
$ docker pull buildpack-deps@sha256:5a099c8c39c1eaacf5f20011a4704b33e9b2f8b5559d7ba453cf616accf90c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245757090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40aa301bba5cdb36c1a9b9f74e15d1db389918958a1dbd9046444b0a638209d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:07:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbac1d6895cea462b85bd61c5b00b59f3b1d16d27b2c7a0a9fb838c4a35ff0b`  
		Last Modified: Fri, 02 Feb 2024 06:22:56 GMT  
		Size: 11.1 MB (11133722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3869ce45a9cfd17d3011945e592fa1799d161adbafd4db9b8bd3659d7965b7`  
		Last Modified: Fri, 02 Feb 2024 06:23:16 GMT  
		Size: 60.9 MB (60904992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997518fc8ff716aa3988c10a05235a0d2f3f09fe4d52e8dd4ea55a266edb2a02`  
		Last Modified: Fri, 02 Feb 2024 06:23:46 GMT  
		Size: 145.1 MB (145133916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06bbef973feb92fd645256eccf79d4ad83b2493d1308ea6fbf33b93175f2e28d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211983832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6baa604c8db1d66316eb9ef3725889845c2fe68d2f5deb855a0ba4a9712ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:54:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996dff6ef7bf273a917daf5f26fdf3ce2a3437a1b88a12d438339cad825fc1a9`  
		Last Modified: Fri, 02 Feb 2024 00:09:47 GMT  
		Size: 55.8 MB (55824821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5faf7a65783ebc0fc71fce330a35048ccfe09acb142df1bcb3449c51e4cc02`  
		Last Modified: Fri, 02 Feb 2024 00:10:15 GMT  
		Size: 122.0 MB (121950628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c8e19ff404d986ed70c9a37728378491351545b1f63dc600b52b67cc7fc56020
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235999243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3577f0f40635ec54c63ace74aa03b9382b74bf2815447d7297fbc2da3158b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb28a40b969d9c86cd7dfd800a5a944b208ada3cd9f8bdef6303362dc2e51a1`  
		Last Modified: Fri, 02 Feb 2024 01:08:15 GMT  
		Size: 61.0 MB (61012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df8ce900192481f0da30214cf0dbf57e840b8842dc245f68513f6afd79e3157`  
		Last Modified: Fri, 02 Feb 2024 01:08:40 GMT  
		Size: 136.8 MB (136796557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d039d78d35643cabe5b2df1832eb9d609fab64344c8d88ea7e8097f4ae67ab8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269529129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c18eda4f812d2fd63ac182480c6a65f39915667de6ffa1ebba948988d9cade`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:05:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c2154c6f7dea8a1736513627d712be0826012c99ae1779a8fc56e36ec1656f`  
		Last Modified: Fri, 02 Feb 2024 02:32:32 GMT  
		Size: 69.7 MB (69653324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e15e3a2cd5f3a2c53f73d28f854d26d6cce5cf8909a67aa711941c4e12f89d`  
		Last Modified: Fri, 02 Feb 2024 02:33:08 GMT  
		Size: 153.6 MB (153618425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ce25d4b95513e23adef005c7fd9686de47217809ddee0313e8cce3f0fdcaa2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226574839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d505195f4353a80806333a66e0853c2c57162ae0f1dab9d7a40034596c00e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:09:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddc6215f51639b9e751c9ce21a6eafd69dfe8cb324818572b591e3eae0d4fd`  
		Last Modified: Fri, 02 Feb 2024 01:33:32 GMT  
		Size: 60.3 MB (60315331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84689abf9543da36ae4ac6e39a52cbc52c219425fe0252a7eb0d2f78b652c9c4`  
		Last Modified: Fri, 02 Feb 2024 01:33:54 GMT  
		Size: 128.6 MB (128550982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:3e2851f3427f9565c91edac93b0811490a271406c9a2a3ff042b3e0567110734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:20.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0a9c6806875afe9f9765d9ea59569f4ca1dec6b84a16ce14d8c14ba1c87ba8f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39718182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777f74cc7faef2a986dc8b9606d33163c0559bb36131a3e5e2fd3d1256b2df46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbac1d6895cea462b85bd61c5b00b59f3b1d16d27b2c7a0a9fb838c4a35ff0b`  
		Last Modified: Fri, 02 Feb 2024 06:22:56 GMT  
		Size: 11.1 MB (11133722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:685522e58ec6ac080fc02a78156dcd12188daecb0cad5f08a6ad2dd6e5c88838
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34208383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9a37b0417478012a7e1cb01d43584be8fb25ee1cc7296f500908280d46e96d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e44afef3d570a2192d3a21369eb2bb6a665cb5015ace2749530e118da7652d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38190366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9131606ec55c459b0fadf79f54cd5d5d2ff7c3db99415d06b3565ab6229a3d55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:61052ed4dfde082d89c08baa9ec09ae4a0657be3295a0392419bcd62397180da
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46257380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae9de359f8e0e053ffdfa852899b95a1b022e18388d1a286bace3eb553ecf34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0903e5570edbd18cfda52e5902d2d3ac8d2c1fc537f53cd628c9a2d209929861
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37708526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5780b02f0e91d91ee0d4c75ec0937daed261ddae8291f3c3fbb2e21634146765`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:cf52c4fff4de6fbf141fecccbe168f18d40324a1733ab3f9569594b12d04b939
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
$ docker pull buildpack-deps@sha256:d5c1357dc17a82fcbf050533276de28eb5348556c1e66b3567c56ab2bf9c5cdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100623174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734a850bee9c779d8a7bbcef1eab90c1dd71dbd13c3c447ba6913d17e92fecc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbac1d6895cea462b85bd61c5b00b59f3b1d16d27b2c7a0a9fb838c4a35ff0b`  
		Last Modified: Fri, 02 Feb 2024 06:22:56 GMT  
		Size: 11.1 MB (11133722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3869ce45a9cfd17d3011945e592fa1799d161adbafd4db9b8bd3659d7965b7`  
		Last Modified: Fri, 02 Feb 2024 06:23:16 GMT  
		Size: 60.9 MB (60904992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7679db02181c821eaf3c9e123ba5bc9f79c65122132d3c12666dbd6c43837e56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90033204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d514200ca52f8623e3fe07018b2558b526a76f8c06dabe134a4651ba501066b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996dff6ef7bf273a917daf5f26fdf3ce2a3437a1b88a12d438339cad825fc1a9`  
		Last Modified: Fri, 02 Feb 2024 00:09:47 GMT  
		Size: 55.8 MB (55824821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:efb0513b800fbbddcab46242de2360dca217dfcca47beb16588e2975453d25c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99202686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cb07a5ca8d12d0d27748239cb61e97c82c2cc3b2f2fa464f0450b55222ce52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb28a40b969d9c86cd7dfd800a5a944b208ada3cd9f8bdef6303362dc2e51a1`  
		Last Modified: Fri, 02 Feb 2024 01:08:15 GMT  
		Size: 61.0 MB (61012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9be807a935c04b3327297d46fb8c6c22f3f4cae154382018718bc613feff81b6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115910704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd40d2021172504c3bd383ce0a1a7ea2adeb61c96998638bce0e293da5b4caea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c2154c6f7dea8a1736513627d712be0826012c99ae1779a8fc56e36ec1656f`  
		Last Modified: Fri, 02 Feb 2024 02:32:32 GMT  
		Size: 69.7 MB (69653324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8046666085765d9bf2050fab2a9cf586f3396073cd2cec9405399dbccfe70b6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98023857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c59508d7157390c04bb299888a57f151ab8c68b8941bc3ed97f9d0ed2e76abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddc6215f51639b9e751c9ce21a6eafd69dfe8cb324818572b591e3eae0d4fd`  
		Last Modified: Fri, 02 Feb 2024 01:33:32 GMT  
		Size: 60.3 MB (60315331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:88ad44a7ede0a5d6f3d8fe80c37ed881e9ef7503f7d2113b7b5c139fefa6129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f8672346b0fb777428615371509403c110627a2d0faf3cfd2718e7537b2545de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250063235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e9d72362a278af11863c18089dadc9da305fd8e8d30db1706cbc04b04b3a67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:12:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9a39c470397903c32405ac6684f74123196728cf153e8f00a4bc25a9ad5fa`  
		Last Modified: Fri, 02 Feb 2024 06:24:10 GMT  
		Size: 39.5 MB (39450166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa202c905468a0a65eec689a73b9f580f6640ff80a02d62ab14b4269fb2daca`  
		Last Modified: Fri, 02 Feb 2024 06:24:42 GMT  
		Size: 173.0 MB (173040419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:56579e6b53540a59b851ba7653982aca23c007a784c94bb6a4aa94df6fbf6d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217314542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc28242d5785ea958aa6a0d4d51726c8367799e7267d65bd22a5035d69700a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:58:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d5022bad6396ad5a6cb649e6d7d08694726302dc3fca7a44c13e3f5ac30d`  
		Last Modified: Fri, 02 Feb 2024 00:10:25 GMT  
		Size: 7.0 MB (7022797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696d12792983d5e91383414e730c71929d81375da8b48757dad5e2c43b79625`  
		Last Modified: Fri, 02 Feb 2024 00:10:40 GMT  
		Size: 42.2 MB (42240510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39d43d0db75bd7b799707677f1dbdb7429fac3fea382e5ff0be946c96ebf6ee`  
		Last Modified: Fri, 02 Feb 2024 00:11:08 GMT  
		Size: 140.5 MB (140524853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe067a914cd3224bb4040ba6ab1bfc2a2f576842cee74c07717fc8725c220318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241353081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1b84b8f8c214cd29f9bc771859efd413aa7095ce18dd1cd58d4fbd226915d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:56:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c57c4e22943bdc69290d3f8794e8a2e6f88492d731e55d42bbab1c04639f6eb`  
		Last Modified: Fri, 02 Feb 2024 01:09:02 GMT  
		Size: 39.4 MB (39365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736ef7ff1a6ba23195fbd71407d2e474032a0f97853d1f46edf2d0d04eb87230`  
		Last Modified: Fri, 02 Feb 2024 01:09:27 GMT  
		Size: 166.5 MB (166517695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:418bbacaab9b7f68449dabbd664df372ddce2e84cb99766e1e4ab6e68333be4f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc534762eb567439ae695adbbe43c770a5d242a22445ff17c8773755b0275f19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:12:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff83656a9f7277ed4028af721dad24c50fa5b1aa50171345db381d06daf43f7d`  
		Last Modified: Fri, 02 Feb 2024 02:33:19 GMT  
		Size: 8.2 MB (8246483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9796e25400f8eaf97eaa611abf40c733cf592de0e724c653064b3b96c416b65`  
		Last Modified: Fri, 02 Feb 2024 02:33:39 GMT  
		Size: 43.8 MB (43763479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1ff09a62e1728a038f10398e632c46d389a2e2eb2c53443a7878b0ff4a8f13`  
		Last Modified: Fri, 02 Feb 2024 02:34:18 GMT  
		Size: 183.7 MB (183699716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:236512f540e7532146f80c458841aff2e94175e89e0d56fcce47e0c47b9b3a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223863647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ddf2f450632e62a7f33c58c50c2e136163b28b3b4f468f9796b1f5195404c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:16:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b25e918744dc60f3fd65aaf829576412d00361b21051000f3822c7226e67`  
		Last Modified: Fri, 02 Feb 2024 01:34:02 GMT  
		Size: 7.0 MB (7038879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ef8c9e80bfa175ac1d1f9cc80ad73756cc4b5510d104e76eab9fb2996f21c9`  
		Last Modified: Fri, 02 Feb 2024 01:34:14 GMT  
		Size: 39.4 MB (39416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5020c9fbfa5f96e33ff00530531a8ecf259cdd21408bda76aa2aa4e9259a77`  
		Last Modified: Fri, 02 Feb 2024 01:34:38 GMT  
		Size: 148.8 MB (148752741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:f70678ffab2d502861bab2a040c7fbcda34f656f65aa5b6d98a8dc41b7b07fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ca247fe943307adbbc89c862972063309df9bdbf3d5a465a729a30bdfb753c34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37572650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99358eaa3f30d6c8bb979a0a8385f0fa6b4030fa5d676c5f7a2f0a512ec4c541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:946fcfa956f0e51964818c238eec222532d4df78c9fbd3c081be301f8dd7c3d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34549179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c919ab35524523d17913d39bc4f2e37bda3ea529c896bb58ae7059176fb227e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d5022bad6396ad5a6cb649e6d7d08694726302dc3fca7a44c13e3f5ac30d`  
		Last Modified: Fri, 02 Feb 2024 00:10:25 GMT  
		Size: 7.0 MB (7022797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bf6a6c222312e0d812ec6b12ea37344464c510d90937183403d7a47287451617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35469714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eecd52d4cc8a99f036d1e08361a520ea21cb5e23e06fe21b6b197503756890b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d5656711867a681e8283ca7af87a5b8b81a1d4fc2972a3db29cc09dd5881360f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43905666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82be83f0500ee8406b164b8a7a0ac3e678ae287321cb584a83cbcc5da3bdf494`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff83656a9f7277ed4028af721dad24c50fa5b1aa50171345db381d06daf43f7d`  
		Last Modified: Fri, 02 Feb 2024 02:33:19 GMT  
		Size: 8.2 MB (8246483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33e671fb304d6abd01cae3fbf077fdd740c71b7308b51b729aefb6bc04fe742a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35694511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa242046750cd4bac13e794163defa6f547b09f3ed3376d579bd6b051d57dee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b25e918744dc60f3fd65aaf829576412d00361b21051000f3822c7226e67`  
		Last Modified: Fri, 02 Feb 2024 01:34:02 GMT  
		Size: 7.0 MB (7038879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:50105ec4dc34351b7aadde13c47544bc99e5de75348393d8e9e2157a402b089e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ac473653eaae3905e8fc87f8ce5a6105e3fbd0b72ecb9d98d766eaa98f66ed7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77022816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edcf3cd0be15910cb39b6eea09069a5b42482c63aa37f4869c25bb2645ff914`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9a39c470397903c32405ac6684f74123196728cf153e8f00a4bc25a9ad5fa`  
		Last Modified: Fri, 02 Feb 2024 06:24:10 GMT  
		Size: 39.5 MB (39450166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e76e7646a6936bec47a21d13b1ff536a43e664b594547ae50a0effdea683070
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76789689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf7cc77eaaf2df12db1f11e199ea41d718543db7e4a7b9ad69179992abfd66c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d5022bad6396ad5a6cb649e6d7d08694726302dc3fca7a44c13e3f5ac30d`  
		Last Modified: Fri, 02 Feb 2024 00:10:25 GMT  
		Size: 7.0 MB (7022797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696d12792983d5e91383414e730c71929d81375da8b48757dad5e2c43b79625`  
		Last Modified: Fri, 02 Feb 2024 00:10:40 GMT  
		Size: 42.2 MB (42240510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d25435931338148a0e89db3840dd6469f1fa180712886e5f399c1d52975ea32f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74835386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408bab5812d49720ec3d1e645690cd2724ce2e6144d8f79ba8d13d2fcffcef78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c57c4e22943bdc69290d3f8794e8a2e6f88492d731e55d42bbab1c04639f6eb`  
		Last Modified: Fri, 02 Feb 2024 01:09:02 GMT  
		Size: 39.4 MB (39365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f3ffe5db9cebbac8cab5b2f958fe769e2f94e52322ba679edca5d08975364ebf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87669145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e272a174802d1005f48c41d236391d05a4749565079f9261edd2985b5864be4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff83656a9f7277ed4028af721dad24c50fa5b1aa50171345db381d06daf43f7d`  
		Last Modified: Fri, 02 Feb 2024 02:33:19 GMT  
		Size: 8.2 MB (8246483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9796e25400f8eaf97eaa611abf40c733cf592de0e724c653064b3b96c416b65`  
		Last Modified: Fri, 02 Feb 2024 02:33:39 GMT  
		Size: 43.8 MB (43763479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a9c84698dc7f4476466493a9e3c4720ee26b4769cb6856ab95c38a12b92aa2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75110906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a2e7d000d01a81ee12b446b2f245c720a8347ea6d2d1ba0c06dea38790e3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b25e918744dc60f3fd65aaf829576412d00361b21051000f3822c7226e67`  
		Last Modified: Fri, 02 Feb 2024 01:34:02 GMT  
		Size: 7.0 MB (7038879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ef8c9e80bfa175ac1d1f9cc80ad73756cc4b5510d104e76eab9fb2996f21c9`  
		Last Modified: Fri, 02 Feb 2024 01:34:14 GMT  
		Size: 39.4 MB (39416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10`

```console
$ docker pull buildpack-deps@sha256:57df129c6a351c0701f07ee4d00dfc5f2b418fc3a7a50a3c9c93d1e20f83dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.10` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:138b0bf02a4899e3b87efdb4f41e9d3d01fa24ff3ceb9c612d0016f15ef0aab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286126174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0798d8057dfdea097ea81ae4f17cd1c2186f9f476a67eede7128374babef1d1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30486de06cd814f639bb675162234bd141b86426c87d43f70eb1fbebf35b62`  
		Last Modified: Fri, 02 Feb 2024 06:25:08 GMT  
		Size: 44.8 MB (44762680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda15b28a080849393425aec2c66e4b830a98b42df059a806a1bd37489474050`  
		Last Modified: Fri, 02 Feb 2024 06:25:41 GMT  
		Size: 203.4 MB (203381033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9e92fada45ce7e502258346671cdd635b8e338d204f337e504ce249982ff30c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251780871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d432dc2ec0d255bc1a6621561ec8b8376dbfb0841b040da1d9b597b2db28ee5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:04:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de61dd38dc0af18a380a823e58045d13cd0b6bf13c269d775509a8a308db69e4`  
		Last Modified: Fri, 02 Feb 2024 00:11:41 GMT  
		Size: 48.9 MB (48949598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a3d11b70586440d9ac926dc050ea93411a1239331c430ee195a2ea149045c0`  
		Last Modified: Fri, 02 Feb 2024 00:12:13 GMT  
		Size: 167.7 MB (167657828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1942e93305eaea743b2356a9c97cbb8d595727287cd2547b8f547262c6580f16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277882548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99620b3449a66a1c78824144cdc58d4a00d44be71c8cdb14306210274fb273d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:01:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3621d05b6a87c0189a07fccebe13e2ebcc2e4f796eb3d58eafa1fb5e33944`  
		Last Modified: Fri, 02 Feb 2024 01:09:55 GMT  
		Size: 44.7 MB (44678006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b380b750a374075b68fc95d0bd3bd95f94d85c4a57330479476a86a4cde04b44`  
		Last Modified: Fri, 02 Feb 2024 01:10:22 GMT  
		Size: 196.2 MB (196185449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a7d19749bb481ad5541065c62b0a4881ad9b89252590cde9053861628db4a16
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300731725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96838c69cc685d14f8c4373e5231fe9f3f90eec6fe91723b985c25ba4df63905`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:21:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde92598b4fc6ed5837ce31fc6e716b9e9a1bd45de6be16b7e87d47b25abc89d`  
		Last Modified: Fri, 02 Feb 2024 02:34:56 GMT  
		Size: 49.6 MB (49557347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4aeea2ebd03398ad7f6c7ee333e19090f9a9350b436ab5e7aad4054b1109fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:37 GMT  
		Size: 207.2 MB (207245961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2a30f09fe037068f789a9e563fc06224f1ae9a1e23750c733e5e16ded8024f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263265077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d02976377119dd09259576c0bdfeaab86f7199801c54badc12fa3e260660044`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:23:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d23dab9f284ea43a1eedf62d67c328771f3148bdb6b7011b59e1cfecfdfc4c`  
		Last Modified: Fri, 02 Feb 2024 01:35:04 GMT  
		Size: 45.2 MB (45232081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484cc5de2ea16481af607caf41d758862606db6ca976aecdbf31bdc149154235`  
		Last Modified: Fri, 02 Feb 2024 01:35:34 GMT  
		Size: 180.6 MB (180581616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-curl`

```console
$ docker pull buildpack-deps@sha256:8053524d7dfa5adfc2c77a9d238045437f6ff7dd6f96c34acfbbe067727529f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.10-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e12b972188e84b41002773ea27e117b48ad461231fc8951ff4d369bffb2516fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37982461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf40ae89d6804df3257bf478c70fcfa247c71deec7d451375130310d1f3c3f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49f319c50a20049e2369b243ec7af40319d270041a57aa6a1f5d6905683e8ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35173445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b973fd1e304463e4b7bc0331602c4d0ce91b7aee2b4d29d62fd48b08ca49d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4fda16a9a3241c3d059c4b278b1e93346e837be64697820ce6a351a839da963a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37019093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d089d52d87f42a3d35c223dfa42b1db04a61e6f576e94a6cbf3b1d33f34b427c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:93cde881bf128a4e7d9a49257bddb6626bc0ef4bfee2c912d8dcda8322e9e0c1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43928417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da68b730a8fa50ef3eba368dc4058f21c8264ee1bb78781bb7c3656de0018cce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:672f57e8ce41a9854457462a609881bf6a78f98f6afec1441939dff65d7219f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37451380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173781f822b0623706926ec60367b00f7352e2f977bb23b1f21af1780d80878f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-scm`

```console
$ docker pull buildpack-deps@sha256:a280af8b962352f1a0878f316e9f9ec4ce097c018e743f38aac4f2c86de0310f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.10-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:243bdb387568cd69fc6bbbf39ddae9a36a05f2f804a0cc770819b8486a7cdd70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82745141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb0593c144279dfca7eeb415785711a1ef877b3cdd99931cfca9beb5c6060d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30486de06cd814f639bb675162234bd141b86426c87d43f70eb1fbebf35b62`  
		Last Modified: Fri, 02 Feb 2024 06:25:08 GMT  
		Size: 44.8 MB (44762680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff3b10e9e13834203eabf65da442e5e6e7f1dc28079bf6420697ef6d54c6f22d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84123043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373f46ea9f5a4f678582773c3389d39f77fa333db7f4484f1353fc0d60d861ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de61dd38dc0af18a380a823e58045d13cd0b6bf13c269d775509a8a308db69e4`  
		Last Modified: Fri, 02 Feb 2024 00:11:41 GMT  
		Size: 48.9 MB (48949598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30d60af6834b94273aff3692ffe1b4737a398c442d812b60eeb95f68310a6d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81697099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e268880f7f6e31b0b6bd1171277d26005b2e7681f030a28a47fa390e3e4ad709`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3621d05b6a87c0189a07fccebe13e2ebcc2e4f796eb3d58eafa1fb5e33944`  
		Last Modified: Fri, 02 Feb 2024 01:09:55 GMT  
		Size: 44.7 MB (44678006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:66efafb92ffb24be5b1b7b30cf4cd6d0ebfac6688e93b50cf150959fd8f2d2f4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93485764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5d4bd8caa62bca916fc82fc2196e2f5659372e4bf364afa13015117552b0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde92598b4fc6ed5837ce31fc6e716b9e9a1bd45de6be16b7e87d47b25abc89d`  
		Last Modified: Fri, 02 Feb 2024 02:34:56 GMT  
		Size: 49.6 MB (49557347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ef20740de594702ba23b9671b59da991be243890fee65645d06c8e2d794a6f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82683461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6882dfc675d521a8e479f6aae28a958103f516928aae183f69b45bb5861f880a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d23dab9f284ea43a1eedf62d67c328771f3148bdb6b7011b59e1cfecfdfc4c`  
		Last Modified: Fri, 02 Feb 2024 01:35:04 GMT  
		Size: 45.2 MB (45232081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:ff7293459765b8e723d15364fd4b1a768615e0dcf0a189efa89d499164ad4d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:24.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cd5f99addc9b35bb1bd8f13bd0448776d50eee8471018bbfd5d1e5d7f64aa85c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321518288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638dcb861eba582270374268162f21bff618683d074e51c68add0d58cf195c29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:20:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2accc45dfab8442a66b0b0fe52964433bb916c6f2b1bb82fa2b89be9c71044c7`  
		Last Modified: Fri, 02 Feb 2024 06:26:10 GMT  
		Size: 45.4 MB (45392993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a966bfe04bc6248febfb91cd451e07428cd7fdba004cca214fcd0789eb2358d`  
		Last Modified: Fri, 02 Feb 2024 06:26:49 GMT  
		Size: 232.0 MB (232007285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa0bb130944677fedf59a198ccb7adaa49f87ffa5ad3972acac42b8586258b44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276226502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba87b96a8fa9144b6aba6687ad2685b46eb6993268141e6bc72a3d3e37ec5495`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:08:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23569f813ab6f239b230aecd3b3f680f19a5269e8d75eac5b6d08abd958163a8`  
		Last Modified: Fri, 02 Feb 2024 00:12:44 GMT  
		Size: 49.6 MB (49588838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ed75b166e905752a38b944cb766ce6506c1a4818a659a1aa29515dd527221`  
		Last Modified: Fri, 02 Feb 2024 00:13:19 GMT  
		Size: 186.0 MB (186003470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:29955b22dab01fba9b7467ea29c40a0b8c58240fbffb712344eb986779c3b1e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307613225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f95227e6909853cbad2fdb57aacb319fc733da05c963a5a0af2ec9c94b6b0d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:05:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159f43017c60d8344e15f48838483bd0c388de3ec837523fa33997c5abcf747`  
		Last Modified: Fri, 02 Feb 2024 01:10:50 GMT  
		Size: 45.4 MB (45436887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267df88e487b88e75384ac703178a1af2818fb054f8191bacfd9bc268eafb99`  
		Last Modified: Fri, 02 Feb 2024 01:11:21 GMT  
		Size: 219.0 MB (219046980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:897444c368722ae80b6417c1767601868632c91c4c9018177534e8081f886aac
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337000958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bf154156ee040b913e076afdc872fb2a6cad63d41d2cd85d887a7cb1d01c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:29:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba806b1584e9dffae35ccf06c2af9e7cbfd293a0fab95bbaf06abb4786f1004`  
		Last Modified: Fri, 02 Feb 2024 02:36:15 GMT  
		Size: 50.5 MB (50484567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b0c2a9fe073574dc2a6d265f90e7c1947fc1459d1e3d9f09db9af597faff5c`  
		Last Modified: Fri, 02 Feb 2024 02:37:02 GMT  
		Size: 235.4 MB (235378899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22ba22df087f3d536bb0160362250138599e72dd805fe47efaa3cdc9fdd3a2eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302078922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef314acfdcd07bfec6ee6997dd3fe06950037a6a65cb86356bf49db81315235`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:29:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850e1ed4384dfa6da051412846b24fc4182a18620863cd54092878378deef24d`  
		Last Modified: Fri, 02 Feb 2024 01:35:55 GMT  
		Size: 46.9 MB (46863566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00c13f803446bd9774a13fd2849578bf70c1892b6e4afc4fe0056f8a85639eb`  
		Last Modified: Fri, 02 Feb 2024 01:36:27 GMT  
		Size: 210.0 MB (209967342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:2b3d1805d56b7fc5af8861c35b0bc2900ef2cdfd44d1e561ba3a37d870994428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:24.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8589ff9d1dcdce60f1e1ed10e53e47d28c834f465f109453622d7fa57a896537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44118010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543bb3daa613f6d802572d20f1ab3ea165bef6d5856f1dcf2c99a5367aebda1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc36a047bedb9cc2d55e5df5c556fea75120543f367636d278c86916503d230f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40634194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185cd3292d981b14a4a9da76e47837fc33c43a4f484df3f411d01accdf05ea73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3ac3862c3e006742a029ecc60a2324222014ae8acf92a92e864451300f16eb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43129358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20e4cd1f5ca7574d960350c4476a93934e8b200b646786f0b1f5f0a1d2c9f50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fe711c6d187cd2610330c0b96c0f9dec93528cc14f293b933464d372a3a34d9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51137492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db055a19de7e40cf0853a4d278999e4b94b60b10682c6ad3299c116af6dc6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f366059ff359089d1d3b5fa5c8dbb3949f5a860a1145f6f4b9e45e1d2b843a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45248014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eceae813ef2bc4fe810bca45196a3a1dd14a5e691438a470cfca40405e46413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:b81fdade78b8b1e869074cce995fa469e91098620b052116ffd5e447a749e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:24.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6073290ef0f60f574d99cee8ba218b5aba7a28aad18a2479d69b0e25a96bea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89511003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612678d4ea5037c12149c14ef1ebc742351224680e67be24b209970346cc7975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2accc45dfab8442a66b0b0fe52964433bb916c6f2b1bb82fa2b89be9c71044c7`  
		Last Modified: Fri, 02 Feb 2024 06:26:10 GMT  
		Size: 45.4 MB (45392993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fac4169eae6a3f6283eafacaa645e32354bc56bbedc8da044333e32267cd1130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90223032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f565b6c40c58d5dda1e1db5b668136d39e000e914133e327904c544859ddbb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23569f813ab6f239b230aecd3b3f680f19a5269e8d75eac5b6d08abd958163a8`  
		Last Modified: Fri, 02 Feb 2024 00:12:44 GMT  
		Size: 49.6 MB (49588838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:61276946f6f4513a27445e72c96098c78ffe9c710109368316d9e0bc0dce7220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0655810e0ec8369892b7d36859a679a4888cdbf9ec433c61d9d3da88f15332d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159f43017c60d8344e15f48838483bd0c388de3ec837523fa33997c5abcf747`  
		Last Modified: Fri, 02 Feb 2024 01:10:50 GMT  
		Size: 45.4 MB (45436887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5eaa7f8b58b6d2c825bbba41bfbb85982b92b1960ff9459d28c461c6e3122b7a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101622059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48d71384d4a15432f007a06fdfb41ef88f3e52c81e42193a54ca861be9acd51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba806b1584e9dffae35ccf06c2af9e7cbfd293a0fab95bbaf06abb4786f1004`  
		Last Modified: Fri, 02 Feb 2024 02:36:15 GMT  
		Size: 50.5 MB (50484567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75586fcdbd103426a67ed8ba26a9e6adf2e9331c80b6c31075c9927178766d16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92111580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7b796bcb4409b4e58436d933a27a24e749e933c6a5a267d513b6081fc4e5cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850e1ed4384dfa6da051412846b24fc4182a18620863cd54092878378deef24d`  
		Last Modified: Fri, 02 Feb 2024 01:35:55 GMT  
		Size: 46.9 MB (46863566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:9e3ce7993b8428dda197c7ec530e18061f6accd7b86d4f52388bbfe42c5e4647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:11b470007b870840c1ddae1598301138425a02bfcb6e94606df692b18cb19d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348887683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6942018a5eeb2b916ebe577069020324def2fc1f6a1e2f996e2b0a809a66200b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:88d23e11c307a07c9635fa398b67fc58eda44298458c194df9c2656e2c70b99b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316010393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c069f0b96a4229d24f1ad3cdec795d70a4155e4a141c139aaefb9825db909b87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbad25eb5c49c8ee60b2f9c576ab52c62fdeeae27d9d0aff4526469c55fa65ac`  
		Last Modified: Wed, 31 Jan 2024 23:23:36 GMT  
		Size: 184.4 MB (184421840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a7c8aa13ba126aa1c2723857454417cf88132a4347c1b5e783dc0ad875592ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301430253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec32f3afea6849eede5cff0f4ef5574ccdab5e5ea87abce251731c0525cc890`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:48:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1cdffc01f516754cad8e5fa8d07fecb2a259e1cc326b70862c5aac8b4c0bd2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339702501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db35cb2694f9208774e3f5394931d06c113d96ea1bc3492f70b19610e44b5e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4299bb649220caaf79678771b6f57f97122a0a5b638fff83400a663d282b3`  
		Last Modified: Wed, 31 Jan 2024 23:52:55 GMT  
		Size: 202.5 MB (202505949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ceb357d720bd10eb4e41459e0a7200f22c4ae7c2c98fafba5ab38a8794cd2cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351525646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d19a853e590a0d8d4fa7445dd07a20e838ec4456dcaba75bb65515024597aac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff5d662d773fea816c984a59d6fe934f5dcb9f01d11c39e790439b20ef367af`  
		Last Modified: Wed, 31 Jan 2024 23:46:03 GMT  
		Size: 210.0 MB (210044410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dbb112f94135b4ac0cef85207494892d97ccf5e71df1d915fed706ac0dcf5728
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325676100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e5d733a01103e92d4699e5b8181c0318db134e4d97137f22dfb211b6470529`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceaccbccba92f2c5c0591cc9226b540f9fd129c4928fda2a1eb8aef24755a25`  
		Last Modified: Thu, 01 Feb 2024 07:48:29 GMT  
		Size: 189.7 MB (189695618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a751044801caaaa7e8af60fd918851e0c0e2bef038667bcb8f498550d0e4e53a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363005737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217bdf30ac180e034858ebe8b1002b1bab8d0729cfb330a0c4d003166064badd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd5edc8501c8ac210226c299c64633308c37f4d32ef7d6bcea2583f769270f0`  
		Last Modified: Wed, 31 Jan 2024 23:48:41 GMT  
		Size: 214.1 MB (214143709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3299f6d6175a16e9ada5b61388ce37ed2d48173280d1bce5bb5a3926ae2af5b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318265940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768fa3e015aa4d40858057939e5fa0946fefe336135f774e738bbb31333e62fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e9ee69e7f405307aed24012667e5bb90820e6d392951de2b5b22485ac9567c`  
		Last Modified: Thu, 01 Feb 2024 08:19:38 GMT  
		Size: 183.1 MB (183147992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:85dceecbffea2a1345b2d53f225ec2737c9d22c13f78c83b21b7cbc9f10b8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e064d828d70273c083e302828da66195b3721147f7eb94957f7df058225ffe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73633837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32649bda04509e90e0d25dc7631132dfbb0773ba6d0f9df44bb8b112eb79b422`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:47766e6c170b6f34992adbb155234ccbb948a4c76eddb9786eb9bc006a7a3dc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70071181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647c434a3afc4146afdf1aaa8d082b7c4a4a8dc78523484b5aa3735a0f6b830`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83ab84a5761fed44320bcbcc8789f3d61df69b193624275b835a77b827904a67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67131674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857493418b037113f78bbae0db4b9c5bd169fb1fb879a2f1c7a5137fdc72d45b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b6320f387a451d56ed24de068f482ca101443417f7182173b68dcde1481a012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257ef1eb997b67c3eeed724379fc71d410ab8d0ac8a4fed695cdd3f5f815dd26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2863aa66a0e18717cf67132780d887c9b19c2b5e7a4ea466d5ecb07f84f0ec82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75492187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebdcfbb5db46626b6fcb68c413c9433c46213e7d858613fbf3e9f873f4efd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:435e1b7b2fc06704be2d54aef1cc0adcc5b4820af35cc546b4862c7e32a36c00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73012097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdf5cb2ca3c8cb3cd9b395baabe19dfb17c5c726834ef774e69e57c7bb6ad76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b309bd1e112dfbe5160471e6d7b8f72f23dcd191f58cb34c68e30c5ca7241eaa
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79277990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006a50642166fcd8ac6b26e3fa5dd3ab653994bd810b0a044dc030a77af78b2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:abca97a306fb19b12a64d5ed1c27563eaeb6fa8431537c36f686b323c6bdeeda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71987681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfd403e72e9d6e7de9123a3408e9ffdb447e4c1e6a2370029ac9c90ea828d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:6e846e5f2840af6aa4e2e87ceaeba56ed20f97865455ee07b7fe8c0adfd812a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:56a9e212ae7b4c8f20b7b6d7a4e2075bd7c57f317ca7baf425568446dcbbe6f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137776165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d955101e289d2ea22378a567c599e963842716dc4ccf39b9f3c3e7adb5c566b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0d4915e5385e0e4a10735f659960065f06d86d59f698a53edb7ac0860215c441
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131588553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e19192a98b21a3a44e4257b4b97fc09a4883ca90b364aa8002bec03f728bdf4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:67ad6e7de182dc3887341a3938dadfaf3817499ad2e30218ff231869e6ca8450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126348343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa7fdb471c4d800073d0ef453344a60dd2ab73705ec8b2fdd105fc76b6295ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30c712713851a7c0ff40c2fe6aff19d7721d89295783f6438d3dcca44a6e2988
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137196552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf08e6c6a9a9986f40cc51f387c1c50ae6908e66d90e4f50c809b770262cc50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a697f1a5a9e34c909edf5f4f07b31f86d544e140eb072410d7a154b4fa0576df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141481236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4ebf0bf90c254160a7db0d3eff44a5f7e02a67e67115dea0e7972198294970`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5d6b5382a8472ecc176a28cb8f5f745fc4486f15fdf4f6ecf36558d07a0d5e6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135980482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7107096402c2f9cc04117e3dfc42459c62b9d65a57dc9edcf681d9e5b844dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5a75ec265ec0e835e3165570df2b34fa6fc1fe9394eb11204eaf7cf5d9495fb0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148862028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9e8d91d6e6c3e95eefe2ee72505bda600bcc4a4a225f28774c9720d959f4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7679ef21819896af1b7e161004996ddc4837dfede6a8088a704d1d52fb2d10ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135117948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc012ba61bdc533695b9ca828cec50f2da6c0f83569c81bf2dbaa548bf395e31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:c669f9b602dd3b397a7c235929ec56fa73a0a76fdf320aaa84b78fcd96634d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ff2f5f8f1d00e9a9ff9c8d75af372c79ade7859af0b6cf0b7b531331f50fc5b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322321527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7ee515d3f6aa5369e529902877b62e4b634a89c6657032a07de794928e2ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:25:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c200adf1811433c67c208599f5f71578e5237cfd9be60d64045c78282562b77`  
		Last Modified: Wed, 31 Jan 2024 23:34:15 GMT  
		Size: 196.9 MB (196898029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1826b57bdb430d3194cd1c273314a7a7d77929e307578dc8ff11d80472ce5a74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295395101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66373d61fe7eefa45758491e4555bd467f60d31966a352bf584e4cd7dca8b378`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:15:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839390782bb735a0c8ac19a96786946523371bf9a989770a9da6c86ca3583548`  
		Last Modified: Wed, 31 Jan 2024 23:24:12 GMT  
		Size: 52.3 MB (52333517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64c9eccbd5ac6085a2760b6ef04a0140c0bf1633c08d30c4dacf7544003818`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 175.1 MB (175124271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ad13234503438c9db7414897589f3941c39306f33a9b5822142c9bb93c86aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282839577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732c39468113bd9bfad045a7c3efa9fd0936c01af8e7d5cb1cf783540bac160b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bfc3e692e8ff6873d25f44400c58bd3aa6d14344de87d8ad43f17573aaa0cf`  
		Last Modified: Thu, 01 Feb 2024 03:00:28 GMT  
		Size: 167.4 MB (167381508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:be7bf6ba36d3d9037eababb65b039b1b122f1d3924d42dcb7bcaa117732ed580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313993398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85550c7be81feba5e8a3ad3bf8f2a22b73df7b28c9af2fede83d6c7539c344ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890edf75599fe558c8b1705d12a7ed49aca378c73d11ce7f7d9f59e1fc0e6c90`  
		Last Modified: Wed, 31 Jan 2024 23:53:47 GMT  
		Size: 189.8 MB (189834575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dcabfd5baceaa01f25a21569557d69f487a16b216e2e21beebc896544e60ce82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328081251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9641c68245b098d111ea9960147cc2149c54759383f4621885dd90984ffba9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:36:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b16eaec20d2529e6d6598173a9d9d703f940af73aa52ac269cec733301bc178`  
		Last Modified: Wed, 31 Jan 2024 23:47:23 GMT  
		Size: 199.8 MB (199825679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6b4a293434f296ec194a59f51a7831ccbe6ae7eb4d9abdccd4d174152c36f172
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301153138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219f5d00bf2a091ce256ebfb0fa9c516c108092c39eb99b7cbff0884d1accf39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4d84da99a70f6525286e6829101a8ec425b5bf8fa809b85cfa4e246e0467d2`  
		Last Modified: Thu, 01 Feb 2024 07:49:34 GMT  
		Size: 53.3 MB (53312108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47251fd4f095a1e69c5e1a5af220fd6f5b6f01fbe471939335aa5d4c348cb1de`  
		Last Modified: Thu, 01 Feb 2024 07:51:31 GMT  
		Size: 179.0 MB (179021258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f8a8441060856266db9ad5c3c748b41665e1ca68b5f5b1fceba4ab6a5164b65b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330849406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954137c589ac342e2d1f5f6de8e5bf4cd2d958385a2b5eced7fde363b905010c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:35:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c8fee1359a50ceab803cfc7fbcbdb50e8cb467db6a3203354529949ebe118e`  
		Last Modified: Wed, 31 Jan 2024 23:49:53 GMT  
		Size: 196.3 MB (196277517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e9bb947336ad421f4d3cbcc3ce8df0e635cbda9b7b158e582d07dd5f1674a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295932407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837660df51f750f52be907d1e0c2168402b78aa3427f0dfce9fc2a378fce885f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd27dc397984da98ece9a2d55abf511e61b71edc88c38624d78b7fc0cb773f`  
		Last Modified: Thu, 01 Feb 2024 08:20:18 GMT  
		Size: 54.1 MB (54071240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b0db4f23942f60acef6ba1bd97c9d42b0327cd92d6882b65d1dd04594b47d`  
		Last Modified: Thu, 01 Feb 2024 08:20:44 GMT  
		Size: 172.9 MB (172923157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:8a1ded1199439e2893c3a14ed128a8e169656f91cea7f52c6511ea83d3021505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:392b93415c196d43f9ddd296d0bbe2d4c7f86f7bc97152ac57d6f3761bda65e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70821991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0265b8bd33cdcfb398a74547cfea59ef0dc7aa739ef9a00f4036567aa94e68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c7f6bb11f436e693d393da85d06273fab562625dea8201b26171da693eb431bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67937313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac64a2e5e820fcf628e418b44489c0ac390d415f755687eba339ba863c0670d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fcd4d73473056cf3a08cdac96ff5d417e7bbd09e5f5fcb4449f76e81d588a21a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65096824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d426ccd69a9ebe907e821e7d52639a3aa1fab0663476ad9d3b395dbd53fcf9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1817e9539b69c89bc7b6096bcda4e5c05d25127e4a04a8d500a4f4a997ff61cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69458882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd363bc5fbd1e9932c3fa7acf632e1bb544c799135a0bb8bb7e8f99d5e652813`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d7b3ec7b96499c513627851d00f7c1edb6c399f35e8b587fd3481eb4c9c1739c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72315708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00b7da0277fc6430f04cd5cc87fc13eeab6074c1778a20e83226eca901efd99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0fb41bb3ea825897c4cc2183c387cc9b5c83c08fb0b5927956220e246ca57474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68819772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98aa22cfe5d2e5bb9217a416ba9a62b9cd532d93a13ac1aa0f1347e34c42d150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fd015c1f0467981471c9c92bcc21db0a267145b239cb36cec5bd65e5f0a56dfd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75697648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c624aef848904d6e2ac0494e4b4e7ba0d1bafa9ec6ce15c44f771db492d04e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf9624c925ecf104e316f59ddbf6d726328eed693bd9e8fb99689076510de6d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68938010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8a7af5459856b466f61dabe3c72978223aeea47b51d7e25a0177841b44e912`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:8f3be3f794de10c69123d3526372ea978df124eaf4cd0d9d0b535726a780a916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b02b73d47f1b559fb62425ad36cd05c9ea76e29ddc2640842b6287811ff662c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125423498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538099b8d88630c43734871876a2315d37433b167e5bc1ccf7c0e25922ffb9e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:add88c0dcd0e5e9f1a0362d8dbe0a32f5f718b443d5da64fffca4c9fa6d59cd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120270830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c74e95094ea139005ad82d17079dbceedb6973ee3733ecb2b85faa35b39d12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839390782bb735a0c8ac19a96786946523371bf9a989770a9da6c86ca3583548`  
		Last Modified: Wed, 31 Jan 2024 23:24:12 GMT  
		Size: 52.3 MB (52333517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:250f81d5141878ba1b293165b45421783d0167ca65b0bfaec00a1f261360b806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115458069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d070db1b356add0880242ca84a74b07a6faaad05aac1fbfa03792420ddd0c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:526fc255badd59b4c7b2f04ddee7f74a1ff63af674465d67277ad6c9eb9eb4ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124158823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dff516f3f2951e48781c3fc5ce4633db96b1f6d82d698426b5c8096ab84d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e525cd2b30db97cc79f76abbf41b14c3513e239d52b3c769b79baa672e4c927d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128255572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108b13f2ff681a421eb07836625a3d9919e1c93bf26e09d6e47685eab6d49bd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bb667d54c6564a17620ec2f59abc81c795f3cecbe0e80d44d3cc16f08b562bd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122131880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb58a1704f223d0b2045d32bfa0369537f7b9f16bf14f9d24be4e99a26bcbb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4d84da99a70f6525286e6829101a8ec425b5bf8fa809b85cfa4e246e0467d2`  
		Last Modified: Thu, 01 Feb 2024 07:49:34 GMT  
		Size: 53.3 MB (53312108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d93de1e827fc0b79a140cbb9d60bd3d5b56720d51f193a338127ebdc280f6497
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134571889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f53276872229e85f5015573fa7149036a987bec45ddb1a886581741d4ee076`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e71b69e9a5fef3106f3d8cc684a3085a2dc1122e6cd43930cc7baab0cbad7d6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123009250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a021a058355268c8b5e1ba0e193a2e32b2ddecc86bd5e35a53a36ac23bca3322`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd27dc397984da98ece9a2d55abf511e61b71edc88c38624d78b7fc0cb773f`  
		Last Modified: Thu, 01 Feb 2024 08:20:18 GMT  
		Size: 54.1 MB (54071240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:e532accd3fe2c1f4b6876ea510e536c189898be7e335f5f832bf1b4fbc87736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5e70966a1235c65158310892f5bc14bc3428be5637f55dc4676210b6e9559232
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311896884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3573968146e06806800b323fd21a3e7e1bdcbecf6e4a5f41dd654934053c9dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:51 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
# Wed, 31 Jan 2024 22:35:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c933d55a84b39f50891da1a3d93708a40af88018898950d1c1d45287cbceead`  
		Last Modified: Wed, 31 Jan 2024 23:34:41 GMT  
		Size: 51.9 MB (51877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec1650ec847faff4a08d29f1974f9dfb31d13d19f2e8c9f6007fdcb96385356`  
		Last Modified: Wed, 31 Jan 2024 23:35:12 GMT  
		Size: 191.9 MB (191933959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:97db629d0aea9dcffcd95d5fa41e2829f80320f3c98ed6a002688a175768f036
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277727240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d410ef8777ef689bdd6ed35a7585b6965ea5bbe7d305b164a0f8898430c7bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a579a1401e8d8e2a5b42e0da1f30d53451c3736d9a0f2bded6153cd62587c1`  
		Last Modified: Thu, 01 Feb 2024 03:00:57 GMT  
		Size: 47.4 MB (47410558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b7ee9d0c5269d27372fc7c4591d9dc02f7eb8a92f2d856e16b40b8b59f6fa`  
		Last Modified: Thu, 01 Feb 2024 03:01:32 GMT  
		Size: 168.1 MB (168133549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f2d63a27b151d2c55fa8ca1db300cb128dc0f5fa16b7b2dcb3629e2519c29c31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302465626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51686d890f59e8f8f4cc77b93c304cd56b0aa8aaceecce9eaa700296391ea5e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:48 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
# Wed, 31 Jan 2024 22:44:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:47:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516414d0ceb2f3d11662b32d4dca67121887880d8412cd692429221ab8231dc9`  
		Last Modified: Wed, 31 Jan 2024 23:54:13 GMT  
		Size: 52.2 MB (52220919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444d708702c0668e681a5831db2080a8fd839aac855f9d3e3f43562582b0a135`  
		Last Modified: Wed, 31 Jan 2024 23:54:38 GMT  
		Size: 183.5 MB (183499590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:295c3cd010a5da0b8146d4e7df0e0ca74cfca409edd1392dab02ab1012d56b3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321314503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14f40aea61ed44115943bba427cb56e373daa2798f9af3851e0569b551cfa82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:39:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a451225425a788a1d90696a4da55a7cdfdeea108bbe137d9440aa1b08d6b3a`  
		Last Modified: Wed, 31 Jan 2024 23:47:57 GMT  
		Size: 53.5 MB (53490202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9085c739803b4fdaa9dbd79869da8fb43e2788872b548c5aea23661a2d89192`  
		Last Modified: Wed, 31 Jan 2024 23:48:45 GMT  
		Size: 198.5 MB (198469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:fb04e5dff10381413541ea0b9efc7389783d5d9b3af557a24f8f06ea1ebcfc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f23749da9005c1584f973a2214ab3ea6a28f877a24e5c1b84655f47602ddef83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68085529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3430fb008fc146f5a3bf5b33bb9442308dac43c1742e258e8318221357f1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:51 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
# Wed, 31 Jan 2024 22:35:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7629bcdf769df4adb53f7f8ce490c59d26120c4db3b26afc982af6195e7caaa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aded50834613a27916572e410a2100b6802896d74f2c4b1a97cb0f38df5c335`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:98686daa1bc58e51e67e29535938404e2a797afc4f38b4f4b45d8129b80ab696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa4b47f57ce7ffdf8a9dc0290d61a35c066ad505920060d396a4a61e0fe4183`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:48 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
# Wed, 31 Jan 2024 22:44:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8fc58e73ddfa62ea4e49eb4ccbb9233c841ea88733edf92375fb96d25918fec1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b03f4bdbdcc8a85ea581106d588797c61bca55ed891e382735fa10aa78b163`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:7373dda0549d9112cd6d447175ecb5bd503ad911ef83a7f4cd9453e0f5a34813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b5dcc207333bcb56534d1b148f1b63e8b4a231b072444094bf3ce01377794d29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119962925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d764f8d7419e8f58c4e1ae18c2e7a396f0c19b093e0f86c39296fbea99f1095`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:51 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
# Wed, 31 Jan 2024 22:35:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c933d55a84b39f50891da1a3d93708a40af88018898950d1c1d45287cbceead`  
		Last Modified: Wed, 31 Jan 2024 23:34:41 GMT  
		Size: 51.9 MB (51877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bb813b9d3124da27383ff45f6492de797d07f073c38f205536ace4e3b5f28f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109593691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fd9965cf8ab7101c1e6ca04853b5b09981b803c66d9eb7e33f70ab285d531d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a579a1401e8d8e2a5b42e0da1f30d53451c3736d9a0f2bded6153cd62587c1`  
		Last Modified: Thu, 01 Feb 2024 03:00:57 GMT  
		Size: 47.4 MB (47410558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:de66ec215a655e84db155568cd4a976c2d1f9a46dec713193c452e07a0e64a7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118966036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d020046489bd2bc545abe7525d8cb6ca3477a50961b7b029049d7b1cd15aa5b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:48 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
# Wed, 31 Jan 2024 22:44:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516414d0ceb2f3d11662b32d4dca67121887880d8412cd692429221ab8231dc9`  
		Last Modified: Wed, 31 Jan 2024 23:54:13 GMT  
		Size: 52.2 MB (52220919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:955ff07b9c7b66e1ef492837ab533b409aeb8c64108eba75ff5cc4f875b6179f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122844858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26500906b05d1bbcde7a5993c9aeafa91d8d338835c4fb72e0b6061e63b6e4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a451225425a788a1d90696a4da55a7cdfdeea108bbe137d9440aa1b08d6b3a`  
		Last Modified: Wed, 31 Jan 2024 23:47:57 GMT  
		Size: 53.5 MB (53490202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:85dceecbffea2a1345b2d53f225ec2737c9d22c13f78c83b21b7cbc9f10b8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e064d828d70273c083e302828da66195b3721147f7eb94957f7df058225ffe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73633837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32649bda04509e90e0d25dc7631132dfbb0773ba6d0f9df44bb8b112eb79b422`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:47766e6c170b6f34992adbb155234ccbb948a4c76eddb9786eb9bc006a7a3dc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70071181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647c434a3afc4146afdf1aaa8d082b7c4a4a8dc78523484b5aa3735a0f6b830`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83ab84a5761fed44320bcbcc8789f3d61df69b193624275b835a77b827904a67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67131674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857493418b037113f78bbae0db4b9c5bd169fb1fb879a2f1c7a5137fdc72d45b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b6320f387a451d56ed24de068f482ca101443417f7182173b68dcde1481a012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257ef1eb997b67c3eeed724379fc71d410ab8d0ac8a4fed695cdd3f5f815dd26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2863aa66a0e18717cf67132780d887c9b19c2b5e7a4ea466d5ecb07f84f0ec82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75492187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebdcfbb5db46626b6fcb68c413c9433c46213e7d858613fbf3e9f873f4efd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:435e1b7b2fc06704be2d54aef1cc0adcc5b4820af35cc546b4862c7e32a36c00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73012097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdf5cb2ca3c8cb3cd9b395baabe19dfb17c5c726834ef774e69e57c7bb6ad76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b309bd1e112dfbe5160471e6d7b8f72f23dcd191f58cb34c68e30c5ca7241eaa
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79277990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006a50642166fcd8ac6b26e3fa5dd3ab653994bd810b0a044dc030a77af78b2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:abca97a306fb19b12a64d5ed1c27563eaeb6fa8431537c36f686b323c6bdeeda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71987681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfd403e72e9d6e7de9123a3408e9ffdb447e4c1e6a2370029ac9c90ea828d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:57ada2cb624bc8a8b38a36551638108650241a494637ce7f22e9e11c3a1ec709
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
$ docker pull buildpack-deps@sha256:5a099c8c39c1eaacf5f20011a4704b33e9b2f8b5559d7ba453cf616accf90c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245757090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40aa301bba5cdb36c1a9b9f74e15d1db389918958a1dbd9046444b0a638209d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:07:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbac1d6895cea462b85bd61c5b00b59f3b1d16d27b2c7a0a9fb838c4a35ff0b`  
		Last Modified: Fri, 02 Feb 2024 06:22:56 GMT  
		Size: 11.1 MB (11133722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3869ce45a9cfd17d3011945e592fa1799d161adbafd4db9b8bd3659d7965b7`  
		Last Modified: Fri, 02 Feb 2024 06:23:16 GMT  
		Size: 60.9 MB (60904992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997518fc8ff716aa3988c10a05235a0d2f3f09fe4d52e8dd4ea55a266edb2a02`  
		Last Modified: Fri, 02 Feb 2024 06:23:46 GMT  
		Size: 145.1 MB (145133916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06bbef973feb92fd645256eccf79d4ad83b2493d1308ea6fbf33b93175f2e28d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211983832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6baa604c8db1d66316eb9ef3725889845c2fe68d2f5deb855a0ba4a9712ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:54:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996dff6ef7bf273a917daf5f26fdf3ce2a3437a1b88a12d438339cad825fc1a9`  
		Last Modified: Fri, 02 Feb 2024 00:09:47 GMT  
		Size: 55.8 MB (55824821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5faf7a65783ebc0fc71fce330a35048ccfe09acb142df1bcb3449c51e4cc02`  
		Last Modified: Fri, 02 Feb 2024 00:10:15 GMT  
		Size: 122.0 MB (121950628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c8e19ff404d986ed70c9a37728378491351545b1f63dc600b52b67cc7fc56020
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235999243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3577f0f40635ec54c63ace74aa03b9382b74bf2815447d7297fbc2da3158b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb28a40b969d9c86cd7dfd800a5a944b208ada3cd9f8bdef6303362dc2e51a1`  
		Last Modified: Fri, 02 Feb 2024 01:08:15 GMT  
		Size: 61.0 MB (61012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df8ce900192481f0da30214cf0dbf57e840b8842dc245f68513f6afd79e3157`  
		Last Modified: Fri, 02 Feb 2024 01:08:40 GMT  
		Size: 136.8 MB (136796557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d039d78d35643cabe5b2df1832eb9d609fab64344c8d88ea7e8097f4ae67ab8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269529129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c18eda4f812d2fd63ac182480c6a65f39915667de6ffa1ebba948988d9cade`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:05:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c2154c6f7dea8a1736513627d712be0826012c99ae1779a8fc56e36ec1656f`  
		Last Modified: Fri, 02 Feb 2024 02:32:32 GMT  
		Size: 69.7 MB (69653324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e15e3a2cd5f3a2c53f73d28f854d26d6cce5cf8909a67aa711941c4e12f89d`  
		Last Modified: Fri, 02 Feb 2024 02:33:08 GMT  
		Size: 153.6 MB (153618425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ce25d4b95513e23adef005c7fd9686de47217809ddee0313e8cce3f0fdcaa2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226574839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d505195f4353a80806333a66e0853c2c57162ae0f1dab9d7a40034596c00e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:09:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddc6215f51639b9e751c9ce21a6eafd69dfe8cb324818572b591e3eae0d4fd`  
		Last Modified: Fri, 02 Feb 2024 01:33:32 GMT  
		Size: 60.3 MB (60315331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84689abf9543da36ae4ac6e39a52cbc52c219425fe0252a7eb0d2f78b652c9c4`  
		Last Modified: Fri, 02 Feb 2024 01:33:54 GMT  
		Size: 128.6 MB (128550982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:3e2851f3427f9565c91edac93b0811490a271406c9a2a3ff042b3e0567110734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0a9c6806875afe9f9765d9ea59569f4ca1dec6b84a16ce14d8c14ba1c87ba8f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39718182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777f74cc7faef2a986dc8b9606d33163c0559bb36131a3e5e2fd3d1256b2df46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbac1d6895cea462b85bd61c5b00b59f3b1d16d27b2c7a0a9fb838c4a35ff0b`  
		Last Modified: Fri, 02 Feb 2024 06:22:56 GMT  
		Size: 11.1 MB (11133722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:685522e58ec6ac080fc02a78156dcd12188daecb0cad5f08a6ad2dd6e5c88838
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34208383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9a37b0417478012a7e1cb01d43584be8fb25ee1cc7296f500908280d46e96d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e44afef3d570a2192d3a21369eb2bb6a665cb5015ace2749530e118da7652d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38190366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9131606ec55c459b0fadf79f54cd5d5d2ff7c3db99415d06b3565ab6229a3d55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:61052ed4dfde082d89c08baa9ec09ae4a0657be3295a0392419bcd62397180da
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46257380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae9de359f8e0e053ffdfa852899b95a1b022e18388d1a286bace3eb553ecf34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0903e5570edbd18cfda52e5902d2d3ac8d2c1fc537f53cd628c9a2d209929861
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37708526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5780b02f0e91d91ee0d4c75ec0937daed261ddae8291f3c3fbb2e21634146765`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:cf52c4fff4de6fbf141fecccbe168f18d40324a1733ab3f9569594b12d04b939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d5c1357dc17a82fcbf050533276de28eb5348556c1e66b3567c56ab2bf9c5cdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100623174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734a850bee9c779d8a7bbcef1eab90c1dd71dbd13c3c447ba6913d17e92fecc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbac1d6895cea462b85bd61c5b00b59f3b1d16d27b2c7a0a9fb838c4a35ff0b`  
		Last Modified: Fri, 02 Feb 2024 06:22:56 GMT  
		Size: 11.1 MB (11133722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3869ce45a9cfd17d3011945e592fa1799d161adbafd4db9b8bd3659d7965b7`  
		Last Modified: Fri, 02 Feb 2024 06:23:16 GMT  
		Size: 60.9 MB (60904992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7679db02181c821eaf3c9e123ba5bc9f79c65122132d3c12666dbd6c43837e56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90033204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d514200ca52f8623e3fe07018b2558b526a76f8c06dabe134a4651ba501066b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996dff6ef7bf273a917daf5f26fdf3ce2a3437a1b88a12d438339cad825fc1a9`  
		Last Modified: Fri, 02 Feb 2024 00:09:47 GMT  
		Size: 55.8 MB (55824821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:efb0513b800fbbddcab46242de2360dca217dfcca47beb16588e2975453d25c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99202686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cb07a5ca8d12d0d27748239cb61e97c82c2cc3b2f2fa464f0450b55222ce52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb28a40b969d9c86cd7dfd800a5a944b208ada3cd9f8bdef6303362dc2e51a1`  
		Last Modified: Fri, 02 Feb 2024 01:08:15 GMT  
		Size: 61.0 MB (61012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9be807a935c04b3327297d46fb8c6c22f3f4cae154382018718bc613feff81b6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115910704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd40d2021172504c3bd383ce0a1a7ea2adeb61c96998638bce0e293da5b4caea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c2154c6f7dea8a1736513627d712be0826012c99ae1779a8fc56e36ec1656f`  
		Last Modified: Fri, 02 Feb 2024 02:32:32 GMT  
		Size: 69.7 MB (69653324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8046666085765d9bf2050fab2a9cf586f3396073cd2cec9405399dbccfe70b6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98023857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c59508d7157390c04bb299888a57f151ab8c68b8941bc3ed97f9d0ed2e76abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddc6215f51639b9e751c9ce21a6eafd69dfe8cb324818572b591e3eae0d4fd`  
		Last Modified: Fri, 02 Feb 2024 01:33:32 GMT  
		Size: 60.3 MB (60315331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:88ad44a7ede0a5d6f3d8fe80c37ed881e9ef7503f7d2113b7b5c139fefa6129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f8672346b0fb777428615371509403c110627a2d0faf3cfd2718e7537b2545de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250063235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e9d72362a278af11863c18089dadc9da305fd8e8d30db1706cbc04b04b3a67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:12:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9a39c470397903c32405ac6684f74123196728cf153e8f00a4bc25a9ad5fa`  
		Last Modified: Fri, 02 Feb 2024 06:24:10 GMT  
		Size: 39.5 MB (39450166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa202c905468a0a65eec689a73b9f580f6640ff80a02d62ab14b4269fb2daca`  
		Last Modified: Fri, 02 Feb 2024 06:24:42 GMT  
		Size: 173.0 MB (173040419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:56579e6b53540a59b851ba7653982aca23c007a784c94bb6a4aa94df6fbf6d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217314542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc28242d5785ea958aa6a0d4d51726c8367799e7267d65bd22a5035d69700a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:58:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d5022bad6396ad5a6cb649e6d7d08694726302dc3fca7a44c13e3f5ac30d`  
		Last Modified: Fri, 02 Feb 2024 00:10:25 GMT  
		Size: 7.0 MB (7022797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696d12792983d5e91383414e730c71929d81375da8b48757dad5e2c43b79625`  
		Last Modified: Fri, 02 Feb 2024 00:10:40 GMT  
		Size: 42.2 MB (42240510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39d43d0db75bd7b799707677f1dbdb7429fac3fea382e5ff0be946c96ebf6ee`  
		Last Modified: Fri, 02 Feb 2024 00:11:08 GMT  
		Size: 140.5 MB (140524853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe067a914cd3224bb4040ba6ab1bfc2a2f576842cee74c07717fc8725c220318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241353081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1b84b8f8c214cd29f9bc771859efd413aa7095ce18dd1cd58d4fbd226915d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:56:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c57c4e22943bdc69290d3f8794e8a2e6f88492d731e55d42bbab1c04639f6eb`  
		Last Modified: Fri, 02 Feb 2024 01:09:02 GMT  
		Size: 39.4 MB (39365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736ef7ff1a6ba23195fbd71407d2e474032a0f97853d1f46edf2d0d04eb87230`  
		Last Modified: Fri, 02 Feb 2024 01:09:27 GMT  
		Size: 166.5 MB (166517695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:418bbacaab9b7f68449dabbd664df372ddce2e84cb99766e1e4ab6e68333be4f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc534762eb567439ae695adbbe43c770a5d242a22445ff17c8773755b0275f19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:12:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff83656a9f7277ed4028af721dad24c50fa5b1aa50171345db381d06daf43f7d`  
		Last Modified: Fri, 02 Feb 2024 02:33:19 GMT  
		Size: 8.2 MB (8246483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9796e25400f8eaf97eaa611abf40c733cf592de0e724c653064b3b96c416b65`  
		Last Modified: Fri, 02 Feb 2024 02:33:39 GMT  
		Size: 43.8 MB (43763479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1ff09a62e1728a038f10398e632c46d389a2e2eb2c53443a7878b0ff4a8f13`  
		Last Modified: Fri, 02 Feb 2024 02:34:18 GMT  
		Size: 183.7 MB (183699716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:236512f540e7532146f80c458841aff2e94175e89e0d56fcce47e0c47b9b3a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223863647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ddf2f450632e62a7f33c58c50c2e136163b28b3b4f468f9796b1f5195404c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:16:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b25e918744dc60f3fd65aaf829576412d00361b21051000f3822c7226e67`  
		Last Modified: Fri, 02 Feb 2024 01:34:02 GMT  
		Size: 7.0 MB (7038879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ef8c9e80bfa175ac1d1f9cc80ad73756cc4b5510d104e76eab9fb2996f21c9`  
		Last Modified: Fri, 02 Feb 2024 01:34:14 GMT  
		Size: 39.4 MB (39416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5020c9fbfa5f96e33ff00530531a8ecf259cdd21408bda76aa2aa4e9259a77`  
		Last Modified: Fri, 02 Feb 2024 01:34:38 GMT  
		Size: 148.8 MB (148752741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:f70678ffab2d502861bab2a040c7fbcda34f656f65aa5b6d98a8dc41b7b07fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ca247fe943307adbbc89c862972063309df9bdbf3d5a465a729a30bdfb753c34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37572650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99358eaa3f30d6c8bb979a0a8385f0fa6b4030fa5d676c5f7a2f0a512ec4c541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:946fcfa956f0e51964818c238eec222532d4df78c9fbd3c081be301f8dd7c3d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34549179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c919ab35524523d17913d39bc4f2e37bda3ea529c896bb58ae7059176fb227e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d5022bad6396ad5a6cb649e6d7d08694726302dc3fca7a44c13e3f5ac30d`  
		Last Modified: Fri, 02 Feb 2024 00:10:25 GMT  
		Size: 7.0 MB (7022797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bf6a6c222312e0d812ec6b12ea37344464c510d90937183403d7a47287451617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35469714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eecd52d4cc8a99f036d1e08361a520ea21cb5e23e06fe21b6b197503756890b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d5656711867a681e8283ca7af87a5b8b81a1d4fc2972a3db29cc09dd5881360f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43905666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82be83f0500ee8406b164b8a7a0ac3e678ae287321cb584a83cbcc5da3bdf494`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff83656a9f7277ed4028af721dad24c50fa5b1aa50171345db381d06daf43f7d`  
		Last Modified: Fri, 02 Feb 2024 02:33:19 GMT  
		Size: 8.2 MB (8246483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33e671fb304d6abd01cae3fbf077fdd740c71b7308b51b729aefb6bc04fe742a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35694511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa242046750cd4bac13e794163defa6f547b09f3ed3376d579bd6b051d57dee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b25e918744dc60f3fd65aaf829576412d00361b21051000f3822c7226e67`  
		Last Modified: Fri, 02 Feb 2024 01:34:02 GMT  
		Size: 7.0 MB (7038879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:50105ec4dc34351b7aadde13c47544bc99e5de75348393d8e9e2157a402b089e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ac473653eaae3905e8fc87f8ce5a6105e3fbd0b72ecb9d98d766eaa98f66ed7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77022816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edcf3cd0be15910cb39b6eea09069a5b42482c63aa37f4869c25bb2645ff914`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9a39c470397903c32405ac6684f74123196728cf153e8f00a4bc25a9ad5fa`  
		Last Modified: Fri, 02 Feb 2024 06:24:10 GMT  
		Size: 39.5 MB (39450166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e76e7646a6936bec47a21d13b1ff536a43e664b594547ae50a0effdea683070
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76789689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf7cc77eaaf2df12db1f11e199ea41d718543db7e4a7b9ad69179992abfd66c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d5022bad6396ad5a6cb649e6d7d08694726302dc3fca7a44c13e3f5ac30d`  
		Last Modified: Fri, 02 Feb 2024 00:10:25 GMT  
		Size: 7.0 MB (7022797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696d12792983d5e91383414e730c71929d81375da8b48757dad5e2c43b79625`  
		Last Modified: Fri, 02 Feb 2024 00:10:40 GMT  
		Size: 42.2 MB (42240510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d25435931338148a0e89db3840dd6469f1fa180712886e5f399c1d52975ea32f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74835386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408bab5812d49720ec3d1e645690cd2724ce2e6144d8f79ba8d13d2fcffcef78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c57c4e22943bdc69290d3f8794e8a2e6f88492d731e55d42bbab1c04639f6eb`  
		Last Modified: Fri, 02 Feb 2024 01:09:02 GMT  
		Size: 39.4 MB (39365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f3ffe5db9cebbac8cab5b2f958fe769e2f94e52322ba679edca5d08975364ebf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87669145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e272a174802d1005f48c41d236391d05a4749565079f9261edd2985b5864be4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff83656a9f7277ed4028af721dad24c50fa5b1aa50171345db381d06daf43f7d`  
		Last Modified: Fri, 02 Feb 2024 02:33:19 GMT  
		Size: 8.2 MB (8246483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9796e25400f8eaf97eaa611abf40c733cf592de0e724c653064b3b96c416b65`  
		Last Modified: Fri, 02 Feb 2024 02:33:39 GMT  
		Size: 43.8 MB (43763479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a9c84698dc7f4476466493a9e3c4720ee26b4769cb6856ab95c38a12b92aa2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75110906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a2e7d000d01a81ee12b446b2f245c720a8347ea6d2d1ba0c06dea38790e3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b25e918744dc60f3fd65aaf829576412d00361b21051000f3822c7226e67`  
		Last Modified: Fri, 02 Feb 2024 01:34:02 GMT  
		Size: 7.0 MB (7038879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ef8c9e80bfa175ac1d1f9cc80ad73756cc4b5510d104e76eab9fb2996f21c9`  
		Last Modified: Fri, 02 Feb 2024 01:34:14 GMT  
		Size: 39.4 MB (39416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:9e3ce7993b8428dda197c7ec530e18061f6accd7b86d4f52388bbfe42c5e4647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:11b470007b870840c1ddae1598301138425a02bfcb6e94606df692b18cb19d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348887683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6942018a5eeb2b916ebe577069020324def2fc1f6a1e2f996e2b0a809a66200b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:88d23e11c307a07c9635fa398b67fc58eda44298458c194df9c2656e2c70b99b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316010393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c069f0b96a4229d24f1ad3cdec795d70a4155e4a141c139aaefb9825db909b87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbad25eb5c49c8ee60b2f9c576ab52c62fdeeae27d9d0aff4526469c55fa65ac`  
		Last Modified: Wed, 31 Jan 2024 23:23:36 GMT  
		Size: 184.4 MB (184421840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a7c8aa13ba126aa1c2723857454417cf88132a4347c1b5e783dc0ad875592ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301430253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec32f3afea6849eede5cff0f4ef5574ccdab5e5ea87abce251731c0525cc890`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:48:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1cdffc01f516754cad8e5fa8d07fecb2a259e1cc326b70862c5aac8b4c0bd2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339702501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db35cb2694f9208774e3f5394931d06c113d96ea1bc3492f70b19610e44b5e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4299bb649220caaf79678771b6f57f97122a0a5b638fff83400a663d282b3`  
		Last Modified: Wed, 31 Jan 2024 23:52:55 GMT  
		Size: 202.5 MB (202505949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ceb357d720bd10eb4e41459e0a7200f22c4ae7c2c98fafba5ab38a8794cd2cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351525646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d19a853e590a0d8d4fa7445dd07a20e838ec4456dcaba75bb65515024597aac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff5d662d773fea816c984a59d6fe934f5dcb9f01d11c39e790439b20ef367af`  
		Last Modified: Wed, 31 Jan 2024 23:46:03 GMT  
		Size: 210.0 MB (210044410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dbb112f94135b4ac0cef85207494892d97ccf5e71df1d915fed706ac0dcf5728
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325676100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e5d733a01103e92d4699e5b8181c0318db134e4d97137f22dfb211b6470529`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceaccbccba92f2c5c0591cc9226b540f9fd129c4928fda2a1eb8aef24755a25`  
		Last Modified: Thu, 01 Feb 2024 07:48:29 GMT  
		Size: 189.7 MB (189695618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a751044801caaaa7e8af60fd918851e0c0e2bef038667bcb8f498550d0e4e53a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363005737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217bdf30ac180e034858ebe8b1002b1bab8d0729cfb330a0c4d003166064badd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd5edc8501c8ac210226c299c64633308c37f4d32ef7d6bcea2583f769270f0`  
		Last Modified: Wed, 31 Jan 2024 23:48:41 GMT  
		Size: 214.1 MB (214143709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3299f6d6175a16e9ada5b61388ce37ed2d48173280d1bce5bb5a3926ae2af5b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318265940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768fa3e015aa4d40858057939e5fa0946fefe336135f774e738bbb31333e62fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e9ee69e7f405307aed24012667e5bb90820e6d392951de2b5b22485ac9567c`  
		Last Modified: Thu, 01 Feb 2024 08:19:38 GMT  
		Size: 183.1 MB (183147992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:57df129c6a351c0701f07ee4d00dfc5f2b418fc3a7a50a3c9c93d1e20f83dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:138b0bf02a4899e3b87efdb4f41e9d3d01fa24ff3ceb9c612d0016f15ef0aab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286126174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0798d8057dfdea097ea81ae4f17cd1c2186f9f476a67eede7128374babef1d1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30486de06cd814f639bb675162234bd141b86426c87d43f70eb1fbebf35b62`  
		Last Modified: Fri, 02 Feb 2024 06:25:08 GMT  
		Size: 44.8 MB (44762680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda15b28a080849393425aec2c66e4b830a98b42df059a806a1bd37489474050`  
		Last Modified: Fri, 02 Feb 2024 06:25:41 GMT  
		Size: 203.4 MB (203381033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9e92fada45ce7e502258346671cdd635b8e338d204f337e504ce249982ff30c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251780871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d432dc2ec0d255bc1a6621561ec8b8376dbfb0841b040da1d9b597b2db28ee5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:04:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de61dd38dc0af18a380a823e58045d13cd0b6bf13c269d775509a8a308db69e4`  
		Last Modified: Fri, 02 Feb 2024 00:11:41 GMT  
		Size: 48.9 MB (48949598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a3d11b70586440d9ac926dc050ea93411a1239331c430ee195a2ea149045c0`  
		Last Modified: Fri, 02 Feb 2024 00:12:13 GMT  
		Size: 167.7 MB (167657828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1942e93305eaea743b2356a9c97cbb8d595727287cd2547b8f547262c6580f16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277882548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99620b3449a66a1c78824144cdc58d4a00d44be71c8cdb14306210274fb273d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:01:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3621d05b6a87c0189a07fccebe13e2ebcc2e4f796eb3d58eafa1fb5e33944`  
		Last Modified: Fri, 02 Feb 2024 01:09:55 GMT  
		Size: 44.7 MB (44678006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b380b750a374075b68fc95d0bd3bd95f94d85c4a57330479476a86a4cde04b44`  
		Last Modified: Fri, 02 Feb 2024 01:10:22 GMT  
		Size: 196.2 MB (196185449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a7d19749bb481ad5541065c62b0a4881ad9b89252590cde9053861628db4a16
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300731725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96838c69cc685d14f8c4373e5231fe9f3f90eec6fe91723b985c25ba4df63905`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:21:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde92598b4fc6ed5837ce31fc6e716b9e9a1bd45de6be16b7e87d47b25abc89d`  
		Last Modified: Fri, 02 Feb 2024 02:34:56 GMT  
		Size: 49.6 MB (49557347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4aeea2ebd03398ad7f6c7ee333e19090f9a9350b436ab5e7aad4054b1109fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:37 GMT  
		Size: 207.2 MB (207245961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2a30f09fe037068f789a9e563fc06224f1ae9a1e23750c733e5e16ded8024f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263265077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d02976377119dd09259576c0bdfeaab86f7199801c54badc12fa3e260660044`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:23:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d23dab9f284ea43a1eedf62d67c328771f3148bdb6b7011b59e1cfecfdfc4c`  
		Last Modified: Fri, 02 Feb 2024 01:35:04 GMT  
		Size: 45.2 MB (45232081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484cc5de2ea16481af607caf41d758862606db6ca976aecdbf31bdc149154235`  
		Last Modified: Fri, 02 Feb 2024 01:35:34 GMT  
		Size: 180.6 MB (180581616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:8053524d7dfa5adfc2c77a9d238045437f6ff7dd6f96c34acfbbe067727529f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e12b972188e84b41002773ea27e117b48ad461231fc8951ff4d369bffb2516fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37982461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf40ae89d6804df3257bf478c70fcfa247c71deec7d451375130310d1f3c3f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49f319c50a20049e2369b243ec7af40319d270041a57aa6a1f5d6905683e8ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35173445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b973fd1e304463e4b7bc0331602c4d0ce91b7aee2b4d29d62fd48b08ca49d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4fda16a9a3241c3d059c4b278b1e93346e837be64697820ce6a351a839da963a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37019093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d089d52d87f42a3d35c223dfa42b1db04a61e6f576e94a6cbf3b1d33f34b427c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:93cde881bf128a4e7d9a49257bddb6626bc0ef4bfee2c912d8dcda8322e9e0c1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43928417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da68b730a8fa50ef3eba368dc4058f21c8264ee1bb78781bb7c3656de0018cce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:672f57e8ce41a9854457462a609881bf6a78f98f6afec1441939dff65d7219f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37451380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173781f822b0623706926ec60367b00f7352e2f977bb23b1f21af1780d80878f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:a280af8b962352f1a0878f316e9f9ec4ce097c018e743f38aac4f2c86de0310f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:243bdb387568cd69fc6bbbf39ddae9a36a05f2f804a0cc770819b8486a7cdd70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82745141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb0593c144279dfca7eeb415785711a1ef877b3cdd99931cfca9beb5c6060d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30486de06cd814f639bb675162234bd141b86426c87d43f70eb1fbebf35b62`  
		Last Modified: Fri, 02 Feb 2024 06:25:08 GMT  
		Size: 44.8 MB (44762680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff3b10e9e13834203eabf65da442e5e6e7f1dc28079bf6420697ef6d54c6f22d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84123043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373f46ea9f5a4f678582773c3389d39f77fa333db7f4484f1353fc0d60d861ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de61dd38dc0af18a380a823e58045d13cd0b6bf13c269d775509a8a308db69e4`  
		Last Modified: Fri, 02 Feb 2024 00:11:41 GMT  
		Size: 48.9 MB (48949598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30d60af6834b94273aff3692ffe1b4737a398c442d812b60eeb95f68310a6d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81697099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e268880f7f6e31b0b6bd1171277d26005b2e7681f030a28a47fa390e3e4ad709`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3621d05b6a87c0189a07fccebe13e2ebcc2e4f796eb3d58eafa1fb5e33944`  
		Last Modified: Fri, 02 Feb 2024 01:09:55 GMT  
		Size: 44.7 MB (44678006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:66efafb92ffb24be5b1b7b30cf4cd6d0ebfac6688e93b50cf150959fd8f2d2f4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93485764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5d4bd8caa62bca916fc82fc2196e2f5659372e4bf364afa13015117552b0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde92598b4fc6ed5837ce31fc6e716b9e9a1bd45de6be16b7e87d47b25abc89d`  
		Last Modified: Fri, 02 Feb 2024 02:34:56 GMT  
		Size: 49.6 MB (49557347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ef20740de594702ba23b9671b59da991be243890fee65645d06c8e2d794a6f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82683461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6882dfc675d521a8e479f6aae28a958103f516928aae183f69b45bb5861f880a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d23dab9f284ea43a1eedf62d67c328771f3148bdb6b7011b59e1cfecfdfc4c`  
		Last Modified: Fri, 02 Feb 2024 01:35:04 GMT  
		Size: 45.2 MB (45232081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:ff7293459765b8e723d15364fd4b1a768615e0dcf0a189efa89d499164ad4d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cd5f99addc9b35bb1bd8f13bd0448776d50eee8471018bbfd5d1e5d7f64aa85c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321518288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638dcb861eba582270374268162f21bff618683d074e51c68add0d58cf195c29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:20:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2accc45dfab8442a66b0b0fe52964433bb916c6f2b1bb82fa2b89be9c71044c7`  
		Last Modified: Fri, 02 Feb 2024 06:26:10 GMT  
		Size: 45.4 MB (45392993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a966bfe04bc6248febfb91cd451e07428cd7fdba004cca214fcd0789eb2358d`  
		Last Modified: Fri, 02 Feb 2024 06:26:49 GMT  
		Size: 232.0 MB (232007285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa0bb130944677fedf59a198ccb7adaa49f87ffa5ad3972acac42b8586258b44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276226502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba87b96a8fa9144b6aba6687ad2685b46eb6993268141e6bc72a3d3e37ec5495`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:08:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23569f813ab6f239b230aecd3b3f680f19a5269e8d75eac5b6d08abd958163a8`  
		Last Modified: Fri, 02 Feb 2024 00:12:44 GMT  
		Size: 49.6 MB (49588838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ed75b166e905752a38b944cb766ce6506c1a4818a659a1aa29515dd527221`  
		Last Modified: Fri, 02 Feb 2024 00:13:19 GMT  
		Size: 186.0 MB (186003470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:29955b22dab01fba9b7467ea29c40a0b8c58240fbffb712344eb986779c3b1e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307613225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f95227e6909853cbad2fdb57aacb319fc733da05c963a5a0af2ec9c94b6b0d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:05:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159f43017c60d8344e15f48838483bd0c388de3ec837523fa33997c5abcf747`  
		Last Modified: Fri, 02 Feb 2024 01:10:50 GMT  
		Size: 45.4 MB (45436887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267df88e487b88e75384ac703178a1af2818fb054f8191bacfd9bc268eafb99`  
		Last Modified: Fri, 02 Feb 2024 01:11:21 GMT  
		Size: 219.0 MB (219046980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:897444c368722ae80b6417c1767601868632c91c4c9018177534e8081f886aac
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337000958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bf154156ee040b913e076afdc872fb2a6cad63d41d2cd85d887a7cb1d01c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:29:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba806b1584e9dffae35ccf06c2af9e7cbfd293a0fab95bbaf06abb4786f1004`  
		Last Modified: Fri, 02 Feb 2024 02:36:15 GMT  
		Size: 50.5 MB (50484567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b0c2a9fe073574dc2a6d265f90e7c1947fc1459d1e3d9f09db9af597faff5c`  
		Last Modified: Fri, 02 Feb 2024 02:37:02 GMT  
		Size: 235.4 MB (235378899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22ba22df087f3d536bb0160362250138599e72dd805fe47efaa3cdc9fdd3a2eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302078922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef314acfdcd07bfec6ee6997dd3fe06950037a6a65cb86356bf49db81315235`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:29:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850e1ed4384dfa6da051412846b24fc4182a18620863cd54092878378deef24d`  
		Last Modified: Fri, 02 Feb 2024 01:35:55 GMT  
		Size: 46.9 MB (46863566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00c13f803446bd9774a13fd2849578bf70c1892b6e4afc4fe0056f8a85639eb`  
		Last Modified: Fri, 02 Feb 2024 01:36:27 GMT  
		Size: 210.0 MB (209967342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:2b3d1805d56b7fc5af8861c35b0bc2900ef2cdfd44d1e561ba3a37d870994428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8589ff9d1dcdce60f1e1ed10e53e47d28c834f465f109453622d7fa57a896537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44118010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543bb3daa613f6d802572d20f1ab3ea165bef6d5856f1dcf2c99a5367aebda1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc36a047bedb9cc2d55e5df5c556fea75120543f367636d278c86916503d230f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40634194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185cd3292d981b14a4a9da76e47837fc33c43a4f484df3f411d01accdf05ea73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3ac3862c3e006742a029ecc60a2324222014ae8acf92a92e864451300f16eb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43129358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20e4cd1f5ca7574d960350c4476a93934e8b200b646786f0b1f5f0a1d2c9f50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fe711c6d187cd2610330c0b96c0f9dec93528cc14f293b933464d372a3a34d9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51137492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db055a19de7e40cf0853a4d278999e4b94b60b10682c6ad3299c116af6dc6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f366059ff359089d1d3b5fa5c8dbb3949f5a860a1145f6f4b9e45e1d2b843a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45248014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eceae813ef2bc4fe810bca45196a3a1dd14a5e691438a470cfca40405e46413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:b81fdade78b8b1e869074cce995fa469e91098620b052116ffd5e447a749e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6073290ef0f60f574d99cee8ba218b5aba7a28aad18a2479d69b0e25a96bea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89511003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612678d4ea5037c12149c14ef1ebc742351224680e67be24b209970346cc7975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2accc45dfab8442a66b0b0fe52964433bb916c6f2b1bb82fa2b89be9c71044c7`  
		Last Modified: Fri, 02 Feb 2024 06:26:10 GMT  
		Size: 45.4 MB (45392993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fac4169eae6a3f6283eafacaa645e32354bc56bbedc8da044333e32267cd1130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90223032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f565b6c40c58d5dda1e1db5b668136d39e000e914133e327904c544859ddbb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23569f813ab6f239b230aecd3b3f680f19a5269e8d75eac5b6d08abd958163a8`  
		Last Modified: Fri, 02 Feb 2024 00:12:44 GMT  
		Size: 49.6 MB (49588838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:61276946f6f4513a27445e72c96098c78ffe9c710109368316d9e0bc0dce7220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0655810e0ec8369892b7d36859a679a4888cdbf9ec433c61d9d3da88f15332d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159f43017c60d8344e15f48838483bd0c388de3ec837523fa33997c5abcf747`  
		Last Modified: Fri, 02 Feb 2024 01:10:50 GMT  
		Size: 45.4 MB (45436887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5eaa7f8b58b6d2c825bbba41bfbb85982b92b1960ff9459d28c461c6e3122b7a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101622059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48d71384d4a15432f007a06fdfb41ef88f3e52c81e42193a54ca861be9acd51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba806b1584e9dffae35ccf06c2af9e7cbfd293a0fab95bbaf06abb4786f1004`  
		Last Modified: Fri, 02 Feb 2024 02:36:15 GMT  
		Size: 50.5 MB (50484567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75586fcdbd103426a67ed8ba26a9e6adf2e9331c80b6c31075c9927178766d16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92111580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7b796bcb4409b4e58436d933a27a24e749e933c6a5a267d513b6081fc4e5cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850e1ed4384dfa6da051412846b24fc4182a18620863cd54092878378deef24d`  
		Last Modified: Fri, 02 Feb 2024 01:35:55 GMT  
		Size: 46.9 MB (46863566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:e532accd3fe2c1f4b6876ea510e536c189898be7e335f5f832bf1b4fbc87736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5e70966a1235c65158310892f5bc14bc3428be5637f55dc4676210b6e9559232
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311896884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3573968146e06806800b323fd21a3e7e1bdcbecf6e4a5f41dd654934053c9dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:51 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
# Wed, 31 Jan 2024 22:35:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c933d55a84b39f50891da1a3d93708a40af88018898950d1c1d45287cbceead`  
		Last Modified: Wed, 31 Jan 2024 23:34:41 GMT  
		Size: 51.9 MB (51877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec1650ec847faff4a08d29f1974f9dfb31d13d19f2e8c9f6007fdcb96385356`  
		Last Modified: Wed, 31 Jan 2024 23:35:12 GMT  
		Size: 191.9 MB (191933959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:97db629d0aea9dcffcd95d5fa41e2829f80320f3c98ed6a002688a175768f036
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277727240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d410ef8777ef689bdd6ed35a7585b6965ea5bbe7d305b164a0f8898430c7bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a579a1401e8d8e2a5b42e0da1f30d53451c3736d9a0f2bded6153cd62587c1`  
		Last Modified: Thu, 01 Feb 2024 03:00:57 GMT  
		Size: 47.4 MB (47410558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b7ee9d0c5269d27372fc7c4591d9dc02f7eb8a92f2d856e16b40b8b59f6fa`  
		Last Modified: Thu, 01 Feb 2024 03:01:32 GMT  
		Size: 168.1 MB (168133549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f2d63a27b151d2c55fa8ca1db300cb128dc0f5fa16b7b2dcb3629e2519c29c31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302465626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51686d890f59e8f8f4cc77b93c304cd56b0aa8aaceecce9eaa700296391ea5e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:48 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
# Wed, 31 Jan 2024 22:44:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:47:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516414d0ceb2f3d11662b32d4dca67121887880d8412cd692429221ab8231dc9`  
		Last Modified: Wed, 31 Jan 2024 23:54:13 GMT  
		Size: 52.2 MB (52220919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444d708702c0668e681a5831db2080a8fd839aac855f9d3e3f43562582b0a135`  
		Last Modified: Wed, 31 Jan 2024 23:54:38 GMT  
		Size: 183.5 MB (183499590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:295c3cd010a5da0b8146d4e7df0e0ca74cfca409edd1392dab02ab1012d56b3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321314503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14f40aea61ed44115943bba427cb56e373daa2798f9af3851e0569b551cfa82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:39:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a451225425a788a1d90696a4da55a7cdfdeea108bbe137d9440aa1b08d6b3a`  
		Last Modified: Wed, 31 Jan 2024 23:47:57 GMT  
		Size: 53.5 MB (53490202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9085c739803b4fdaa9dbd79869da8fb43e2788872b548c5aea23661a2d89192`  
		Last Modified: Wed, 31 Jan 2024 23:48:45 GMT  
		Size: 198.5 MB (198469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:fb04e5dff10381413541ea0b9efc7389783d5d9b3af557a24f8f06ea1ebcfc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f23749da9005c1584f973a2214ab3ea6a28f877a24e5c1b84655f47602ddef83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68085529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3430fb008fc146f5a3bf5b33bb9442308dac43c1742e258e8318221357f1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:51 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
# Wed, 31 Jan 2024 22:35:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7629bcdf769df4adb53f7f8ce490c59d26120c4db3b26afc982af6195e7caaa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aded50834613a27916572e410a2100b6802896d74f2c4b1a97cb0f38df5c335`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:98686daa1bc58e51e67e29535938404e2a797afc4f38b4f4b45d8129b80ab696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa4b47f57ce7ffdf8a9dc0290d61a35c066ad505920060d396a4a61e0fe4183`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:48 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
# Wed, 31 Jan 2024 22:44:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8fc58e73ddfa62ea4e49eb4ccbb9233c841ea88733edf92375fb96d25918fec1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b03f4bdbdcc8a85ea581106d588797c61bca55ed891e382735fa10aa78b163`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:7373dda0549d9112cd6d447175ecb5bd503ad911ef83a7f4cd9453e0f5a34813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b5dcc207333bcb56534d1b148f1b63e8b4a231b072444094bf3ce01377794d29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119962925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d764f8d7419e8f58c4e1ae18c2e7a396f0c19b093e0f86c39296fbea99f1095`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:51 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
# Wed, 31 Jan 2024 22:35:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c933d55a84b39f50891da1a3d93708a40af88018898950d1c1d45287cbceead`  
		Last Modified: Wed, 31 Jan 2024 23:34:41 GMT  
		Size: 51.9 MB (51877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bb813b9d3124da27383ff45f6492de797d07f073c38f205536ace4e3b5f28f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109593691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fd9965cf8ab7101c1e6ca04853b5b09981b803c66d9eb7e33f70ab285d531d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a579a1401e8d8e2a5b42e0da1f30d53451c3736d9a0f2bded6153cd62587c1`  
		Last Modified: Thu, 01 Feb 2024 03:00:57 GMT  
		Size: 47.4 MB (47410558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:de66ec215a655e84db155568cd4a976c2d1f9a46dec713193c452e07a0e64a7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118966036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d020046489bd2bc545abe7525d8cb6ca3477a50961b7b029049d7b1cd15aa5b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:48 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
# Wed, 31 Jan 2024 22:44:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516414d0ceb2f3d11662b32d4dca67121887880d8412cd692429221ab8231dc9`  
		Last Modified: Wed, 31 Jan 2024 23:54:13 GMT  
		Size: 52.2 MB (52220919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:955ff07b9c7b66e1ef492837ab533b409aeb8c64108eba75ff5cc4f875b6179f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122844858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26500906b05d1bbcde7a5993c9aeafa91d8d338835c4fb72e0b6061e63b6e4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a451225425a788a1d90696a4da55a7cdfdeea108bbe137d9440aa1b08d6b3a`  
		Last Modified: Wed, 31 Jan 2024 23:47:57 GMT  
		Size: 53.5 MB (53490202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:c669f9b602dd3b397a7c235929ec56fa73a0a76fdf320aaa84b78fcd96634d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ff2f5f8f1d00e9a9ff9c8d75af372c79ade7859af0b6cf0b7b531331f50fc5b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322321527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7ee515d3f6aa5369e529902877b62e4b634a89c6657032a07de794928e2ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:25:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c200adf1811433c67c208599f5f71578e5237cfd9be60d64045c78282562b77`  
		Last Modified: Wed, 31 Jan 2024 23:34:15 GMT  
		Size: 196.9 MB (196898029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1826b57bdb430d3194cd1c273314a7a7d77929e307578dc8ff11d80472ce5a74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295395101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66373d61fe7eefa45758491e4555bd467f60d31966a352bf584e4cd7dca8b378`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:15:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839390782bb735a0c8ac19a96786946523371bf9a989770a9da6c86ca3583548`  
		Last Modified: Wed, 31 Jan 2024 23:24:12 GMT  
		Size: 52.3 MB (52333517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64c9eccbd5ac6085a2760b6ef04a0140c0bf1633c08d30c4dacf7544003818`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 175.1 MB (175124271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ad13234503438c9db7414897589f3941c39306f33a9b5822142c9bb93c86aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282839577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732c39468113bd9bfad045a7c3efa9fd0936c01af8e7d5cb1cf783540bac160b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bfc3e692e8ff6873d25f44400c58bd3aa6d14344de87d8ad43f17573aaa0cf`  
		Last Modified: Thu, 01 Feb 2024 03:00:28 GMT  
		Size: 167.4 MB (167381508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:be7bf6ba36d3d9037eababb65b039b1b122f1d3924d42dcb7bcaa117732ed580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313993398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85550c7be81feba5e8a3ad3bf8f2a22b73df7b28c9af2fede83d6c7539c344ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890edf75599fe558c8b1705d12a7ed49aca378c73d11ce7f7d9f59e1fc0e6c90`  
		Last Modified: Wed, 31 Jan 2024 23:53:47 GMT  
		Size: 189.8 MB (189834575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dcabfd5baceaa01f25a21569557d69f487a16b216e2e21beebc896544e60ce82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328081251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9641c68245b098d111ea9960147cc2149c54759383f4621885dd90984ffba9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:36:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b16eaec20d2529e6d6598173a9d9d703f940af73aa52ac269cec733301bc178`  
		Last Modified: Wed, 31 Jan 2024 23:47:23 GMT  
		Size: 199.8 MB (199825679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6b4a293434f296ec194a59f51a7831ccbe6ae7eb4d9abdccd4d174152c36f172
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301153138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219f5d00bf2a091ce256ebfb0fa9c516c108092c39eb99b7cbff0884d1accf39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4d84da99a70f6525286e6829101a8ec425b5bf8fa809b85cfa4e246e0467d2`  
		Last Modified: Thu, 01 Feb 2024 07:49:34 GMT  
		Size: 53.3 MB (53312108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47251fd4f095a1e69c5e1a5af220fd6f5b6f01fbe471939335aa5d4c348cb1de`  
		Last Modified: Thu, 01 Feb 2024 07:51:31 GMT  
		Size: 179.0 MB (179021258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f8a8441060856266db9ad5c3c748b41665e1ca68b5f5b1fceba4ab6a5164b65b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330849406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954137c589ac342e2d1f5f6de8e5bf4cd2d958385a2b5eced7fde363b905010c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:35:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c8fee1359a50ceab803cfc7fbcbdb50e8cb467db6a3203354529949ebe118e`  
		Last Modified: Wed, 31 Jan 2024 23:49:53 GMT  
		Size: 196.3 MB (196277517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e9bb947336ad421f4d3cbcc3ce8df0e635cbda9b7b158e582d07dd5f1674a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295932407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837660df51f750f52be907d1e0c2168402b78aa3427f0dfce9fc2a378fce885f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd27dc397984da98ece9a2d55abf511e61b71edc88c38624d78b7fc0cb773f`  
		Last Modified: Thu, 01 Feb 2024 08:20:18 GMT  
		Size: 54.1 MB (54071240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b0db4f23942f60acef6ba1bd97c9d42b0327cd92d6882b65d1dd04594b47d`  
		Last Modified: Thu, 01 Feb 2024 08:20:44 GMT  
		Size: 172.9 MB (172923157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:8a1ded1199439e2893c3a14ed128a8e169656f91cea7f52c6511ea83d3021505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:392b93415c196d43f9ddd296d0bbe2d4c7f86f7bc97152ac57d6f3761bda65e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70821991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0265b8bd33cdcfb398a74547cfea59ef0dc7aa739ef9a00f4036567aa94e68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c7f6bb11f436e693d393da85d06273fab562625dea8201b26171da693eb431bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67937313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac64a2e5e820fcf628e418b44489c0ac390d415f755687eba339ba863c0670d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fcd4d73473056cf3a08cdac96ff5d417e7bbd09e5f5fcb4449f76e81d588a21a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65096824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d426ccd69a9ebe907e821e7d52639a3aa1fab0663476ad9d3b395dbd53fcf9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1817e9539b69c89bc7b6096bcda4e5c05d25127e4a04a8d500a4f4a997ff61cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69458882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd363bc5fbd1e9932c3fa7acf632e1bb544c799135a0bb8bb7e8f99d5e652813`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d7b3ec7b96499c513627851d00f7c1edb6c399f35e8b587fd3481eb4c9c1739c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72315708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00b7da0277fc6430f04cd5cc87fc13eeab6074c1778a20e83226eca901efd99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0fb41bb3ea825897c4cc2183c387cc9b5c83c08fb0b5927956220e246ca57474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68819772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98aa22cfe5d2e5bb9217a416ba9a62b9cd532d93a13ac1aa0f1347e34c42d150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fd015c1f0467981471c9c92bcc21db0a267145b239cb36cec5bd65e5f0a56dfd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75697648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c624aef848904d6e2ac0494e4b4e7ba0d1bafa9ec6ce15c44f771db492d04e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf9624c925ecf104e316f59ddbf6d726328eed693bd9e8fb99689076510de6d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68938010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8a7af5459856b466f61dabe3c72978223aeea47b51d7e25a0177841b44e912`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:8f3be3f794de10c69123d3526372ea978df124eaf4cd0d9d0b535726a780a916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b02b73d47f1b559fb62425ad36cd05c9ea76e29ddc2640842b6287811ff662c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125423498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538099b8d88630c43734871876a2315d37433b167e5bc1ccf7c0e25922ffb9e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:add88c0dcd0e5e9f1a0362d8dbe0a32f5f718b443d5da64fffca4c9fa6d59cd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120270830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c74e95094ea139005ad82d17079dbceedb6973ee3733ecb2b85faa35b39d12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839390782bb735a0c8ac19a96786946523371bf9a989770a9da6c86ca3583548`  
		Last Modified: Wed, 31 Jan 2024 23:24:12 GMT  
		Size: 52.3 MB (52333517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:250f81d5141878ba1b293165b45421783d0167ca65b0bfaec00a1f261360b806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115458069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d070db1b356add0880242ca84a74b07a6faaad05aac1fbfa03792420ddd0c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:526fc255badd59b4c7b2f04ddee7f74a1ff63af674465d67277ad6c9eb9eb4ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124158823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dff516f3f2951e48781c3fc5ce4633db96b1f6d82d698426b5c8096ab84d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e525cd2b30db97cc79f76abbf41b14c3513e239d52b3c769b79baa672e4c927d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128255572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108b13f2ff681a421eb07836625a3d9919e1c93bf26e09d6e47685eab6d49bd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bb667d54c6564a17620ec2f59abc81c795f3cecbe0e80d44d3cc16f08b562bd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122131880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb58a1704f223d0b2045d32bfa0369537f7b9f16bf14f9d24be4e99a26bcbb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4d84da99a70f6525286e6829101a8ec425b5bf8fa809b85cfa4e246e0467d2`  
		Last Modified: Thu, 01 Feb 2024 07:49:34 GMT  
		Size: 53.3 MB (53312108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d93de1e827fc0b79a140cbb9d60bd3d5b56720d51f193a338127ebdc280f6497
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134571889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f53276872229e85f5015573fa7149036a987bec45ddb1a886581741d4ee076`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e71b69e9a5fef3106f3d8cc684a3085a2dc1122e6cd43930cc7baab0cbad7d6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123009250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a021a058355268c8b5e1ba0e193a2e32b2ddecc86bd5e35a53a36ac23bca3322`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd27dc397984da98ece9a2d55abf511e61b71edc88c38624d78b7fc0cb773f`  
		Last Modified: Thu, 01 Feb 2024 08:20:18 GMT  
		Size: 54.1 MB (54071240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:6e846e5f2840af6aa4e2e87ceaeba56ed20f97865455ee07b7fe8c0adfd812a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:56a9e212ae7b4c8f20b7b6d7a4e2075bd7c57f317ca7baf425568446dcbbe6f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137776165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d955101e289d2ea22378a567c599e963842716dc4ccf39b9f3c3e7adb5c566b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0d4915e5385e0e4a10735f659960065f06d86d59f698a53edb7ac0860215c441
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131588553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e19192a98b21a3a44e4257b4b97fc09a4883ca90b364aa8002bec03f728bdf4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:67ad6e7de182dc3887341a3938dadfaf3817499ad2e30218ff231869e6ca8450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126348343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa7fdb471c4d800073d0ef453344a60dd2ab73705ec8b2fdd105fc76b6295ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30c712713851a7c0ff40c2fe6aff19d7721d89295783f6438d3dcca44a6e2988
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137196552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf08e6c6a9a9986f40cc51f387c1c50ae6908e66d90e4f50c809b770262cc50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a697f1a5a9e34c909edf5f4f07b31f86d544e140eb072410d7a154b4fa0576df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141481236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4ebf0bf90c254160a7db0d3eff44a5f7e02a67e67115dea0e7972198294970`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5d6b5382a8472ecc176a28cb8f5f745fc4486f15fdf4f6ecf36558d07a0d5e6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135980482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7107096402c2f9cc04117e3dfc42459c62b9d65a57dc9edcf681d9e5b844dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5a75ec265ec0e835e3165570df2b34fa6fc1fe9394eb11204eaf7cf5d9495fb0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148862028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9e8d91d6e6c3e95eefe2ee72505bda600bcc4a4a225f28774c9720d959f4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7679ef21819896af1b7e161004996ddc4837dfede6a8088a704d1d52fb2d10ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135117948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc012ba61bdc533695b9ca828cec50f2da6c0f83569c81bf2dbaa548bf395e31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:ed4c3524dee1dc8078b6461660f9fcae37173977a3e46ebb1e39a0867d1902c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:169324d78892d54a26963dd63352e483624df43a66519dc0da809bc5806e36d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411829417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0012ce685aaf6184293aa150c4c0b36deae27bccd0c3e69846c998bea1ad21c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:29:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b5ec6ffb24174c2e8d7b59efdd6b0613b5bcef62a7cde965c456ae6a2b2ea`  
		Last Modified: Wed, 31 Jan 2024 23:35:43 GMT  
		Size: 66.4 MB (66425971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a184e8b47a1727cd21427c2dee2e8a6f3115ef79fef28d35348016479e476b31`  
		Last Modified: Wed, 31 Jan 2024 23:36:25 GMT  
		Size: 268.7 MB (268727614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bbb57464ac66ec70c19c9c2893dbd7a8b0b6a94fc4bef74e85c7902fde9f62d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369083888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9adc5bdb8e634c2ac9e5a8ea25050bdf234804c602643a80739b5d9ffd7248c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:19:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162728a10cded66e397f0df0db68b9dbb11c61c6b79d3baaa731a13664cf8521`  
		Last Modified: Wed, 31 Jan 2024 23:25:18 GMT  
		Size: 64.1 MB (64084887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee4e2f462817b287c66187ea14cd84563505c938a524b8b18f70f4647313ad2`  
		Last Modified: Wed, 31 Jan 2024 23:26:02 GMT  
		Size: 232.4 MB (232354211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d27b106950812dd6e99124eefab26434b4645d2d03dafe55694c6df13aaa7dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352098769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2eccf2ee6c64c1a12e0014aeb302632ce3f5ef3ad7808ab3cc60948217bd51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:53:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:55:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d5c17bde538214384a501538668ef9f5559e9cda83e4b7913d622823ccc1a`  
		Last Modified: Thu, 01 Feb 2024 03:02:04 GMT  
		Size: 61.4 MB (61445900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c2e9b449796e0d1f2fe06bc96516088f81a158362ef93789c88a92cdd7152`  
		Last Modified: Thu, 01 Feb 2024 03:02:46 GMT  
		Size: 221.2 MB (221205326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5cceba7add3138cd5036d039e05b3741b5554a2e75aa358a00178d9dbf07a417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.7 MB (399740160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8ea879302b206dc6cab6a5c13cf1db0ea988bc88c8e90eccb9509beb9ca5ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:49:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2cf8c96bc8d8d3f9a21a0e32a3a2e78e0e214cf8eabcf8557a33907fe41c6`  
		Last Modified: Wed, 31 Jan 2024 23:55:07 GMT  
		Size: 66.5 MB (66539836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5323d8abfd6729b2ec644ba5d2746fefc2b0c082516df2a62c9824abb27a7907`  
		Last Modified: Wed, 31 Jan 2024 23:55:40 GMT  
		Size: 256.9 MB (256947291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6fd5852b23d2806ab37b0fca5e70f5662c9beeb49c025e6f96406e7081d03027
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (408024921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3df00b9ffff249d715ab097ae63eebd1578b53e2c051bb1708252005a0aff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:42:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad4f66a2cd19b6eea3bc0f180db9669dac381b31d1500c7c9b561e5310599f`  
		Last Modified: Wed, 31 Jan 2024 23:49:21 GMT  
		Size: 68.2 MB (68224658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe5a975d38b389f8e13d306a52b282e5e5e79a0ab45543efe60de531f525987`  
		Last Modified: Wed, 31 Jan 2024 23:50:22 GMT  
		Size: 261.2 MB (261157854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e204d973ead7cc9b7c4f1685db5fc42121ecf47cd34db73e9de993b154035b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.8 MB (378776131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a6e7aa6d535e9480ef49a1e45249776e91ec4c3296fed72f685611542c8443`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:35:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bae2c96b6133a9c62aa17246799e040dbce8e2ce06213bc63d1ec7c2e221ca`  
		Last Modified: Thu, 01 Feb 2024 07:52:48 GMT  
		Size: 65.2 MB (65236018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f89ac0febda87ad1ba70e78d3946224343691268ac714ef2f9b1023a6698e`  
		Last Modified: Thu, 01 Feb 2024 07:55:26 GMT  
		Size: 237.3 MB (237328354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:966835a25e3d7a7d337aec37e74a0ecf014ca86ce0c5a1c29fb049d9b1aac163
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423499249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45e81aacf6b190c3e5b7079e99f9b1c8b3b135d2c2799c200df1fa2832393b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:41:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bfff2a14e6e587d4c11641dfff4fc47965b3e5a5be2c00940d05089da4f95`  
		Last Modified: Wed, 31 Jan 2024 23:50:28 GMT  
		Size: 71.9 MB (71937073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c37b376fae9652527604ce30a952fd7e31e1ee0519177a6a9560c684924741`  
		Last Modified: Wed, 31 Jan 2024 23:51:19 GMT  
		Size: 268.9 MB (268883342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cf306643fc52c8ffb549d64ca6cb90dd4d8045a6bb26cfb3ea09670657581f9b
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612f38a8cd5bccb124d6fe189bfe0f9165c382d1ca4c5b1a909ba37e9fee531b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:41:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f8b671531c36b200b6e84dd21a3c784a776685b99bb9638b337cfd52d06fb8`  
		Last Modified: Wed, 31 Jan 2024 22:43:30 GMT  
		Size: 65.7 MB (65693017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fb34953da70cdb0c9a80fb3ba5c765f0a6d96c77f79a0cafcc9dff16dfc62a`  
		Last Modified: Wed, 31 Jan 2024 22:49:25 GMT  
		Size: 300.3 MB (300254507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2e324ae53d9fd5db2018731bbe7fcbcbab4172d4ecaa9a3613e96e61232483cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388238210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005e32576495a2ec040447a36691b99b28f1a28743a3a33fe8a378bdbea58739`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:43:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c0a5ccbf3d4c81b3650225ea3b2d9eae4bd38f2e909a10e6c82117a577b24`  
		Last Modified: Thu, 01 Feb 2024 08:21:22 GMT  
		Size: 67.5 MB (67535565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d73b1c78c6ad532b4f42a143c03c1198813b160bb51460a53290871ac728a68`  
		Last Modified: Thu, 01 Feb 2024 08:21:59 GMT  
		Size: 243.5 MB (243473683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:ff73bf8cd7d96872785619595d038c8e90ab5786e95ca0db16a5c27284f81a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fcd2d9099030515aeb5f83284ea996ae70d3574b8de265661ba1588d8489f94e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76675832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d4f4ca2cb7f034ff1f539af0a06830aa81a5a5e14c3794a84b0555e6c905ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c42c8819f1fa5380b5b5e29f8eeddea27f524d09fbb64332095004705f0460ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72644790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb54c99b149e0581f2727767ac3ce54802736c5425f8c87727e63dbe142a3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:86da99842ef26b82eff6b152da87b23b444361d86d4e7cd96a1d151e750276e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69447543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdeba4944fe5bb9db1d931e3cc152318179a31a7382a4285d42ab8c210832f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bbcba588bae85846e7d7335a4c37d794d121dab50f2eaccf1d778091ef4e6eb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76253033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54f8f75ddf41d7078ffa54e5fbcad654c7c81735fd749c2cea562553fb8bbbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:19d121e6ee2ce272210391657681ae25a7c00d30e41d137892c7790612a10927
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78642409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67d6b14ca1804b8f79826bb27046b3153b9e1ed115fbb9dc111dfc1075d88c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0601797f655badef54dea4e87ffb29a3e9a2a09155df555d06c88ab5b847d341
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76211759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e4ffeaebf0041f02568ffcb40e3a846aa3a0acb73791de9b7af6605ee20780`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1ac4a3ad5d3bf651112f8d660acb7a620a7346ff12038a0ceb051e0de5756051
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82678834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358460f8c89c426b007de7787673a61b110055b4cce49e7dcbe9ee092809d47f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:67f8a76b0939dba6d21780840fb30310d54991ca90634b51cffd416e2d344f96
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74538899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c61be68605628329917168d49371cd583ba1bd6dd4a9ce99295025f2cdd03a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e9c35bf4ff5560030b773a4313e74303ca9abc4f76733b51c2cceab24ed61db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59015da23604a0123e6c648008596096a38231cbd08df796981592e8967ce82a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:b1f26b0b04c18442f48eceed88043658b641d96d0f8b67894fd371e5b1f69ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ecf8dda7f148b5e3929a2b9a784fdbab34a0214c6585b40ad942ba66b1384ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143101803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787eee0a5e2473253978555bf527fbb5fdefbd5b9044a06de57b5431c64e572`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b5ec6ffb24174c2e8d7b59efdd6b0613b5bcef62a7cde965c456ae6a2b2ea`  
		Last Modified: Wed, 31 Jan 2024 23:35:43 GMT  
		Size: 66.4 MB (66425971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fa0a7b3fc115eb7c50fdc121201b0f3cad61bc1aebe5431d723aa89c4276d81a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc1ccb440ba9cfc7dd732a50febaa76de48f748d05f381de5e076f2db2d8311`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162728a10cded66e397f0df0db68b9dbb11c61c6b79d3baaa731a13664cf8521`  
		Last Modified: Wed, 31 Jan 2024 23:25:18 GMT  
		Size: 64.1 MB (64084887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bc770f8215593410866c545b078b6c734690c704829b84e484ac261f8397c17d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130893443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a112abeca93d31b15a585b5d5c6f6b83020c1b10c0e0cfab3638ce8a249c272`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:53:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d5c17bde538214384a501538668ef9f5559e9cda83e4b7913d622823ccc1a`  
		Last Modified: Thu, 01 Feb 2024 03:02:04 GMT  
		Size: 61.4 MB (61445900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e50e6e87ada960fe674558c4c969c3f5c2a4376120151969b5d92b92aa2ed593
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142792869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e52d22551e9b7307d6ecf5f5151565ec72517200d28b1ed52e08dec63b594a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2cf8c96bc8d8d3f9a21a0e32a3a2e78e0e214cf8eabcf8557a33907fe41c6`  
		Last Modified: Wed, 31 Jan 2024 23:55:07 GMT  
		Size: 66.5 MB (66539836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e37db9b541825e0b461db7b1b3152315ff0ababb91262d5a28a073ce368abea0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146867067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b23f42a39184a2d5b358f89bda2622a92bb313cb551fac68e2da13ea220693`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad4f66a2cd19b6eea3bc0f180db9669dac381b31d1500c7c9b561e5310599f`  
		Last Modified: Wed, 31 Jan 2024 23:49:21 GMT  
		Size: 68.2 MB (68224658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fc0825bd389a6489fc62e1ac0b9edc1d57ac46cd5b0c4a6e7e6b5857d473b845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141447777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec64eb59a353b81dcaa6ca4fa3f268d8126a1a2499682b25aab14231ad0d51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bae2c96b6133a9c62aa17246799e040dbce8e2ce06213bc63d1ec7c2e221ca`  
		Last Modified: Thu, 01 Feb 2024 07:52:48 GMT  
		Size: 65.2 MB (65236018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c35af313037569737d47ff9054cd1f7f9bf415d6f8d94534a166f11b0c03fbf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154615907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6077912799958be3a58ab47c99949b783e864b50458ceaea23470245b2608a13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bfff2a14e6e587d4c11641dfff4fc47965b3e5a5be2c00940d05089da4f95`  
		Last Modified: Wed, 31 Jan 2024 23:50:28 GMT  
		Size: 71.9 MB (71937073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ff5d0793ef43078309ca6a97d67d7e0f26961d5f2a58fb16a9288192cd147631
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140231916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dca8ca1f900819fc3fd4311ddfad7e9713941b0ef695be38126286ae0de9f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f8b671531c36b200b6e84dd21a3c784a776685b99bb9638b337cfd52d06fb8`  
		Last Modified: Wed, 31 Jan 2024 22:43:30 GMT  
		Size: 65.7 MB (65693017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f65853fd4f580166d1d03cea84837b87e35ed3cd312174b15a8231df43afbafa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144764527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e4cd715bf0a897de59bb4489f02b586036192e46f18e78aa6439127c639e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c0a5ccbf3d4c81b3650225ea3b2d9eae4bd38f2e909a10e6c82117a577b24`  
		Last Modified: Thu, 01 Feb 2024 08:21:22 GMT  
		Size: 67.5 MB (67535565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:9e3ce7993b8428dda197c7ec530e18061f6accd7b86d4f52388bbfe42c5e4647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:11b470007b870840c1ddae1598301138425a02bfcb6e94606df692b18cb19d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348887683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6942018a5eeb2b916ebe577069020324def2fc1f6a1e2f996e2b0a809a66200b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:88d23e11c307a07c9635fa398b67fc58eda44298458c194df9c2656e2c70b99b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316010393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c069f0b96a4229d24f1ad3cdec795d70a4155e4a141c139aaefb9825db909b87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbad25eb5c49c8ee60b2f9c576ab52c62fdeeae27d9d0aff4526469c55fa65ac`  
		Last Modified: Wed, 31 Jan 2024 23:23:36 GMT  
		Size: 184.4 MB (184421840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a7c8aa13ba126aa1c2723857454417cf88132a4347c1b5e783dc0ad875592ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301430253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec32f3afea6849eede5cff0f4ef5574ccdab5e5ea87abce251731c0525cc890`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:48:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1cdffc01f516754cad8e5fa8d07fecb2a259e1cc326b70862c5aac8b4c0bd2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339702501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db35cb2694f9208774e3f5394931d06c113d96ea1bc3492f70b19610e44b5e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4299bb649220caaf79678771b6f57f97122a0a5b638fff83400a663d282b3`  
		Last Modified: Wed, 31 Jan 2024 23:52:55 GMT  
		Size: 202.5 MB (202505949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ceb357d720bd10eb4e41459e0a7200f22c4ae7c2c98fafba5ab38a8794cd2cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351525646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d19a853e590a0d8d4fa7445dd07a20e838ec4456dcaba75bb65515024597aac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff5d662d773fea816c984a59d6fe934f5dcb9f01d11c39e790439b20ef367af`  
		Last Modified: Wed, 31 Jan 2024 23:46:03 GMT  
		Size: 210.0 MB (210044410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dbb112f94135b4ac0cef85207494892d97ccf5e71df1d915fed706ac0dcf5728
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325676100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e5d733a01103e92d4699e5b8181c0318db134e4d97137f22dfb211b6470529`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceaccbccba92f2c5c0591cc9226b540f9fd129c4928fda2a1eb8aef24755a25`  
		Last Modified: Thu, 01 Feb 2024 07:48:29 GMT  
		Size: 189.7 MB (189695618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a751044801caaaa7e8af60fd918851e0c0e2bef038667bcb8f498550d0e4e53a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363005737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217bdf30ac180e034858ebe8b1002b1bab8d0729cfb330a0c4d003166064badd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd5edc8501c8ac210226c299c64633308c37f4d32ef7d6bcea2583f769270f0`  
		Last Modified: Wed, 31 Jan 2024 23:48:41 GMT  
		Size: 214.1 MB (214143709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3299f6d6175a16e9ada5b61388ce37ed2d48173280d1bce5bb5a3926ae2af5b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318265940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768fa3e015aa4d40858057939e5fa0946fefe336135f774e738bbb31333e62fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e9ee69e7f405307aed24012667e5bb90820e6d392951de2b5b22485ac9567c`  
		Last Modified: Thu, 01 Feb 2024 08:19:38 GMT  
		Size: 183.1 MB (183147992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:85dceecbffea2a1345b2d53f225ec2737c9d22c13f78c83b21b7cbc9f10b8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e064d828d70273c083e302828da66195b3721147f7eb94957f7df058225ffe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73633837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32649bda04509e90e0d25dc7631132dfbb0773ba6d0f9df44bb8b112eb79b422`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:47766e6c170b6f34992adbb155234ccbb948a4c76eddb9786eb9bc006a7a3dc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70071181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647c434a3afc4146afdf1aaa8d082b7c4a4a8dc78523484b5aa3735a0f6b830`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83ab84a5761fed44320bcbcc8789f3d61df69b193624275b835a77b827904a67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67131674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857493418b037113f78bbae0db4b9c5bd169fb1fb879a2f1c7a5137fdc72d45b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b6320f387a451d56ed24de068f482ca101443417f7182173b68dcde1481a012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257ef1eb997b67c3eeed724379fc71d410ab8d0ac8a4fed695cdd3f5f815dd26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2863aa66a0e18717cf67132780d887c9b19c2b5e7a4ea466d5ecb07f84f0ec82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75492187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebdcfbb5db46626b6fcb68c413c9433c46213e7d858613fbf3e9f873f4efd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:435e1b7b2fc06704be2d54aef1cc0adcc5b4820af35cc546b4862c7e32a36c00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73012097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdf5cb2ca3c8cb3cd9b395baabe19dfb17c5c726834ef774e69e57c7bb6ad76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b309bd1e112dfbe5160471e6d7b8f72f23dcd191f58cb34c68e30c5ca7241eaa
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79277990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006a50642166fcd8ac6b26e3fa5dd3ab653994bd810b0a044dc030a77af78b2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:abca97a306fb19b12a64d5ed1c27563eaeb6fa8431537c36f686b323c6bdeeda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71987681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfd403e72e9d6e7de9123a3408e9ffdb447e4c1e6a2370029ac9c90ea828d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:6e846e5f2840af6aa4e2e87ceaeba56ed20f97865455ee07b7fe8c0adfd812a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:56a9e212ae7b4c8f20b7b6d7a4e2075bd7c57f317ca7baf425568446dcbbe6f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137776165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d955101e289d2ea22378a567c599e963842716dc4ccf39b9f3c3e7adb5c566b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0d4915e5385e0e4a10735f659960065f06d86d59f698a53edb7ac0860215c441
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131588553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e19192a98b21a3a44e4257b4b97fc09a4883ca90b364aa8002bec03f728bdf4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:67ad6e7de182dc3887341a3938dadfaf3817499ad2e30218ff231869e6ca8450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126348343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa7fdb471c4d800073d0ef453344a60dd2ab73705ec8b2fdd105fc76b6295ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30c712713851a7c0ff40c2fe6aff19d7721d89295783f6438d3dcca44a6e2988
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137196552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf08e6c6a9a9986f40cc51f387c1c50ae6908e66d90e4f50c809b770262cc50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a697f1a5a9e34c909edf5f4f07b31f86d544e140eb072410d7a154b4fa0576df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141481236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4ebf0bf90c254160a7db0d3eff44a5f7e02a67e67115dea0e7972198294970`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5d6b5382a8472ecc176a28cb8f5f745fc4486f15fdf4f6ecf36558d07a0d5e6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135980482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7107096402c2f9cc04117e3dfc42459c62b9d65a57dc9edcf681d9e5b844dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5a75ec265ec0e835e3165570df2b34fa6fc1fe9394eb11204eaf7cf5d9495fb0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148862028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9e8d91d6e6c3e95eefe2ee72505bda600bcc4a4a225f28774c9720d959f4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7679ef21819896af1b7e161004996ddc4837dfede6a8088a704d1d52fb2d10ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135117948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc012ba61bdc533695b9ca828cec50f2da6c0f83569c81bf2dbaa548bf395e31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:b902087d4e6dc08365debc5c7473cca58b2beeb5b6a02398769cb889dacd7634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea270324fc89bffc8655b18530eaf16c8be105028b541b14fd8e27c3d8c18509
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 MB (406084464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f5e6f7876e6a769bfc4648d373d5b92011e54a6457c200421daccd1e4a0ee0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:02:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b2c7ba7e29214031a9c39d6d5b6571c726fcfdab6f617b8aae44203ea601ea`  
		Last Modified: Fri, 02 Feb 2024 06:22:05 GMT  
		Size: 66.4 MB (66423406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beaa393fc5b0cf30ad7c7983d01a5f0299988e669717a9879a7b05b7a2bd2a`  
		Last Modified: Fri, 02 Feb 2024 06:22:46 GMT  
		Size: 263.0 MB (263037605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e64909db19a56e73d1b3ce133800dd6afdb77355d9e98472b94fa0d463b4c176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367829572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d6f8248127c2d250742b5da26a3d5cf1fc769ca82bb995894b9c41d3589fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:51:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae023c275943af5403b4457371b90865b8075cde3ba18ef56c9dcce109b643a9`  
		Last Modified: Fri, 02 Feb 2024 00:53:11 GMT  
		Size: 64.1 MB (64079789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbc67ab1f5ac10951b154ba7862006f5310f069ce3ec1976ec50d38633bb6a`  
		Last Modified: Fri, 02 Feb 2024 00:54:04 GMT  
		Size: 231.6 MB (231557249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:47ee187d76f9489b091eb1b1a77ff83c3ad5323bf58fc6f270a6985bf8f5487a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343879173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb91b9c52756a00109e626e23382f06182acd4e151d3478584efc666772880`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:28:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945560866c3256a8a40e1abfb8b34b94c6d6f046db32782069e2544c08c8e2e`  
		Last Modified: Fri, 02 Feb 2024 02:30:14 GMT  
		Size: 61.4 MB (61443263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0cf67d92aae40416c3351a4c43a4cf6213b002911b7d09ee0b4686c20da763`  
		Last Modified: Fri, 02 Feb 2024 02:31:00 GMT  
		Size: 213.4 MB (213432585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:215ae05dd29b76b8e018951df5d2e8de5fb11f7285ee3222cc17e078485b843c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386193256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8209ad79eeeb994c392831c0ee634da34495b938ac1ff448464d6e00e44f982`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a766100162b3e4745b3fea6e0c168464cca872d32ac0adb8922d33c224aa3a5`  
		Last Modified: Fri, 02 Feb 2024 01:07:14 GMT  
		Size: 66.5 MB (66537471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf7c421b734f06c61de04526591b6befd47bc6b071c6e6fe381fdb1ad41eaf7`  
		Last Modified: Fri, 02 Feb 2024 01:07:48 GMT  
		Size: 243.9 MB (243897783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2a3d51d6fa62c5809f71d347a615fc6da91c1ba3fad139aac228bb332f158f0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.1 MB (400115296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6540614f2841db8efa796aff98eb4518fbe179cbe1fe49848203f50bb685abd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:41:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44a5c722cd80db8316b102f28c77833949cff82e03df4affc5a5ff9a7005cfe`  
		Last Modified: Fri, 02 Feb 2024 00:42:21 GMT  
		Size: 68.2 MB (68222097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ace9b60f073f6580a56f02847a10adc40b1fa636a055219897cae655993ee5`  
		Last Modified: Fri, 02 Feb 2024 00:43:20 GMT  
		Size: 253.8 MB (253821689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a9127a52341c87d8ef547fb6ad050d83834d6ce150e345bdb4029d8243c15b4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.7 MB (371712191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24a867a30154297a6b4b4c872d62ecca372a17dbe8bb0c3a64c8bca9bc5ea66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:14:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3da179896578bdfa4dfee5627d51e3a213d69a2df22deb29cbc53008828a13`  
		Last Modified: Fri, 02 Feb 2024 01:16:41 GMT  
		Size: 65.2 MB (65235503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bedade2ce97660e9257fc41e4cea8f14e47e33edd244328d9198b8d84451afa`  
		Last Modified: Fri, 02 Feb 2024 01:19:11 GMT  
		Size: 230.9 MB (230864470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:66a8c5be286e23f66fb2ed6fab20cdb3dad12ddd90701e1283ea198bc23fcb65
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.6 MB (408582792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097287d3f5cbe01cc504af055be0c654057ef22919b3da1e054a407996162d39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:57:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24561474467a520bc8085c580cb92087055164baf8702494e9b2e1dc34825ce8`  
		Last Modified: Fri, 02 Feb 2024 02:31:11 GMT  
		Size: 71.9 MB (71935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93e7ca5c80e8f2f02d9ac6b4b4be99c286789f9a34f79d3eda30ad8e96cd16a`  
		Last Modified: Fri, 02 Feb 2024 02:31:59 GMT  
		Size: 254.2 MB (254196302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cba332f9b6a486b056733fba480355cf2ec74e89c99344db631962540078c282
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (373971420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa3ca098cb4eccabb3b3349b1532ed101ec00ffd4fc7395e8ed386548eda31c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:02:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01072c7522404012c43b712d6cf353bb9f279ab8edf997c932c4711b106e26f`  
		Last Modified: Fri, 02 Feb 2024 01:32:32 GMT  
		Size: 67.5 MB (67531843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed432a71247d47fe7a572eeeaa2b8bb341d410ab737f7831698cf32e78d463f1`  
		Last Modified: Fri, 02 Feb 2024 01:33:06 GMT  
		Size: 229.8 MB (229819269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:9676f249efa277d6f658ace6f62655d6e6bd184e8a5ee19cfe40a17f20519919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:84326e327314455c4bab2f12086f2976fad56f95d2c73b0e5dc8287b3d77dd01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76623453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1876ac991c0d94e9d40ec790f81fac9d0192bced604cdcafc921362ff7692364`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1c1112adc813c8c551efa6a9791d7f9a7ad836aad790eb3c79664eafeead7660
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72192534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44dea16c77d1eae9cffc13842c542dd71f840b414ac3889cfc6943cea769cd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:198091b0bb21f5b70c09cfe4c9abf18a0caf90a2711ce5e11b8e0c7cea1df75a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69003325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5893a7a2f2dfaa3342ad12fcf0d5b2993b234942d22d770a6d0bfc8b697f842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9e3db3937a4305ab49d8eda5fd1e314e93e2c0f3ce2b42d445d85d32baa8e37c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75758002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9698bc796186610ee6dee8989c9eb771a9941c97cf3fdaa57fc9aca8f20ea3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6439562975c8cabcfdf34862ddc6d02f6bdcdeb17df571aa406a928d07a0bfec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78071510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc88dafe8aed02987ad83dc9438108f74887677f82061f88ad2551cef6f889af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:21ec5313fd1457ca59dcf375c12cafac4a4611ebe538337b6ff190e04df56ee9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75612218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6255bd7972476b0d526c4d9f9b54ebc1b4dd2ebffc4ff2655ca168442fa16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d59e4fac0b969781c28610b951bf8eb8a57c48d355e11d1b8887e98e8678b4a9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82451067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a4d9065304aed90b2672ecb6051043e0535de87a78930564cc8537b57b87d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac91fe14bc5679daebfd5242044b3ab23d236734ed5b09d91fa090705e8339d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76620308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87c04436a08f3abb6c4a7e54ef408f89b2eef9dc20e929b6a0d56ca34d23f81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:85be88ba10801dc37696f31fc70c7900a3342455cb4c3b8e6a2c3d734576cbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4437f607bdd70ac12aeb352eae79b45c158907c9cb09c41c8dadf4d9c438f71c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143046859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1354b97d51d703463d6249b4b2fb8b9f5f2a6b9b18f3942642e2446700b7e9de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b2c7ba7e29214031a9c39d6d5b6571c726fcfdab6f617b8aae44203ea601ea`  
		Last Modified: Fri, 02 Feb 2024 06:22:05 GMT  
		Size: 66.4 MB (66423406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c2f116c65bed7847f12c604fbc69ccb6a551081dda5c1727ad6daaa87529b91b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136272323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e032cfe9eae809653f7313667aeb21ff1e97bf5cae8acb8f82d458ca43bae66a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae023c275943af5403b4457371b90865b8075cde3ba18ef56c9dcce109b643a9`  
		Last Modified: Fri, 02 Feb 2024 00:53:11 GMT  
		Size: 64.1 MB (64079789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:26f1881770e1a4241bb91647983dfaf5733050b79f85ecb3d63140c7b53a8077
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130446588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b45ee2c2aa82f2df8d8b1530b7ae98a9908f4605bdd2900ca9d974f10778c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945560866c3256a8a40e1abfb8b34b94c6d6f046db32782069e2544c08c8e2e`  
		Last Modified: Fri, 02 Feb 2024 02:30:14 GMT  
		Size: 61.4 MB (61443263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e63139846865bc42cc3e349db609fbee01c231cb2b1745073e20279a6e34c899
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142295473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2075f8036ab5bca069ff4d296bf195866a167ee4c2a45123e1050acf3dd94f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a766100162b3e4745b3fea6e0c168464cca872d32ac0adb8922d33c224aa3a5`  
		Last Modified: Fri, 02 Feb 2024 01:07:14 GMT  
		Size: 66.5 MB (66537471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:85621da6d689ed0f1fd70768ea8d6d8a4db2d4697ebe6525b62cbac32c7dfda1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146293607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed0866095f22be5cb6d8f3992a9d0e02140719519dcd899a2e502aa15898896`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44a5c722cd80db8316b102f28c77833949cff82e03df4affc5a5ff9a7005cfe`  
		Last Modified: Fri, 02 Feb 2024 00:42:21 GMT  
		Size: 68.2 MB (68222097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:66abc3eee181e8c57427b58b0b93fb1c2b70d3193627e7ff860b6d03ce275542
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140847721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152a707744b6ab3f3a3a1282707dffb63243e86bc958541547065da96a7b329`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3da179896578bdfa4dfee5627d51e3a213d69a2df22deb29cbc53008828a13`  
		Last Modified: Fri, 02 Feb 2024 01:16:41 GMT  
		Size: 65.2 MB (65235503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d77ae466a3b63ce78c37e94a45ecdcbf0785f1a3ce276e6b3514233624afb230
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154386490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e1b98ec2c42050bd63cf0ec1b4520c25cb528c265b8831e4c2e1207d639f3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24561474467a520bc8085c580cb92087055164baf8702494e9b2e1dc34825ce8`  
		Last Modified: Fri, 02 Feb 2024 02:31:11 GMT  
		Size: 71.9 MB (71935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f28588b7a81835756634c70de1a870936cde45a630684a746864673356f3fc11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144152151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba6a20a7a071749a1c4f613c122eabbff3d1ea79cd3d9ac1df343bf7575fc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01072c7522404012c43b712d6cf353bb9f279ab8edf997c932c4711b106e26f`  
		Last Modified: Fri, 02 Feb 2024 01:32:32 GMT  
		Size: 67.5 MB (67531843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:b902087d4e6dc08365debc5c7473cca58b2beeb5b6a02398769cb889dacd7634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea270324fc89bffc8655b18530eaf16c8be105028b541b14fd8e27c3d8c18509
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 MB (406084464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f5e6f7876e6a769bfc4648d373d5b92011e54a6457c200421daccd1e4a0ee0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:02:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b2c7ba7e29214031a9c39d6d5b6571c726fcfdab6f617b8aae44203ea601ea`  
		Last Modified: Fri, 02 Feb 2024 06:22:05 GMT  
		Size: 66.4 MB (66423406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beaa393fc5b0cf30ad7c7983d01a5f0299988e669717a9879a7b05b7a2bd2a`  
		Last Modified: Fri, 02 Feb 2024 06:22:46 GMT  
		Size: 263.0 MB (263037605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e64909db19a56e73d1b3ce133800dd6afdb77355d9e98472b94fa0d463b4c176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367829572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d6f8248127c2d250742b5da26a3d5cf1fc769ca82bb995894b9c41d3589fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:51:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae023c275943af5403b4457371b90865b8075cde3ba18ef56c9dcce109b643a9`  
		Last Modified: Fri, 02 Feb 2024 00:53:11 GMT  
		Size: 64.1 MB (64079789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbc67ab1f5ac10951b154ba7862006f5310f069ce3ec1976ec50d38633bb6a`  
		Last Modified: Fri, 02 Feb 2024 00:54:04 GMT  
		Size: 231.6 MB (231557249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:47ee187d76f9489b091eb1b1a77ff83c3ad5323bf58fc6f270a6985bf8f5487a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343879173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb91b9c52756a00109e626e23382f06182acd4e151d3478584efc666772880`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:28:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945560866c3256a8a40e1abfb8b34b94c6d6f046db32782069e2544c08c8e2e`  
		Last Modified: Fri, 02 Feb 2024 02:30:14 GMT  
		Size: 61.4 MB (61443263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0cf67d92aae40416c3351a4c43a4cf6213b002911b7d09ee0b4686c20da763`  
		Last Modified: Fri, 02 Feb 2024 02:31:00 GMT  
		Size: 213.4 MB (213432585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:215ae05dd29b76b8e018951df5d2e8de5fb11f7285ee3222cc17e078485b843c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386193256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8209ad79eeeb994c392831c0ee634da34495b938ac1ff448464d6e00e44f982`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a766100162b3e4745b3fea6e0c168464cca872d32ac0adb8922d33c224aa3a5`  
		Last Modified: Fri, 02 Feb 2024 01:07:14 GMT  
		Size: 66.5 MB (66537471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf7c421b734f06c61de04526591b6befd47bc6b071c6e6fe381fdb1ad41eaf7`  
		Last Modified: Fri, 02 Feb 2024 01:07:48 GMT  
		Size: 243.9 MB (243897783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2a3d51d6fa62c5809f71d347a615fc6da91c1ba3fad139aac228bb332f158f0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.1 MB (400115296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6540614f2841db8efa796aff98eb4518fbe179cbe1fe49848203f50bb685abd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:41:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44a5c722cd80db8316b102f28c77833949cff82e03df4affc5a5ff9a7005cfe`  
		Last Modified: Fri, 02 Feb 2024 00:42:21 GMT  
		Size: 68.2 MB (68222097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ace9b60f073f6580a56f02847a10adc40b1fa636a055219897cae655993ee5`  
		Last Modified: Fri, 02 Feb 2024 00:43:20 GMT  
		Size: 253.8 MB (253821689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a9127a52341c87d8ef547fb6ad050d83834d6ce150e345bdb4029d8243c15b4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.7 MB (371712191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24a867a30154297a6b4b4c872d62ecca372a17dbe8bb0c3a64c8bca9bc5ea66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:14:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3da179896578bdfa4dfee5627d51e3a213d69a2df22deb29cbc53008828a13`  
		Last Modified: Fri, 02 Feb 2024 01:16:41 GMT  
		Size: 65.2 MB (65235503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bedade2ce97660e9257fc41e4cea8f14e47e33edd244328d9198b8d84451afa`  
		Last Modified: Fri, 02 Feb 2024 01:19:11 GMT  
		Size: 230.9 MB (230864470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:66a8c5be286e23f66fb2ed6fab20cdb3dad12ddd90701e1283ea198bc23fcb65
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.6 MB (408582792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097287d3f5cbe01cc504af055be0c654057ef22919b3da1e054a407996162d39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:57:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24561474467a520bc8085c580cb92087055164baf8702494e9b2e1dc34825ce8`  
		Last Modified: Fri, 02 Feb 2024 02:31:11 GMT  
		Size: 71.9 MB (71935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93e7ca5c80e8f2f02d9ac6b4b4be99c286789f9a34f79d3eda30ad8e96cd16a`  
		Last Modified: Fri, 02 Feb 2024 02:31:59 GMT  
		Size: 254.2 MB (254196302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cba332f9b6a486b056733fba480355cf2ec74e89c99344db631962540078c282
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (373971420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa3ca098cb4eccabb3b3349b1532ed101ec00ffd4fc7395e8ed386548eda31c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:02:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01072c7522404012c43b712d6cf353bb9f279ab8edf997c932c4711b106e26f`  
		Last Modified: Fri, 02 Feb 2024 01:32:32 GMT  
		Size: 67.5 MB (67531843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed432a71247d47fe7a572eeeaa2b8bb341d410ab737f7831698cf32e78d463f1`  
		Last Modified: Fri, 02 Feb 2024 01:33:06 GMT  
		Size: 229.8 MB (229819269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:9676f249efa277d6f658ace6f62655d6e6bd184e8a5ee19cfe40a17f20519919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:84326e327314455c4bab2f12086f2976fad56f95d2c73b0e5dc8287b3d77dd01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76623453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1876ac991c0d94e9d40ec790f81fac9d0192bced604cdcafc921362ff7692364`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1c1112adc813c8c551efa6a9791d7f9a7ad836aad790eb3c79664eafeead7660
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72192534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44dea16c77d1eae9cffc13842c542dd71f840b414ac3889cfc6943cea769cd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:198091b0bb21f5b70c09cfe4c9abf18a0caf90a2711ce5e11b8e0c7cea1df75a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69003325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5893a7a2f2dfaa3342ad12fcf0d5b2993b234942d22d770a6d0bfc8b697f842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9e3db3937a4305ab49d8eda5fd1e314e93e2c0f3ce2b42d445d85d32baa8e37c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75758002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9698bc796186610ee6dee8989c9eb771a9941c97cf3fdaa57fc9aca8f20ea3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6439562975c8cabcfdf34862ddc6d02f6bdcdeb17df571aa406a928d07a0bfec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78071510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc88dafe8aed02987ad83dc9438108f74887677f82061f88ad2551cef6f889af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:21ec5313fd1457ca59dcf375c12cafac4a4611ebe538337b6ff190e04df56ee9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75612218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6255bd7972476b0d526c4d9f9b54ebc1b4dd2ebffc4ff2655ca168442fa16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d59e4fac0b969781c28610b951bf8eb8a57c48d355e11d1b8887e98e8678b4a9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82451067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a4d9065304aed90b2672ecb6051043e0535de87a78930564cc8537b57b87d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac91fe14bc5679daebfd5242044b3ab23d236734ed5b09d91fa090705e8339d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76620308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87c04436a08f3abb6c4a7e54ef408f89b2eef9dc20e929b6a0d56ca34d23f81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:85be88ba10801dc37696f31fc70c7900a3342455cb4c3b8e6a2c3d734576cbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4437f607bdd70ac12aeb352eae79b45c158907c9cb09c41c8dadf4d9c438f71c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143046859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1354b97d51d703463d6249b4b2fb8b9f5f2a6b9b18f3942642e2446700b7e9de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b2c7ba7e29214031a9c39d6d5b6571c726fcfdab6f617b8aae44203ea601ea`  
		Last Modified: Fri, 02 Feb 2024 06:22:05 GMT  
		Size: 66.4 MB (66423406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c2f116c65bed7847f12c604fbc69ccb6a551081dda5c1727ad6daaa87529b91b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136272323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e032cfe9eae809653f7313667aeb21ff1e97bf5cae8acb8f82d458ca43bae66a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae023c275943af5403b4457371b90865b8075cde3ba18ef56c9dcce109b643a9`  
		Last Modified: Fri, 02 Feb 2024 00:53:11 GMT  
		Size: 64.1 MB (64079789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:26f1881770e1a4241bb91647983dfaf5733050b79f85ecb3d63140c7b53a8077
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130446588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b45ee2c2aa82f2df8d8b1530b7ae98a9908f4605bdd2900ca9d974f10778c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945560866c3256a8a40e1abfb8b34b94c6d6f046db32782069e2544c08c8e2e`  
		Last Modified: Fri, 02 Feb 2024 02:30:14 GMT  
		Size: 61.4 MB (61443263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e63139846865bc42cc3e349db609fbee01c231cb2b1745073e20279a6e34c899
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142295473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2075f8036ab5bca069ff4d296bf195866a167ee4c2a45123e1050acf3dd94f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a766100162b3e4745b3fea6e0c168464cca872d32ac0adb8922d33c224aa3a5`  
		Last Modified: Fri, 02 Feb 2024 01:07:14 GMT  
		Size: 66.5 MB (66537471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:85621da6d689ed0f1fd70768ea8d6d8a4db2d4697ebe6525b62cbac32c7dfda1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146293607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed0866095f22be5cb6d8f3992a9d0e02140719519dcd899a2e502aa15898896`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44a5c722cd80db8316b102f28c77833949cff82e03df4affc5a5ff9a7005cfe`  
		Last Modified: Fri, 02 Feb 2024 00:42:21 GMT  
		Size: 68.2 MB (68222097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:66abc3eee181e8c57427b58b0b93fb1c2b70d3193627e7ff860b6d03ce275542
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140847721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152a707744b6ab3f3a3a1282707dffb63243e86bc958541547065da96a7b329`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3da179896578bdfa4dfee5627d51e3a213d69a2df22deb29cbc53008828a13`  
		Last Modified: Fri, 02 Feb 2024 01:16:41 GMT  
		Size: 65.2 MB (65235503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d77ae466a3b63ce78c37e94a45ecdcbf0785f1a3ce276e6b3514233624afb230
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154386490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e1b98ec2c42050bd63cf0ec1b4520c25cb528c265b8831e4c2e1207d639f3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24561474467a520bc8085c580cb92087055164baf8702494e9b2e1dc34825ce8`  
		Last Modified: Fri, 02 Feb 2024 02:31:11 GMT  
		Size: 71.9 MB (71935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f28588b7a81835756634c70de1a870936cde45a630684a746864673356f3fc11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144152151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba6a20a7a071749a1c4f613c122eabbff3d1ea79cd3d9ac1df343bf7575fc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01072c7522404012c43b712d6cf353bb9f279ab8edf997c932c4711b106e26f`  
		Last Modified: Fri, 02 Feb 2024 01:32:32 GMT  
		Size: 67.5 MB (67531843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:ed4c3524dee1dc8078b6461660f9fcae37173977a3e46ebb1e39a0867d1902c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:169324d78892d54a26963dd63352e483624df43a66519dc0da809bc5806e36d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411829417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0012ce685aaf6184293aa150c4c0b36deae27bccd0c3e69846c998bea1ad21c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:29:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b5ec6ffb24174c2e8d7b59efdd6b0613b5bcef62a7cde965c456ae6a2b2ea`  
		Last Modified: Wed, 31 Jan 2024 23:35:43 GMT  
		Size: 66.4 MB (66425971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a184e8b47a1727cd21427c2dee2e8a6f3115ef79fef28d35348016479e476b31`  
		Last Modified: Wed, 31 Jan 2024 23:36:25 GMT  
		Size: 268.7 MB (268727614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bbb57464ac66ec70c19c9c2893dbd7a8b0b6a94fc4bef74e85c7902fde9f62d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369083888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9adc5bdb8e634c2ac9e5a8ea25050bdf234804c602643a80739b5d9ffd7248c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:19:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162728a10cded66e397f0df0db68b9dbb11c61c6b79d3baaa731a13664cf8521`  
		Last Modified: Wed, 31 Jan 2024 23:25:18 GMT  
		Size: 64.1 MB (64084887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee4e2f462817b287c66187ea14cd84563505c938a524b8b18f70f4647313ad2`  
		Last Modified: Wed, 31 Jan 2024 23:26:02 GMT  
		Size: 232.4 MB (232354211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d27b106950812dd6e99124eefab26434b4645d2d03dafe55694c6df13aaa7dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352098769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2eccf2ee6c64c1a12e0014aeb302632ce3f5ef3ad7808ab3cc60948217bd51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:53:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:55:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d5c17bde538214384a501538668ef9f5559e9cda83e4b7913d622823ccc1a`  
		Last Modified: Thu, 01 Feb 2024 03:02:04 GMT  
		Size: 61.4 MB (61445900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c2e9b449796e0d1f2fe06bc96516088f81a158362ef93789c88a92cdd7152`  
		Last Modified: Thu, 01 Feb 2024 03:02:46 GMT  
		Size: 221.2 MB (221205326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5cceba7add3138cd5036d039e05b3741b5554a2e75aa358a00178d9dbf07a417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.7 MB (399740160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8ea879302b206dc6cab6a5c13cf1db0ea988bc88c8e90eccb9509beb9ca5ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:49:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2cf8c96bc8d8d3f9a21a0e32a3a2e78e0e214cf8eabcf8557a33907fe41c6`  
		Last Modified: Wed, 31 Jan 2024 23:55:07 GMT  
		Size: 66.5 MB (66539836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5323d8abfd6729b2ec644ba5d2746fefc2b0c082516df2a62c9824abb27a7907`  
		Last Modified: Wed, 31 Jan 2024 23:55:40 GMT  
		Size: 256.9 MB (256947291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6fd5852b23d2806ab37b0fca5e70f5662c9beeb49c025e6f96406e7081d03027
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (408024921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3df00b9ffff249d715ab097ae63eebd1578b53e2c051bb1708252005a0aff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:42:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad4f66a2cd19b6eea3bc0f180db9669dac381b31d1500c7c9b561e5310599f`  
		Last Modified: Wed, 31 Jan 2024 23:49:21 GMT  
		Size: 68.2 MB (68224658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe5a975d38b389f8e13d306a52b282e5e5e79a0ab45543efe60de531f525987`  
		Last Modified: Wed, 31 Jan 2024 23:50:22 GMT  
		Size: 261.2 MB (261157854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e204d973ead7cc9b7c4f1685db5fc42121ecf47cd34db73e9de993b154035b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.8 MB (378776131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a6e7aa6d535e9480ef49a1e45249776e91ec4c3296fed72f685611542c8443`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:35:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bae2c96b6133a9c62aa17246799e040dbce8e2ce06213bc63d1ec7c2e221ca`  
		Last Modified: Thu, 01 Feb 2024 07:52:48 GMT  
		Size: 65.2 MB (65236018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f89ac0febda87ad1ba70e78d3946224343691268ac714ef2f9b1023a6698e`  
		Last Modified: Thu, 01 Feb 2024 07:55:26 GMT  
		Size: 237.3 MB (237328354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:966835a25e3d7a7d337aec37e74a0ecf014ca86ce0c5a1c29fb049d9b1aac163
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423499249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45e81aacf6b190c3e5b7079e99f9b1c8b3b135d2c2799c200df1fa2832393b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:41:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bfff2a14e6e587d4c11641dfff4fc47965b3e5a5be2c00940d05089da4f95`  
		Last Modified: Wed, 31 Jan 2024 23:50:28 GMT  
		Size: 71.9 MB (71937073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c37b376fae9652527604ce30a952fd7e31e1ee0519177a6a9560c684924741`  
		Last Modified: Wed, 31 Jan 2024 23:51:19 GMT  
		Size: 268.9 MB (268883342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cf306643fc52c8ffb549d64ca6cb90dd4d8045a6bb26cfb3ea09670657581f9b
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612f38a8cd5bccb124d6fe189bfe0f9165c382d1ca4c5b1a909ba37e9fee531b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:41:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f8b671531c36b200b6e84dd21a3c784a776685b99bb9638b337cfd52d06fb8`  
		Last Modified: Wed, 31 Jan 2024 22:43:30 GMT  
		Size: 65.7 MB (65693017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fb34953da70cdb0c9a80fb3ba5c765f0a6d96c77f79a0cafcc9dff16dfc62a`  
		Last Modified: Wed, 31 Jan 2024 22:49:25 GMT  
		Size: 300.3 MB (300254507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2e324ae53d9fd5db2018731bbe7fcbcbab4172d4ecaa9a3613e96e61232483cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388238210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005e32576495a2ec040447a36691b99b28f1a28743a3a33fe8a378bdbea58739`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:43:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c0a5ccbf3d4c81b3650225ea3b2d9eae4bd38f2e909a10e6c82117a577b24`  
		Last Modified: Thu, 01 Feb 2024 08:21:22 GMT  
		Size: 67.5 MB (67535565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d73b1c78c6ad532b4f42a143c03c1198813b160bb51460a53290871ac728a68`  
		Last Modified: Thu, 01 Feb 2024 08:21:59 GMT  
		Size: 243.5 MB (243473683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:ff73bf8cd7d96872785619595d038c8e90ab5786e95ca0db16a5c27284f81a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fcd2d9099030515aeb5f83284ea996ae70d3574b8de265661ba1588d8489f94e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76675832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d4f4ca2cb7f034ff1f539af0a06830aa81a5a5e14c3794a84b0555e6c905ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c42c8819f1fa5380b5b5e29f8eeddea27f524d09fbb64332095004705f0460ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72644790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb54c99b149e0581f2727767ac3ce54802736c5425f8c87727e63dbe142a3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:86da99842ef26b82eff6b152da87b23b444361d86d4e7cd96a1d151e750276e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69447543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdeba4944fe5bb9db1d931e3cc152318179a31a7382a4285d42ab8c210832f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bbcba588bae85846e7d7335a4c37d794d121dab50f2eaccf1d778091ef4e6eb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76253033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54f8f75ddf41d7078ffa54e5fbcad654c7c81735fd749c2cea562553fb8bbbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:19d121e6ee2ce272210391657681ae25a7c00d30e41d137892c7790612a10927
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78642409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67d6b14ca1804b8f79826bb27046b3153b9e1ed115fbb9dc111dfc1075d88c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0601797f655badef54dea4e87ffb29a3e9a2a09155df555d06c88ab5b847d341
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76211759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e4ffeaebf0041f02568ffcb40e3a846aa3a0acb73791de9b7af6605ee20780`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1ac4a3ad5d3bf651112f8d660acb7a620a7346ff12038a0ceb051e0de5756051
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82678834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358460f8c89c426b007de7787673a61b110055b4cce49e7dcbe9ee092809d47f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:67f8a76b0939dba6d21780840fb30310d54991ca90634b51cffd416e2d344f96
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74538899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c61be68605628329917168d49371cd583ba1bd6dd4a9ce99295025f2cdd03a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e9c35bf4ff5560030b773a4313e74303ca9abc4f76733b51c2cceab24ed61db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59015da23604a0123e6c648008596096a38231cbd08df796981592e8967ce82a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:b1f26b0b04c18442f48eceed88043658b641d96d0f8b67894fd371e5b1f69ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ecf8dda7f148b5e3929a2b9a784fdbab34a0214c6585b40ad942ba66b1384ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143101803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787eee0a5e2473253978555bf527fbb5fdefbd5b9044a06de57b5431c64e572`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b5ec6ffb24174c2e8d7b59efdd6b0613b5bcef62a7cde965c456ae6a2b2ea`  
		Last Modified: Wed, 31 Jan 2024 23:35:43 GMT  
		Size: 66.4 MB (66425971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fa0a7b3fc115eb7c50fdc121201b0f3cad61bc1aebe5431d723aa89c4276d81a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc1ccb440ba9cfc7dd732a50febaa76de48f748d05f381de5e076f2db2d8311`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162728a10cded66e397f0df0db68b9dbb11c61c6b79d3baaa731a13664cf8521`  
		Last Modified: Wed, 31 Jan 2024 23:25:18 GMT  
		Size: 64.1 MB (64084887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bc770f8215593410866c545b078b6c734690c704829b84e484ac261f8397c17d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130893443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a112abeca93d31b15a585b5d5c6f6b83020c1b10c0e0cfab3638ce8a249c272`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:53:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d5c17bde538214384a501538668ef9f5559e9cda83e4b7913d622823ccc1a`  
		Last Modified: Thu, 01 Feb 2024 03:02:04 GMT  
		Size: 61.4 MB (61445900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e50e6e87ada960fe674558c4c969c3f5c2a4376120151969b5d92b92aa2ed593
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142792869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e52d22551e9b7307d6ecf5f5151565ec72517200d28b1ed52e08dec63b594a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2cf8c96bc8d8d3f9a21a0e32a3a2e78e0e214cf8eabcf8557a33907fe41c6`  
		Last Modified: Wed, 31 Jan 2024 23:55:07 GMT  
		Size: 66.5 MB (66539836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e37db9b541825e0b461db7b1b3152315ff0ababb91262d5a28a073ce368abea0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146867067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b23f42a39184a2d5b358f89bda2622a92bb313cb551fac68e2da13ea220693`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad4f66a2cd19b6eea3bc0f180db9669dac381b31d1500c7c9b561e5310599f`  
		Last Modified: Wed, 31 Jan 2024 23:49:21 GMT  
		Size: 68.2 MB (68224658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fc0825bd389a6489fc62e1ac0b9edc1d57ac46cd5b0c4a6e7e6b5857d473b845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141447777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec64eb59a353b81dcaa6ca4fa3f268d8126a1a2499682b25aab14231ad0d51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bae2c96b6133a9c62aa17246799e040dbce8e2ce06213bc63d1ec7c2e221ca`  
		Last Modified: Thu, 01 Feb 2024 07:52:48 GMT  
		Size: 65.2 MB (65236018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c35af313037569737d47ff9054cd1f7f9bf415d6f8d94534a166f11b0c03fbf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154615907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6077912799958be3a58ab47c99949b783e864b50458ceaea23470245b2608a13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bfff2a14e6e587d4c11641dfff4fc47965b3e5a5be2c00940d05089da4f95`  
		Last Modified: Wed, 31 Jan 2024 23:50:28 GMT  
		Size: 71.9 MB (71937073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ff5d0793ef43078309ca6a97d67d7e0f26961d5f2a58fb16a9288192cd147631
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140231916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dca8ca1f900819fc3fd4311ddfad7e9713941b0ef695be38126286ae0de9f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f8b671531c36b200b6e84dd21a3c784a776685b99bb9638b337cfd52d06fb8`  
		Last Modified: Wed, 31 Jan 2024 22:43:30 GMT  
		Size: 65.7 MB (65693017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f65853fd4f580166d1d03cea84837b87e35ed3cd312174b15a8231df43afbafa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144764527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e4cd715bf0a897de59bb4489f02b586036192e46f18e78aa6439127c639e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c0a5ccbf3d4c81b3650225ea3b2d9eae4bd38f2e909a10e6c82117a577b24`  
		Last Modified: Thu, 01 Feb 2024 08:21:22 GMT  
		Size: 67.5 MB (67535565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
