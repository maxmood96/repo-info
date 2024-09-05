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
$ docker pull buildpack-deps@sha256:cd57ae2ab2536c11a7278b0c95a35390548b7f0193da23d7d84177e4d7cf0d48
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
$ docker pull buildpack-deps@sha256:bf1693622639614d7b51fcd557f2fec6d0ef45ebfad0c564cc2b2cf4c2f20ac5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245813153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e57f6349bebbf2a428b64e05e30e1452edf15c7d243fffdeebd6c6236495618`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:22:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d5b87a1475cb2bebd4a61e0e510c509560007aae9a127bb2e2a3fbcae76366`  
		Last Modified: Sat, 17 Aug 2024 01:31:14 GMT  
		Size: 11.1 MB (11133643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c879a37493b932706443549377060adf5849bd3e29c8fb34c4dfd2778dc1f30`  
		Last Modified: Sat, 17 Aug 2024 01:31:30 GMT  
		Size: 60.9 MB (60928764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98010dc515f7ff2be46b7513048e5c34d9377fc6a095ee86a755e499cb45ff7a`  
		Last Modified: Sat, 17 Aug 2024 01:31:56 GMT  
		Size: 145.2 MB (145166523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ec9fcaf7094b2237811dc6b2b9a0d4c73215c022acb086c50ade9023d3614317
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732aa4089e3b70bb63e38ec6814220cbb6eeaf82f5813b48e759889d54cc7962`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:18:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c44db121413be01c8efff606c5352913b04ea7d55ee9de266ca29e99f87a2`  
		Last Modified: Sat, 17 Aug 2024 01:29:02 GMT  
		Size: 9.6 MB (9606860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb0f6813a18000ba2cb151eb902bcefa325c57d600f5b2984b4d714ff817f3`  
		Last Modified: Sat, 17 Aug 2024 01:29:18 GMT  
		Size: 55.9 MB (55880086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5303ee8b4e59213cb809629d6ed390394c4c2b1765b8b01d2821ece8009c8b1f`  
		Last Modified: Sat, 17 Aug 2024 01:29:42 GMT  
		Size: 122.0 MB (121995770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3560e765fa6616970f9f436aa030ef20183457c2cf776cfe92388daf7a7695fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236090788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb726f00c17be72618aa4dffa20c2733a05a6e4b8a9f7613a225d1ab74aa6c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:14:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4364aa85a5a14128c7776ea4c23fcc57b40e56f723c123e3cadeeecd0d8be2dd`  
		Last Modified: Sat, 17 Aug 2024 01:24:35 GMT  
		Size: 11.0 MB (10982873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39beac17021b4ec51b652179fb388e7e59592ce3f5ed20929fdbf26ef4ec509`  
		Last Modified: Sat, 17 Aug 2024 01:24:49 GMT  
		Size: 61.1 MB (61055242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3146142e7a6e9c2d67b7df46b7b7f5d444be67ae3811abe7930cdf5535b23e0`  
		Last Modified: Sat, 17 Aug 2024 01:25:13 GMT  
		Size: 136.8 MB (136847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b884c241172d9d8ab634d137b51ff711e3f9d34eaada09d00957e39165b9c7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269570472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877a3c50c4d46dcd80b4fbf7ddc15e07d8519eb0fca42540d5ed757a57e94f6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:32:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd820297f3a00612ecd6f1ec3bd3e61123757fbe396a2cfae8b72f4c9c3aa0`  
		Last Modified: Sat, 17 Aug 2024 00:45:41 GMT  
		Size: 12.9 MB (12942071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac4e3b1bd2a4b79796a1da959333bd0d81548cbdfc5a17698fecfed1c641eb`  
		Last Modified: Sat, 17 Aug 2024 00:46:02 GMT  
		Size: 69.7 MB (69666130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46328d3b2d6b1b48d29412e39ea3baf09f40da4b405f70b4c0933ca7f3957561`  
		Last Modified: Sat, 17 Aug 2024 00:46:37 GMT  
		Size: 153.6 MB (153646151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:48d4d71cd62bc6344df0ee99ec9dd32a28d1521e0afd5fcdeb42ece679d71f4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226610931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bee57d9186d59476c20f53641c8bfca2c324fd7db6bf2e2fbb15f54964059ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:39:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8558e11a11831e23888e185bc022adc3e2a26aaa954ba10de957e7cb3719`  
		Last Modified: Sat, 17 Aug 2024 01:49:35 GMT  
		Size: 10.7 MB (10690160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4161498da3a2456c6b02d48ff2531a9fa0ed9d922edc7bc5f5c812347f644991`  
		Last Modified: Sat, 17 Aug 2024 01:49:49 GMT  
		Size: 60.3 MB (60339016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef7e14bb5b2b64bb51f343306326f543bd4525cc7cf20de8f7918cda292aefa`  
		Last Modified: Sat, 17 Aug 2024 01:50:10 GMT  
		Size: 128.6 MB (128568337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:e4007830688c72c63f9a1c9dbbea008ada3f0cecd692d53d69831b3970c77334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:20.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:543dcdb8e4675b69377e57cb70705ceb2c9f02d1ef38cee8fa58b78bafbca179
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39717866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1fadd79005d87467388f766899da33502c249ffc40d19ff2bfe22c202586f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d5b87a1475cb2bebd4a61e0e510c509560007aae9a127bb2e2a3fbcae76366`  
		Last Modified: Sat, 17 Aug 2024 01:31:14 GMT  
		Size: 11.1 MB (11133643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf7ba37697834a257c8552c0e335ab190cd10b7168298dcde5b9db5e97a39b18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34210681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0627b1ad06d51d3d87049da3bb58897d4fb4bba1a4f4e5b6511e69801dff2669`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c44db121413be01c8efff606c5352913b04ea7d55ee9de266ca29e99f87a2`  
		Last Modified: Sat, 17 Aug 2024 01:29:02 GMT  
		Size: 9.6 MB (9606860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4d91718ae34e7c67060562da2bd29fbc1789a457e84065b8cb8a09df33014b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38188117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f7bc6d40365e785e8170c1924cfa0c0e155af80c799f4ab704c57b99bbddc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4364aa85a5a14128c7776ea4c23fcc57b40e56f723c123e3cadeeecd0d8be2dd`  
		Last Modified: Sat, 17 Aug 2024 01:24:35 GMT  
		Size: 11.0 MB (10982873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4bd90b8805674433662921e3ed887fb91bbc6eb0b4c32618b0f1c6325fafb078
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46258191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0191540db9246e90617f7c6e8d2ea928cc207e9cf44c8a2495bbe0e17154e73c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd820297f3a00612ecd6f1ec3bd3e61123757fbe396a2cfae8b72f4c9c3aa0`  
		Last Modified: Sat, 17 Aug 2024 00:45:41 GMT  
		Size: 12.9 MB (12942071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24a1e11685862a8d2b943a1fbe00ba330a2e1448c0f154a6c36f8c2145eac29a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33874516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f60da6d80260eec4d7e3a10864e8dbbc5b2aec182b0269299a509de5e46de9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:45:25 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:45:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:45:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:45:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:45:56 GMT
ADD file:e801325f695dfee333234d27e4a3f460f2c87b0489699f1e3315d4b62550aade in / 
# Tue, 13 Aug 2024 09:45:58 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38e511e701a08f7bc3aef62d319fc8ea5dd4ce126a870719810f76ffdb74f7c5`  
		Last Modified: Mon, 26 Aug 2024 23:45:46 GMT  
		Size: 24.2 MB (24249703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379daf9f1fd009398df91bca6e9f7fe3bd97d786aaf5a2ef6e06fa7455011e3`  
		Last Modified: Mon, 26 Aug 2024 23:45:35 GMT  
		Size: 9.6 MB (9624813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7d126aac64329338d47e20f3e07e55d90edd66715567071977ed662d3e08046c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37703578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8f9c3ddd47ee2052f1131103ce0d906f296bf5d0c8e1c7d7581ae39724f0d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8558e11a11831e23888e185bc022adc3e2a26aaa954ba10de957e7cb3719`  
		Last Modified: Sat, 17 Aug 2024 01:49:35 GMT  
		Size: 10.7 MB (10690160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:7009735d9e9364f666ea8ba53ce9de337509bf7f08b86b5fed5f1edee90cff54
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
$ docker pull buildpack-deps@sha256:ab7f61d9ecf51804a5966854943194d47e44b98f6ba8d45ac9147834f65187ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100646630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1dd9bb2d7acf43cc802201d2dde00e149ff8af7cdb68a9279ed4f904c44c5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d5b87a1475cb2bebd4a61e0e510c509560007aae9a127bb2e2a3fbcae76366`  
		Last Modified: Sat, 17 Aug 2024 01:31:14 GMT  
		Size: 11.1 MB (11133643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c879a37493b932706443549377060adf5849bd3e29c8fb34c4dfd2778dc1f30`  
		Last Modified: Sat, 17 Aug 2024 01:31:30 GMT  
		Size: 60.9 MB (60928764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:59b5e39e5da4dc9d13bc2622a16d5b9b315546817c18513c487443de77c7765c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90090767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d145582d134fa5fd62627f8bba5579f49c707fd915e596ac45e8754dfcb75173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c44db121413be01c8efff606c5352913b04ea7d55ee9de266ca29e99f87a2`  
		Last Modified: Sat, 17 Aug 2024 01:29:02 GMT  
		Size: 9.6 MB (9606860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb0f6813a18000ba2cb151eb902bcefa325c57d600f5b2984b4d714ff817f3`  
		Last Modified: Sat, 17 Aug 2024 01:29:18 GMT  
		Size: 55.9 MB (55880086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:470cb82eab9c13f5c9abf92ad48923c6f4f5bb4aeb845c87f6e348e2d76f0c58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99243359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9254e12c5ebae17d5e08583286e495e6fb066b31a81edec524b6bed847f7a742`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4364aa85a5a14128c7776ea4c23fcc57b40e56f723c123e3cadeeecd0d8be2dd`  
		Last Modified: Sat, 17 Aug 2024 01:24:35 GMT  
		Size: 11.0 MB (10982873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39beac17021b4ec51b652179fb388e7e59592ce3f5ed20929fdbf26ef4ec509`  
		Last Modified: Sat, 17 Aug 2024 01:24:49 GMT  
		Size: 61.1 MB (61055242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:587093fa59e291b2e93393714dd0602a3b5832fc8f0b2eb6f026567c722e3807
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115924321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c280a99103ef064c559961e89984563474d74e528b43846ad7157dc36570490`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd820297f3a00612ecd6f1ec3bd3e61123757fbe396a2cfae8b72f4c9c3aa0`  
		Last Modified: Sat, 17 Aug 2024 00:45:41 GMT  
		Size: 12.9 MB (12942071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac4e3b1bd2a4b79796a1da959333bd0d81548cbdfc5a17698fecfed1c641eb`  
		Last Modified: Sat, 17 Aug 2024 00:46:02 GMT  
		Size: 69.7 MB (69666130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:36f6b49833d078f1d33ff183c902ec25b4ec5f1608a9d80ab42a1a2d2ca92503
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98042594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1d76f41b71565cc55898b6507e07c63598ce49867de9c22e757c2f297a969`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:39:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8558e11a11831e23888e185bc022adc3e2a26aaa954ba10de957e7cb3719`  
		Last Modified: Sat, 17 Aug 2024 01:49:35 GMT  
		Size: 10.7 MB (10690160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4161498da3a2456c6b02d48ff2531a9fa0ed9d922edc7bc5f5c812347f644991`  
		Last Modified: Sat, 17 Aug 2024 01:49:49 GMT  
		Size: 60.3 MB (60339016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:f94d4ac32b86b5e47c8309b8bde444d2b1ac185c515ee28ff4ebad588b0f21a5
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
$ docker pull buildpack-deps@sha256:a396fd7b825e12db08385ba54a8e5d17b12d7763e0b5db605ee5cccd236e6278
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250125255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5243157ef580dc6b962baf1d1e3cca36554b300e92223a811b2141027f9d4194`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:23:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:26:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d48c0031858d2d5110443ab36636bb43de1b4f9563d5121d289db6d7f72b40c`  
		Last Modified: Sat, 17 Aug 2024 01:32:18 GMT  
		Size: 39.5 MB (39461389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64250174469444d1b75872928fbe6818c56d6048cb5dca703b136af150046ee`  
		Last Modified: Sat, 17 Aug 2024 01:32:47 GMT  
		Size: 173.1 MB (173131517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a12f7b9a6f8b2f40a9d9efd6a7d42d7ba7f9fc908831857963574d2c1089e45b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217369666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a676edd37e9e7fa74a9ae9679a9e0087c55e5b10f6bc015b55fe1351b0e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:23:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facb95feeaeeb475846b3b20ee6a1f49fe09ff11e6be5c51044287df974edd6e`  
		Last Modified: Sat, 17 Aug 2024 01:29:51 GMT  
		Size: 7.0 MB (6992292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dac84cd042e2f25b48491d3dc0d9e796a7c229b7e09eb6f7e5368e97885a6`  
		Last Modified: Sat, 17 Aug 2024 01:30:07 GMT  
		Size: 42.2 MB (42244605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc3d603dc51fdb36b23fe9014cf77cf1634b7886703af66327a6a3222208086`  
		Last Modified: Sat, 17 Aug 2024 01:30:34 GMT  
		Size: 140.6 MB (140597719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:debf3598205a32dbb3829aba26eb6aae66c9a0d80ee126dc25ac1dfc2215956c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241399470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cccb2121d73f6ba7129795cc4a205fa76c2e70e5077a882d4d1aa8f2976e19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d7e3e6589ca2b01d191dcd38e16911631b1c1ecd6d6a1b19725adb25bcb33d`  
		Last Modified: Sat, 17 Aug 2024 01:25:35 GMT  
		Size: 39.4 MB (39382817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b3fa84bfaf4c88e61f4c2f8463313a09d480bee9d645c6c985bbed278ad01`  
		Last Modified: Sat, 17 Aug 2024 01:25:59 GMT  
		Size: 166.6 MB (166586020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:29b40fd42cc6f87f2bab315b49a247720758dd3b20daf66fafc0d8e3fad62e5a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271178540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03eb1be347df2cbf52a00aaaef1d912274de4d2dca1447953005d091a91145a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:38:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e29f857d015b0cbd97132074499724818f965d9a1d1390e861faf881b42a4`  
		Last Modified: Sat, 17 Aug 2024 00:46:46 GMT  
		Size: 8.2 MB (8190468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5792bb7235062f0d15f661a3f95bf8576db3f4ce19571f3c267126a3c7bd9069`  
		Last Modified: Sat, 17 Aug 2024 00:47:08 GMT  
		Size: 43.8 MB (43762057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a345e3cd75c476690515018f7406086ff6bc6b9d6d9143e614b5360d4f6c`  
		Last Modified: Sat, 17 Aug 2024 00:47:43 GMT  
		Size: 183.6 MB (183638371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5fed60b701ca50e50f9d91d1978511824521955643fe0bcb9791a0702314d9e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274995693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a4ab7dac9668b13a456ab8594ef91edc86d446b92d636316a277c14587c69d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Aug 2024 23:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Aug 2024 23:33:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:294ed87c40f8cf1413b3239e9975c38b12851c23334c529e90fa3e66d8f9f7e4`  
		Last Modified: Mon, 26 Aug 2024 23:46:16 GMT  
		Size: 27.7 MB (27710015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ace411d40322925822a30951a8290f84a11b834aff42c4227e9c888e6361`  
		Last Modified: Mon, 26 Aug 2024 23:46:02 GMT  
		Size: 7.1 MB (7100644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac83254f47c5a724e33abcf115362b29bfe72cd30c65493e9ac149d51093ee6`  
		Last Modified: Mon, 26 Aug 2024 23:47:08 GMT  
		Size: 42.3 MB (42311519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d94c75ef45ceefed0016875844a54b4a5e12e38e6ebb9250a26bac49f668f4`  
		Last Modified: Mon, 26 Aug 2024 23:51:07 GMT  
		Size: 197.9 MB (197873515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:970430e975f7fed83986a5dae6f95a27c5a4f5b6ead048ad2398e7750bc74f09
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223844496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e497765afc3c27c37895408c78c108f628e59ceeb542cc836ed3139da0e41536`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:43:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:45:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c437abab0275e6e3a6dc85400e2dd6035a546805afed5be0790bbe780fa2aa`  
		Last Modified: Sat, 17 Aug 2024 01:50:16 GMT  
		Size: 7.0 MB (7003356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43ea6d3e4350aa4d9b05bfac88decd19c457b21aa1f2b46407fd5895421b095`  
		Last Modified: Sat, 17 Aug 2024 01:50:26 GMT  
		Size: 39.4 MB (39416903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a20c48c231bd78419ceb6c8a4fe183a35d4402af1f5c9c03d0c6bc5cbfde34`  
		Last Modified: Sat, 17 Aug 2024 01:50:49 GMT  
		Size: 148.8 MB (148785734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:6c1c0223866007184103547fe530a16ec4866e76f951ab46d77f04fb5327778b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:22.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:901890331f06331c1caf4d640bc0399a918fcf967f2d09222118072fee68ed47
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37532349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0cce36c8ed8dedd75830a5c97e06db0c2f598b01af0e6de2a27eccab75b12f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4d25f50812748a1e7445db2eedb7a70b4be96b8af52c6db9c2768274649c862e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8487b734d1c640503adf958e48a743d5c0e4ce2e6964882eeb973729724761`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facb95feeaeeb475846b3b20ee6a1f49fe09ff11e6be5c51044287df974edd6e`  
		Last Modified: Sat, 17 Aug 2024 01:29:51 GMT  
		Size: 7.0 MB (6992292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f9cdcf11df92a79c36fbb45be15108fbeaaed05ebb445c20a63169f19d18f3c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35430633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e5393f0d4ce9c80a07a767186740b4a4235b067393a58080fca7c5806a44b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:225b091fa10b0a2cf0fe8996232873a82e3cbb68a1be60ab03424c969b3fbbea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43778112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f733f9ac26e356e2b82fd49785948dddfadd0f9bce2f00cdfbaeac48ca532245`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e29f857d015b0cbd97132074499724818f965d9a1d1390e861faf881b42a4`  
		Last Modified: Sat, 17 Aug 2024 00:46:46 GMT  
		Size: 8.2 MB (8190468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:31015f4795d4d614f41e9d19c75d23abdb5ac339d3dbb74d4e09eaaca5efdba6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8b253ea5d99eb7aef8bdd08de84376c39254e3c3f1753e73cda20919d3d524`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:294ed87c40f8cf1413b3239e9975c38b12851c23334c529e90fa3e66d8f9f7e4`  
		Last Modified: Mon, 26 Aug 2024 23:46:16 GMT  
		Size: 27.7 MB (27710015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ace411d40322925822a30951a8290f84a11b834aff42c4227e9c888e6361`  
		Last Modified: Mon, 26 Aug 2024 23:46:02 GMT  
		Size: 7.1 MB (7100644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:07790c7c9d9e68a7b881c7f56abc6f808b99b910e7a785f4ab77f9ff1e596342
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35641859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda44fc20438c945c9055592ea2a740fef4765074d09a0d730bda4e73044eec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c437abab0275e6e3a6dc85400e2dd6035a546805afed5be0790bbe780fa2aa`  
		Last Modified: Sat, 17 Aug 2024 01:50:16 GMT  
		Size: 7.0 MB (7003356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:c43e80c35315b693c7d14b4e9608895e28361237b35ac959ada11e533fc3660a
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
$ docker pull buildpack-deps@sha256:698f64014507b56ee2d366b2a8a96c5cde7860defc92b291af6203f0b017496e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76993738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff9e0089988e6903f9eedb1f01c84f4c0fd6cd503dd3c9af67b82ad8ac3d60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:23:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d48c0031858d2d5110443ab36636bb43de1b4f9563d5121d289db6d7f72b40c`  
		Last Modified: Sat, 17 Aug 2024 01:32:18 GMT  
		Size: 39.5 MB (39461389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ce09b9f813c75be557f135c80174a3d9f72430076bcf68150bff69b7dae6eb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76771947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12b0f1c0b7272953ccc51b50f8dbf4aee9a7bbd7f9897eebb2bca87396de09d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facb95feeaeeb475846b3b20ee6a1f49fe09ff11e6be5c51044287df974edd6e`  
		Last Modified: Sat, 17 Aug 2024 01:29:51 GMT  
		Size: 7.0 MB (6992292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dac84cd042e2f25b48491d3dc0d9e796a7c229b7e09eb6f7e5368e97885a6`  
		Last Modified: Sat, 17 Aug 2024 01:30:07 GMT  
		Size: 42.2 MB (42244605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:efab8f1cfdb230f6e65f3dec3532cea57049d37b987b44bc7a9155e1703f4d12
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74813450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd51ce3b8f9d1c03500aa82e6f0e2bb3198321cccad3546e69ae9f4a551a2d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d7e3e6589ca2b01d191dcd38e16911631b1c1ecd6d6a1b19725adb25bcb33d`  
		Last Modified: Sat, 17 Aug 2024 01:25:35 GMT  
		Size: 39.4 MB (39382817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c2ff96617d783ada9cb33c533847c5b23aa55acff44899f15aedae650b514a4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87540169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2444144ae15c8970970bf8799ba611cbd99cf51034436dc7d775fd844ae86df9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e29f857d015b0cbd97132074499724818f965d9a1d1390e861faf881b42a4`  
		Last Modified: Sat, 17 Aug 2024 00:46:46 GMT  
		Size: 8.2 MB (8190468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5792bb7235062f0d15f661a3f95bf8576db3f4ce19571f3c267126a3c7bd9069`  
		Last Modified: Sat, 17 Aug 2024 00:47:08 GMT  
		Size: 43.8 MB (43762057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6e3db9770d82d45db88df1d36723ce265c7965fc8c6606eacd80eca91ba603e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77122178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b223cbdb8c5546ba9ed89b715ae297a96f33bb77038e2e6f8224802562fe354b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Aug 2024 23:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:294ed87c40f8cf1413b3239e9975c38b12851c23334c529e90fa3e66d8f9f7e4`  
		Last Modified: Mon, 26 Aug 2024 23:46:16 GMT  
		Size: 27.7 MB (27710015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ace411d40322925822a30951a8290f84a11b834aff42c4227e9c888e6361`  
		Last Modified: Mon, 26 Aug 2024 23:46:02 GMT  
		Size: 7.1 MB (7100644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac83254f47c5a724e33abcf115362b29bfe72cd30c65493e9ac149d51093ee6`  
		Last Modified: Mon, 26 Aug 2024 23:47:08 GMT  
		Size: 42.3 MB (42311519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d680df10b2d49e7e257e6ce7fef8083c386873a5d9176e4f0e4202aa09f9d231
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75058762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3b6a80a663c6b40f8e3fcf49fb64d1803dd93a4689404de3be6122cbc03dd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:43:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c437abab0275e6e3a6dc85400e2dd6035a546805afed5be0790bbe780fa2aa`  
		Last Modified: Sat, 17 Aug 2024 01:50:16 GMT  
		Size: 7.0 MB (7003356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43ea6d3e4350aa4d9b05bfac88decd19c457b21aa1f2b46407fd5895421b095`  
		Last Modified: Sat, 17 Aug 2024 01:50:26 GMT  
		Size: 39.4 MB (39416903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:d1efe49d2a055c28dc6ccb292899eec33018a29fe267765b43a41f10eb5865e4
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
$ docker pull buildpack-deps@sha256:dbfee7e7ee2340b0d6567efd3a8a9281ce45ee78598485b4d7a7f09fe641811a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279787125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c54fa271c5fb3ca0e18e8011847ed2e9cd8c033b1b6ffc67eb41e9f18193a65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:30:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1ca6bfd59b4127ffec4664a8d1e54ea862180100d40aeb40be3f042b8780af`  
		Last Modified: Sat, 17 Aug 2024 01:32:56 GMT  
		Size: 13.6 MB (13615674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5776cc91e40203afa47aee5918fda211d15a380be379e60770d3186c2bbdfa`  
		Last Modified: Sat, 17 Aug 2024 01:33:10 GMT  
		Size: 45.5 MB (45476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe981aa2513ef31d687e87f7466c92065fb22c8c3a1f3491b89b552b1ad65fb7`  
		Last Modified: Sat, 17 Aug 2024 01:33:42 GMT  
		Size: 190.1 MB (190127690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3fe36aff5ed130ddfde72ab3e8f2ff5a91b142f9b986e6703ab30e426fa2109c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240043505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b943ca2d91c0f7fd97f07b9a99922c68242be969ceae8cf5c7d6fe8fe07ef42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:28:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c6e3ee23495dde6aacd7387cda5d097d12375226029008e2458cbfa9ed0d6`  
		Last Modified: Sat, 17 Aug 2024 01:30:43 GMT  
		Size: 12.8 MB (12773383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb96a6a812e45055b7676e783359615606d9732634a27fcc8e5f90dba0cdc38`  
		Last Modified: Sat, 17 Aug 2024 01:31:00 GMT  
		Size: 49.0 MB (49021511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d8b9c6bc43d5558a2b951ce712a06393e8335c8e10d57912e67d7f52176a2`  
		Last Modified: Sat, 17 Aug 2024 01:31:28 GMT  
		Size: 150.6 MB (150559371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f454e252cf6d2a1fd13ee819afb58768a6510bd1b05c8c2ea7e5f188c491ac1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270882007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd3d542d4445328bb8f18374ebddb0f5997669f387947b7c37d277cf84c0a69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:23:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a012413ccee10b0979cc0a8a4dbe55d3b3d7da3ab29297f5f9c123b2b126a4`  
		Last Modified: Sat, 17 Aug 2024 01:26:08 GMT  
		Size: 13.5 MB (13452136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3fc2143112f81cac57d899b6b74e9823eacdb070d57fe48697e0476d5b7922`  
		Last Modified: Sat, 17 Aug 2024 01:26:22 GMT  
		Size: 45.4 MB (45429639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fd0de2c4b08430014c443872339edde35b841e197e3f9700b472c466a61430`  
		Last Modified: Sat, 17 Aug 2024 01:26:47 GMT  
		Size: 182.1 MB (182090203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cc5114d6a58e74589c75ced266bf04b778c33f883d50b326435d025a0ee02de3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299140106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3366172af3c194b5390ab31a9a6a902e332eb1ec203282a31dcf787d5a188d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:44:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b02f58c3bb9b5e807e488d763aebfd412e5c890fe7395af264f03013905316d`  
		Last Modified: Sat, 17 Aug 2024 00:48:14 GMT  
		Size: 50.7 MB (50713751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ad33d7385c0e28e8c738c1308b8fa4b34b109adf7fd7fd112f9d0cd58de69`  
		Last Modified: Sat, 17 Aug 2024 00:48:54 GMT  
		Size: 196.8 MB (196800287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:343ce2a2f7835b6e472455fc20d62f4b1bc0a8ba882302865daa7e88d945cc23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342710842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12de875f5f9606da9fee429ae26a9abe9f14926b260f6ce8e88bfa8310c546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:39:04 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:39:39 GMT
ADD file:75a3b8c8bc557fdb66bdc49a2a84206986fe15571577feb7dd59c28963aebbe1 in / 
# Thu, 01 Aug 2024 14:39:41 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 26 Aug 2024 23:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 26 Aug 2024 23:44:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7cf048cdc1e6ca12f1a2101771d1217b7a6c3a2045516b5d28e4ff96223fa106`  
		Last Modified: Mon, 26 Aug 2024 23:51:40 GMT  
		Size: 31.9 MB (31898096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea2c157a2f80b8dae691e1a22d4a573cb68674124557f3dd115c9d90a0ed3b`  
		Last Modified: Mon, 26 Aug 2024 23:51:31 GMT  
		Size: 16.4 MB (16425854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52773e5ffae3bd09a6127cf2a4d2a1f83184ff591ae56ece2f1e530020bed073`  
		Last Modified: Mon, 26 Aug 2024 23:52:35 GMT  
		Size: 53.9 MB (53929997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3ef92e2f61ba657d4f35753d47bd810ffbacf0c0fccd43bb62ee4446badbb9`  
		Last Modified: Mon, 26 Aug 2024 23:57:07 GMT  
		Size: 240.5 MB (240456895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ba2226ac5d3ba5e49f1642fc0dcc05023352cfbbaa010cfedefa131876e99820
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262190525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836608c2e7df5618cab581fc05e38837074a184a85b1db14bc487d1c659910df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:46:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:48:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042bd266644c5e20fcd21cd963b6af3a4f42327bce19ddb3c7f6be5cf1465c5`  
		Last Modified: Sat, 17 Aug 2024 01:50:56 GMT  
		Size: 15.0 MB (14988257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d49ef9b9b276d1eaec35ac35644a2dec74931b57d891ca0cf93f7dc38d487`  
		Last Modified: Sat, 17 Aug 2024 01:51:08 GMT  
		Size: 47.1 MB (47114045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0769f3c11079252bed91efd5483db844a62961322eddaf3d249ad00da37b6`  
		Last Modified: Sat, 17 Aug 2024 01:51:33 GMT  
		Size: 169.4 MB (169395899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:77996a99be212be2be1c121960fca37fc891247b1266b604662c50bddcf89372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:79dd12360d2c69fb1f4f12c8f3d17f7c9f42e23a7c442b4415f50e8ebd77014d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992a8debfe0bed9089eb69a260383021bce2ef2bc09ad4b816b99cf6b5c26572`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1ca6bfd59b4127ffec4664a8d1e54ea862180100d40aeb40be3f042b8780af`  
		Last Modified: Sat, 17 Aug 2024 01:32:56 GMT  
		Size: 13.6 MB (13615674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6ef36dc65396dfa5e2211df2d441eb3a1d376744fc0ad7c44eb460646487b72
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40462623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc46af37225001abb4475256b54906ad24be323206fe6aeafee63a4e15465be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c6e3ee23495dde6aacd7387cda5d097d12375226029008e2458cbfa9ed0d6`  
		Last Modified: Sat, 17 Aug 2024 01:30:43 GMT  
		Size: 12.8 MB (12773383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eb483f89c5551848b2bdb2a113d25d70324dc18c8e2a30ecff379d780a720402
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43362165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6650bb4f0519da0766241c5686f2c9a2236edb645660c9cc8adf9b384774c6dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a012413ccee10b0979cc0a8a4dbe55d3b3d7da3ab29297f5f9c123b2b126a4`  
		Last Modified: Sat, 17 Aug 2024 01:26:08 GMT  
		Size: 13.5 MB (13452136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:939db20dfdccb4508129df097660aa6b8b1b74b8e5a9235f04e6e7bd8bdec00a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51626068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a407552833b5b43c46a6ebec6a71906f514b2f383acf027d8ed2aec6b40ec09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6333be5c165a9c25f7432777d2f5c947e6a2f52dcd21449c2084d6a2ac5c1216
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48323950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c345e12c9db2111f673a3511723995d50c278fed4f44b2d38e4869a67103d81b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:39:04 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:39:39 GMT
ADD file:75a3b8c8bc557fdb66bdc49a2a84206986fe15571577feb7dd59c28963aebbe1 in / 
# Thu, 01 Aug 2024 14:39:41 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7cf048cdc1e6ca12f1a2101771d1217b7a6c3a2045516b5d28e4ff96223fa106`  
		Last Modified: Mon, 26 Aug 2024 23:51:40 GMT  
		Size: 31.9 MB (31898096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea2c157a2f80b8dae691e1a22d4a573cb68674124557f3dd115c9d90a0ed3b`  
		Last Modified: Mon, 26 Aug 2024 23:51:31 GMT  
		Size: 16.4 MB (16425854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:61b6032f68e20dbce644cd1233623d2f60f0c6930dc5063d4ac064ea8d9c50ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45680581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6014e9474dbcc7c8c553d72aafbbe058ff7411a6971f5f6fff6f253a3e34bf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042bd266644c5e20fcd21cd963b6af3a4f42327bce19ddb3c7f6be5cf1465c5`  
		Last Modified: Sat, 17 Aug 2024 01:50:56 GMT  
		Size: 15.0 MB (14988257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:bed3d809d5cbccf0f5f9ed8b0930d6d73e974bb00c520050e2fddf1734108eca
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
$ docker pull buildpack-deps@sha256:534ad44c162160c9365023ed328da30f02c5b771e649fc37581a9ba61ced6d19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89659435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771021b2c4cdea239fa2c1a6e7d1f2f770e7838d65795ce316a09c8388984466`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1ca6bfd59b4127ffec4664a8d1e54ea862180100d40aeb40be3f042b8780af`  
		Last Modified: Sat, 17 Aug 2024 01:32:56 GMT  
		Size: 13.6 MB (13615674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5776cc91e40203afa47aee5918fda211d15a380be379e60770d3186c2bbdfa`  
		Last Modified: Sat, 17 Aug 2024 01:33:10 GMT  
		Size: 45.5 MB (45476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:246cbc5056ad0bb88b99598f13c40b5457206cc577a5a25f4dca5dd6916fc323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89484134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b610a682eb0a03418ed50058a521c1f1953e2581b96a929de0f73c7b8a083d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c6e3ee23495dde6aacd7387cda5d097d12375226029008e2458cbfa9ed0d6`  
		Last Modified: Sat, 17 Aug 2024 01:30:43 GMT  
		Size: 12.8 MB (12773383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb96a6a812e45055b7676e783359615606d9732634a27fcc8e5f90dba0cdc38`  
		Last Modified: Sat, 17 Aug 2024 01:31:00 GMT  
		Size: 49.0 MB (49021511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6600f12108c07eb81d530685c8bed0f3ab19746a8d7b4d8c021eb8434e82d2c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88791804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e56eb0060a581c8f2270b08792b38f5fbcb79b6698bb8b0a1d62cd4cc4d4f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a012413ccee10b0979cc0a8a4dbe55d3b3d7da3ab29297f5f9c123b2b126a4`  
		Last Modified: Sat, 17 Aug 2024 01:26:08 GMT  
		Size: 13.5 MB (13452136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3fc2143112f81cac57d899b6b74e9823eacdb070d57fe48697e0476d5b7922`  
		Last Modified: Sat, 17 Aug 2024 01:26:22 GMT  
		Size: 45.4 MB (45429639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd44cea5713601b9d67059c57e116e28b331fadcddb64dffd60f12cedfc40923
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102339819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295ecb5a3e55316f1ba417d43ce139c5137df9033cf99f943ab4dd924ecbb00d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b02f58c3bb9b5e807e488d763aebfd412e5c890fe7395af264f03013905316d`  
		Last Modified: Sat, 17 Aug 2024 00:48:14 GMT  
		Size: 50.7 MB (50713751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ceea6ca1c43481f76732c7d3e14bd92c2d6336e332dd5f7d1905ce679cbc7f0b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102253947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03df7edb24fd621f7b915bf4aa8675858e7392e04153e0cedec1fa8015475ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:39:04 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:39:39 GMT
ADD file:75a3b8c8bc557fdb66bdc49a2a84206986fe15571577feb7dd59c28963aebbe1 in / 
# Thu, 01 Aug 2024 14:39:41 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 26 Aug 2024 23:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7cf048cdc1e6ca12f1a2101771d1217b7a6c3a2045516b5d28e4ff96223fa106`  
		Last Modified: Mon, 26 Aug 2024 23:51:40 GMT  
		Size: 31.9 MB (31898096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea2c157a2f80b8dae691e1a22d4a573cb68674124557f3dd115c9d90a0ed3b`  
		Last Modified: Mon, 26 Aug 2024 23:51:31 GMT  
		Size: 16.4 MB (16425854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52773e5ffae3bd09a6127cf2a4d2a1f83184ff591ae56ece2f1e530020bed073`  
		Last Modified: Mon, 26 Aug 2024 23:52:35 GMT  
		Size: 53.9 MB (53929997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0fed4047a264089ebbfaf4f5afee2d54efa50b339ff5f636b50aa069e455e22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92794626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c19cb866a87617680f1f7b8f5e14167811acc2f6e6173d92d75490d48610dc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:46:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042bd266644c5e20fcd21cd963b6af3a4f42327bce19ddb3c7f6be5cf1465c5`  
		Last Modified: Sat, 17 Aug 2024 01:50:56 GMT  
		Size: 15.0 MB (14988257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d49ef9b9b276d1eaec35ac35644a2dec74931b57d891ca0cf93f7dc38d487`  
		Last Modified: Sat, 17 Aug 2024 01:51:08 GMT  
		Size: 47.1 MB (47114045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:3482f48a94e991a648afa7e928a52800e8d9de9135b7cdf1e0afd895f2e0e1dd
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
$ docker pull buildpack-deps@sha256:36c2f5ea2f2ed1af1a446e2a4b9c0581b2e9f6426c9c666c302f3f9da33d9233
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349024496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68e5df27df86c2708cfa83cb52ccb6743a7e33e15c08e881e1a7b139e17eaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9f466c772c63c0e404781bd892c92479011664bf06f3cef798537d746b179c6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316100401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493e5bda9d497e34a2368597973d59f8726156a38ca2253594f5cc160dbcc44`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29df05d41a6c52dd0e5bf38b1bd02aabd071cdfc47e5db769d4f8027cbce9b07`  
		Last Modified: Tue, 13 Aug 2024 01:30:40 GMT  
		Size: 184.5 MB (184530610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14bef58de028be12d34b7d805db521356633a00a79f137bb9f3b40507b15c1cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301543748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a3d866e963713e2b0df1ca898afeec6d371ecb89003a9583c5eeeabe181b8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf1b5402e12f0e97f96b3da218271b7caf2abf4a321ce82a42bedc2d72eb82`  
		Last Modified: Wed, 04 Sep 2024 22:36:55 GMT  
		Size: 175.2 MB (175209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86e5ce1c1f020479b72379683bbaaba7231a8116d5e7c58f2296616614edfa2d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339829397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71f840d8ec66950efb66641927297df50dfd31df6ac0fca91b03f94b6dcbbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:02:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c2a8d94613f34ce7d0ac4fd4e51800d8f4aa8a0bc9347fe5c8436b4c3bd5`  
		Last Modified: Wed, 04 Sep 2024 22:08:46 GMT  
		Size: 202.7 MB (202652028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c74dfe011eb174893ece8c3425af9325b29bcf3b255dc6e801e51559d7e4fc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351614656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bd62f9c712d1e81e60de9dc0a2e3a0204625ac0827903ce83fe542f65e3bd9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:06:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:80c1fa486a8fe97ada53cf595bbf926961ccd26376ac7b955e202996f7c3fcce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325968669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ce2a7a0bc3c2b559803f3b5f224da10915c34d06666b56f5c7c5398f56493e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93661e8bade5668baa650e17db139abcf2b722965a5fbccb9f55952cf3a58f`  
		Last Modified: Tue, 13 Aug 2024 01:34:16 GMT  
		Size: 189.8 MB (189802742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e1e4dc245c2aa0f0dadb1aced70100a855dbb67c14f3ea00f313201d7391b80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363098887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199ffe8f176fb39cd04f4be9dc7085de14b523d0334dab77db8947fe524ccd88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:22:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:245b9b0711a7536d1e01d84674d3150ed436ded567d718c318ed6f0991c7fdb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318370851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11952f41cd8b223618a6668fc853d395c9ec9cbe84e9f8096e511a00a6696512`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:d837e875e25e20675b44816d84a6ee4bf55f334430e024b3167598038928e438
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
$ docker pull buildpack-deps@sha256:66e568a0a9e5131643f75cea2fe66c8b45cc0395469455b5769ec2f051ee687b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73609855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f970a070b94afe24b57c75affd184376a5184f3f89257081f38f470e378ff16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0a6ef7c61de7721a295dca8e97bb78d27624162034e64abae614b705e4bf4ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09194f0040c080f5fb56b3fb0339a44e743b1cae3ac4748998b7f95c3f2f8f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5f2f9b35615c65ef5907c414739f3c797f3ffed0d930f9dd7b804fb44c6e2f8a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1be3ba03c082f27c71f0ab4f19490077884e870604189d30b5c0a62f4a604e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3ecd6e86b392efaaa7b0ccfc022e224fe6542a1c5a76865b63fbe3362af4e489
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc916e017c53b1c9e80e6ca1d4977005c6f31a98c64fbd683dc49f98c0bfc9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3612c7ccf08d122ee492ab85372b19fe18a7d7337341fd6e764344a2f97ab2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3502433f1c3c8c63799bd241a5a37328bb670138e1bf9b65d74a5bc3dd77d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fea9e7e67e7b3f4cfa2c41ec170a1441ddd2f616fbc3ec48fceb33f384affcdc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db64fceb23f2d8915303c28c71b92b4446a541960f1b090c0ff16c58457bda4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2afd8ac0056f6339cd6e120016dddf7da8b0d0b9bb1bf8b4fb224030c8327179
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08af492de9c4b4dba33292c74f6d83a0bb23f4706dbcc91dbd7fa16d7384722a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a34981c40380a750bf180a238c928fd2c0d4d850401ab232c5522418f5917fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e55127375c42a52b0cdff321d3068ce4218382ea8fff382d9c06f2bb5e4ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:e2ea1bc81a724065d5629534f53d30f60729c4576001bc066aaf56e300ea237f
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
$ docker pull buildpack-deps@sha256:68e358c3c05d520af01b674163e1f5d31a6172366ed0352550d4b5f4001cdfd9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137757873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2581f163f0552bbce9b3a5d33ec03b5f75be04876ea325c1f0a2f936f293fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1d2cb11ccef3f86147133f3dde474766ccae22d038c1498ade71e3d9505fe665
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131569791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efbb3e4bc9ebc13547c5d9944bbe33ee0a59fcfef91a5535a2fc4c3527826e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ef757fc27d5b94c652221e08501ca120f44bc94bcc3eb9b3130b28f91307c18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126334298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833eb6fd43fd38ce68fc4749a0272945c863058498498304d502e076b86aa650`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c0796108d4f0bb51a454428f5166df78cc3e40136a7d253ac1d8beeb85f734e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137177369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0013d72146ac385cfbc7a7ab43109e4916a8e8fba1e0c7aeaad85545273d89a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fc24d91b13db9bea6198bb18d275403768ca62332ea9815b3e91b87bda5b6ec4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128efb528b94818265ba8257926d66c6c6ded4a2257a29e6bf86f4ad39ef4ecb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4d1ee8e4bdbe8b07ec10c0d1115f4e722abb614ca2123f5524e48c3b653f8451
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e0fe59d2d5ca07f6a297b61740fb334b836d66fdab89d2d1c3ae797d7a8cfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67fb44179c22a0a46e18108147c764d2096f18d571fd9b0b90c37a493a55701f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a399ae7695be551ea659c15ec8842777bf6d4db45eca491da16667270d6fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:732c22618cfcd4e8ef5da95054a577ddec7f874e23557a128b01813304bd6048
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ae05d5608df2ce534b0015ec009bbac71560883de2290f6691dcaa8a9588d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:a6ae1502d0a7478947fd44eaf824483cd394a3a3a18015cb922c15de1e24b9e0
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
$ docker pull buildpack-deps@sha256:10a4036dfab922ead2cfebd38ad6880fd220be472d07b0ddf78428a548acc74f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322639503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab79b6993cafa55d4bb27f42d4a7d9151d8ff09fd9b00803dff1a6d0d061fa6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:57:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:641f090b8ccaa18cb371821c1cf43252189d3c11741ed51e1fada95c2ee9f288
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295537834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6d84aa0143aba03b59a838196830f2757eca2b5e1c8d03af86ebbffb96c511`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc22013229b56309440bd8fc1d5ea5676b191eef21e7b46a13f701910c56462`  
		Last Modified: Tue, 13 Aug 2024 01:31:10 GMT  
		Size: 52.3 MB (52329471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d1eab0e56c7f5eda9931e89b45d4088957214e10070dd831c5879c06fffcf`  
		Last Modified: Tue, 13 Aug 2024 01:31:46 GMT  
		Size: 175.2 MB (175244246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:803b714c506cda16406db60e38e9dc395c9830311d7c78ba044e1b5e4f867072
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283246496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f5954c9e1191853abacb6effda18c4b5bc3590eb3b29680c31b0377ec40f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:31:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a810222c5e9f2cbfb1260daae6fe81f9c63f9fa8cad05812e717e0135194dd`  
		Last Modified: Wed, 04 Sep 2024 22:37:24 GMT  
		Size: 50.6 MB (50616939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae26722d7d3c0994148ae4ede7eb08ae409fa7ac05c21ff66d41b5f7966fcad`  
		Last Modified: Wed, 04 Sep 2024 22:37:57 GMT  
		Size: 167.5 MB (167509349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e6ad79369b89f3b7e1d2a7a488db0f943067bcec96f234fde8be4296e62d5811
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314276579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a407b93f2f1b9c154892204f16a039161bedf6e8dccb5d4f7951145491f8263e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:04:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2c74c1774e448d6bb324968dd639df704566af4ae9461a86ec79cc6e8de709`  
		Last Modified: Wed, 04 Sep 2024 22:09:38 GMT  
		Size: 190.0 MB (189961799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4f3ebc102ec78f80d2b3055e46bc6df3d9d30bd344701f75fc79520382f5685c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328222990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef63590d9618b3491dd4dffe9c1a4523662c21fed4e57f84fb1e63f1f72bc5fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:09:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29843169a9c8306d94c89194ed26f3e75a8d2afa2d64a020ecbfd7f77998e397`  
		Last Modified: Tue, 13 Aug 2024 01:16:03 GMT  
		Size: 200.0 MB (199953236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:99b1989c136bc87e0ebd9086d96c27cc952fdf0ae2c9ab102e21d08a805ec990
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301518540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597a7a2e07a11e8dc70a7ae64312a4251e2097851bf68687fbb193c706ed0585`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:11:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b3474926636ee8b68ffaabc4b0327c4331cc3894af8f568c64d5f6f1d8594`  
		Last Modified: Tue, 13 Aug 2024 01:35:20 GMT  
		Size: 53.3 MB (53310999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acdb857f86d97c41d9b15b80df1ae493a4f9aa861236fc1b5fbf24ed5257567`  
		Last Modified: Tue, 13 Aug 2024 01:37:17 GMT  
		Size: 179.2 MB (179162196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4327d8a1a81e9755a664e3e15772b180a74b77c376c7d1ceccfdfb87a681bb0a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330991662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745b30ddf4d9d5cd2ce026ff4115c1d083935043473f115237dce720f58f05c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:26:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f036d67ca6dd9f8302ee75fa7409b9e24f1557528c725d1b15a5d8d019aae30
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296102116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c67476fdcfa6533a7f193a889a8ab07789f3354f024f764300e29ebeaf7a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:3708731f454324d6f2a7d2f25e37549896564b18b2907268bbbf168f6e5af72d
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
$ docker pull buildpack-deps@sha256:b2ab43637316a966d7564590785da3116fae87b52b907a5902fac9ea50229dde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466b383277cf6493fa742bf3fb69e36fb7f73ca32ad5144e04b152c941c323a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:95dfb0ec397c71c94c6e076ecb5346340f3dcf4327daa9174c5ba8e40a9d3922
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395d531798cd6c5aa61f96c696b9339f9a6b5fe4519527ae61f07c3a4dd8919c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e7afdad0f3b3df78a5cf51155a52d76832932cd6e03f28fdc574553d70cbd697
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3676be8e05fff3206a23ec525511e61d914a13bdfc8f61c6e84b939e9f3d70a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9f6af9c3ed8f6d7f676495af771260c9613758c38202ce10c30b9eccc2cafdbe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69481331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea0b2da908ed00a3825a18f9acd4a1898d9a20bf6ce8b93885508d458a292e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:11c49d08efb516426e63b794ff0a6a3e6f7d6ca47101c8a0a1382390ddfe0a41
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72342047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e404efea07746cc36cf3c48082a8023e994f30b3e282181c50de52ab22fc787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2e53d71d4de748cbbaa71f785bc60badead1c7dbabe66ae888229af3fbad5d15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69045345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8199f996ed824b9d6d1c8620a66af2fa0254ee49022ba7aa7636e656d9df13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:34ae04276fc096d665517bd951570adf94b0e304739c1cb82528af95fe9363fa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d18f0b36ae6d2807784af58b7b7b01c29288b1a28d21b4f161f88b4d5e801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:34e92b89bcad65835615a813c2e92ddd58c4398b8bb73619ea899ff33ecf2e16
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed06a5a153c1e116f2a080896ef906396f2d8d41d9d263c6de0d56a8667971e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:45f5e141493a46219849c6f6acce6edc74e5804b4650f0a40ee16adc9bd5baef
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
$ docker pull buildpack-deps@sha256:4aef53b9a2eae41c83be8f573280b21013c421e704b19b08312173d0e3e35573
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125571750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b31b3c521a9d88d81aa84171eba30d1f9b198944fdff4b09f8c830a8751dc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a86730fc51beab973cb8add78f2a7e58deebff1e672c01d62614821d77a79a90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120293588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d361f615568448e949e16d27136fe91cd71e9fa15a0c10306291505053e8b45a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc22013229b56309440bd8fc1d5ea5676b191eef21e7b46a13f701910c56462`  
		Last Modified: Tue, 13 Aug 2024 01:31:10 GMT  
		Size: 52.3 MB (52329471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce3b9e370af68730a4b51563bd8e8bdafce6d4eff06b4c3bab7af18aed7cae97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115737147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7d917904ba0aba7a811d8927b48c9d24febc228111d2b66aeab0bedbedc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a810222c5e9f2cbfb1260daae6fe81f9c63f9fa8cad05812e717e0135194dd`  
		Last Modified: Wed, 04 Sep 2024 22:37:24 GMT  
		Size: 50.6 MB (50616939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:25055f990335dc5e442f1da22b05a2229bfa4e780330493c9fc1a0b91c4d36b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124314780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058d4847d703ccb14c228bd019b880f4a587bdf25cb89d195fc24363bdea5c75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2c3044d7a286ae2a788c5b37f5bd2fe6aa0ffbc115851050defffac0fd544962
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128269754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6dbb003a1a505f2070fde5fd98afdca9b926fea0fee1d727d782182c96a174`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:35b801921e609d3209dacf1b5ba52b01de7c3aa9e8aa02c6391d36341e616684
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122356344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcab7119b603616470e424761bd314b03772c99f37bb1c28be22208d5e17e2ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b3474926636ee8b68ffaabc4b0327c4331cc3894af8f568c64d5f6f1d8594`  
		Last Modified: Tue, 13 Aug 2024 01:35:20 GMT  
		Size: 53.3 MB (53310999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b24b3a40397e5e4780ec4987a4c5de21b5a10aed81c711c231d6debb8669d609
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221000ca1ce797c56fce59ac01ef1cd91a243101b30d6d0fec00980d1226a63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3946705950289b1cd5ee35a7981aabd8a53eafc5e536516a12c29dcb83bc7205
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123041240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c52f640c0a850aadaaf7abcdfb8230a8322f73ee3c1e5c69a140e8d7e315c26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:d837e875e25e20675b44816d84a6ee4bf55f334430e024b3167598038928e438
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
$ docker pull buildpack-deps@sha256:66e568a0a9e5131643f75cea2fe66c8b45cc0395469455b5769ec2f051ee687b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73609855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f970a070b94afe24b57c75affd184376a5184f3f89257081f38f470e378ff16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0a6ef7c61de7721a295dca8e97bb78d27624162034e64abae614b705e4bf4ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09194f0040c080f5fb56b3fb0339a44e743b1cae3ac4748998b7f95c3f2f8f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5f2f9b35615c65ef5907c414739f3c797f3ffed0d930f9dd7b804fb44c6e2f8a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1be3ba03c082f27c71f0ab4f19490077884e870604189d30b5c0a62f4a604e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3ecd6e86b392efaaa7b0ccfc022e224fe6542a1c5a76865b63fbe3362af4e489
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc916e017c53b1c9e80e6ca1d4977005c6f31a98c64fbd683dc49f98c0bfc9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3612c7ccf08d122ee492ab85372b19fe18a7d7337341fd6e764344a2f97ab2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3502433f1c3c8c63799bd241a5a37328bb670138e1bf9b65d74a5bc3dd77d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fea9e7e67e7b3f4cfa2c41ec170a1441ddd2f616fbc3ec48fceb33f384affcdc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db64fceb23f2d8915303c28c71b92b4446a541960f1b090c0ff16c58457bda4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2afd8ac0056f6339cd6e120016dddf7da8b0d0b9bb1bf8b4fb224030c8327179
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08af492de9c4b4dba33292c74f6d83a0bb23f4706dbcc91dbd7fa16d7384722a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a34981c40380a750bf180a238c928fd2c0d4d850401ab232c5522418f5917fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e55127375c42a52b0cdff321d3068ce4218382ea8fff382d9c06f2bb5e4ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:cd57ae2ab2536c11a7278b0c95a35390548b7f0193da23d7d84177e4d7cf0d48
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
$ docker pull buildpack-deps@sha256:bf1693622639614d7b51fcd557f2fec6d0ef45ebfad0c564cc2b2cf4c2f20ac5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245813153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e57f6349bebbf2a428b64e05e30e1452edf15c7d243fffdeebd6c6236495618`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:22:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d5b87a1475cb2bebd4a61e0e510c509560007aae9a127bb2e2a3fbcae76366`  
		Last Modified: Sat, 17 Aug 2024 01:31:14 GMT  
		Size: 11.1 MB (11133643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c879a37493b932706443549377060adf5849bd3e29c8fb34c4dfd2778dc1f30`  
		Last Modified: Sat, 17 Aug 2024 01:31:30 GMT  
		Size: 60.9 MB (60928764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98010dc515f7ff2be46b7513048e5c34d9377fc6a095ee86a755e499cb45ff7a`  
		Last Modified: Sat, 17 Aug 2024 01:31:56 GMT  
		Size: 145.2 MB (145166523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ec9fcaf7094b2237811dc6b2b9a0d4c73215c022acb086c50ade9023d3614317
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732aa4089e3b70bb63e38ec6814220cbb6eeaf82f5813b48e759889d54cc7962`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:18:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c44db121413be01c8efff606c5352913b04ea7d55ee9de266ca29e99f87a2`  
		Last Modified: Sat, 17 Aug 2024 01:29:02 GMT  
		Size: 9.6 MB (9606860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb0f6813a18000ba2cb151eb902bcefa325c57d600f5b2984b4d714ff817f3`  
		Last Modified: Sat, 17 Aug 2024 01:29:18 GMT  
		Size: 55.9 MB (55880086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5303ee8b4e59213cb809629d6ed390394c4c2b1765b8b01d2821ece8009c8b1f`  
		Last Modified: Sat, 17 Aug 2024 01:29:42 GMT  
		Size: 122.0 MB (121995770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3560e765fa6616970f9f436aa030ef20183457c2cf776cfe92388daf7a7695fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236090788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb726f00c17be72618aa4dffa20c2733a05a6e4b8a9f7613a225d1ab74aa6c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:14:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4364aa85a5a14128c7776ea4c23fcc57b40e56f723c123e3cadeeecd0d8be2dd`  
		Last Modified: Sat, 17 Aug 2024 01:24:35 GMT  
		Size: 11.0 MB (10982873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39beac17021b4ec51b652179fb388e7e59592ce3f5ed20929fdbf26ef4ec509`  
		Last Modified: Sat, 17 Aug 2024 01:24:49 GMT  
		Size: 61.1 MB (61055242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3146142e7a6e9c2d67b7df46b7b7f5d444be67ae3811abe7930cdf5535b23e0`  
		Last Modified: Sat, 17 Aug 2024 01:25:13 GMT  
		Size: 136.8 MB (136847429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b884c241172d9d8ab634d137b51ff711e3f9d34eaada09d00957e39165b9c7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269570472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877a3c50c4d46dcd80b4fbf7ddc15e07d8519eb0fca42540d5ed757a57e94f6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:32:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd820297f3a00612ecd6f1ec3bd3e61123757fbe396a2cfae8b72f4c9c3aa0`  
		Last Modified: Sat, 17 Aug 2024 00:45:41 GMT  
		Size: 12.9 MB (12942071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac4e3b1bd2a4b79796a1da959333bd0d81548cbdfc5a17698fecfed1c641eb`  
		Last Modified: Sat, 17 Aug 2024 00:46:02 GMT  
		Size: 69.7 MB (69666130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46328d3b2d6b1b48d29412e39ea3baf09f40da4b405f70b4c0933ca7f3957561`  
		Last Modified: Sat, 17 Aug 2024 00:46:37 GMT  
		Size: 153.6 MB (153646151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:48d4d71cd62bc6344df0ee99ec9dd32a28d1521e0afd5fcdeb42ece679d71f4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226610931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bee57d9186d59476c20f53641c8bfca2c324fd7db6bf2e2fbb15f54964059ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:39:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8558e11a11831e23888e185bc022adc3e2a26aaa954ba10de957e7cb3719`  
		Last Modified: Sat, 17 Aug 2024 01:49:35 GMT  
		Size: 10.7 MB (10690160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4161498da3a2456c6b02d48ff2531a9fa0ed9d922edc7bc5f5c812347f644991`  
		Last Modified: Sat, 17 Aug 2024 01:49:49 GMT  
		Size: 60.3 MB (60339016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef7e14bb5b2b64bb51f343306326f543bd4525cc7cf20de8f7918cda292aefa`  
		Last Modified: Sat, 17 Aug 2024 01:50:10 GMT  
		Size: 128.6 MB (128568337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:e4007830688c72c63f9a1c9dbbea008ada3f0cecd692d53d69831b3970c77334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:543dcdb8e4675b69377e57cb70705ceb2c9f02d1ef38cee8fa58b78bafbca179
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39717866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1fadd79005d87467388f766899da33502c249ffc40d19ff2bfe22c202586f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d5b87a1475cb2bebd4a61e0e510c509560007aae9a127bb2e2a3fbcae76366`  
		Last Modified: Sat, 17 Aug 2024 01:31:14 GMT  
		Size: 11.1 MB (11133643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf7ba37697834a257c8552c0e335ab190cd10b7168298dcde5b9db5e97a39b18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34210681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0627b1ad06d51d3d87049da3bb58897d4fb4bba1a4f4e5b6511e69801dff2669`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c44db121413be01c8efff606c5352913b04ea7d55ee9de266ca29e99f87a2`  
		Last Modified: Sat, 17 Aug 2024 01:29:02 GMT  
		Size: 9.6 MB (9606860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4d91718ae34e7c67060562da2bd29fbc1789a457e84065b8cb8a09df33014b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38188117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f7bc6d40365e785e8170c1924cfa0c0e155af80c799f4ab704c57b99bbddc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4364aa85a5a14128c7776ea4c23fcc57b40e56f723c123e3cadeeecd0d8be2dd`  
		Last Modified: Sat, 17 Aug 2024 01:24:35 GMT  
		Size: 11.0 MB (10982873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4bd90b8805674433662921e3ed887fb91bbc6eb0b4c32618b0f1c6325fafb078
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46258191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0191540db9246e90617f7c6e8d2ea928cc207e9cf44c8a2495bbe0e17154e73c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd820297f3a00612ecd6f1ec3bd3e61123757fbe396a2cfae8b72f4c9c3aa0`  
		Last Modified: Sat, 17 Aug 2024 00:45:41 GMT  
		Size: 12.9 MB (12942071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24a1e11685862a8d2b943a1fbe00ba330a2e1448c0f154a6c36f8c2145eac29a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33874516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f60da6d80260eec4d7e3a10864e8dbbc5b2aec182b0269299a509de5e46de9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:45:25 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:45:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:45:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:45:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:45:56 GMT
ADD file:e801325f695dfee333234d27e4a3f460f2c87b0489699f1e3315d4b62550aade in / 
# Tue, 13 Aug 2024 09:45:58 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38e511e701a08f7bc3aef62d319fc8ea5dd4ce126a870719810f76ffdb74f7c5`  
		Last Modified: Mon, 26 Aug 2024 23:45:46 GMT  
		Size: 24.2 MB (24249703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379daf9f1fd009398df91bca6e9f7fe3bd97d786aaf5a2ef6e06fa7455011e3`  
		Last Modified: Mon, 26 Aug 2024 23:45:35 GMT  
		Size: 9.6 MB (9624813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7d126aac64329338d47e20f3e07e55d90edd66715567071977ed662d3e08046c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37703578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8f9c3ddd47ee2052f1131103ce0d906f296bf5d0c8e1c7d7581ae39724f0d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8558e11a11831e23888e185bc022adc3e2a26aaa954ba10de957e7cb3719`  
		Last Modified: Sat, 17 Aug 2024 01:49:35 GMT  
		Size: 10.7 MB (10690160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:7009735d9e9364f666ea8ba53ce9de337509bf7f08b86b5fed5f1edee90cff54
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
$ docker pull buildpack-deps@sha256:ab7f61d9ecf51804a5966854943194d47e44b98f6ba8d45ac9147834f65187ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100646630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1dd9bb2d7acf43cc802201d2dde00e149ff8af7cdb68a9279ed4f904c44c5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d5b87a1475cb2bebd4a61e0e510c509560007aae9a127bb2e2a3fbcae76366`  
		Last Modified: Sat, 17 Aug 2024 01:31:14 GMT  
		Size: 11.1 MB (11133643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c879a37493b932706443549377060adf5849bd3e29c8fb34c4dfd2778dc1f30`  
		Last Modified: Sat, 17 Aug 2024 01:31:30 GMT  
		Size: 60.9 MB (60928764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:59b5e39e5da4dc9d13bc2622a16d5b9b315546817c18513c487443de77c7765c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90090767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d145582d134fa5fd62627f8bba5579f49c707fd915e596ac45e8754dfcb75173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c44db121413be01c8efff606c5352913b04ea7d55ee9de266ca29e99f87a2`  
		Last Modified: Sat, 17 Aug 2024 01:29:02 GMT  
		Size: 9.6 MB (9606860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb0f6813a18000ba2cb151eb902bcefa325c57d600f5b2984b4d714ff817f3`  
		Last Modified: Sat, 17 Aug 2024 01:29:18 GMT  
		Size: 55.9 MB (55880086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:470cb82eab9c13f5c9abf92ad48923c6f4f5bb4aeb845c87f6e348e2d76f0c58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99243359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9254e12c5ebae17d5e08583286e495e6fb066b31a81edec524b6bed847f7a742`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4364aa85a5a14128c7776ea4c23fcc57b40e56f723c123e3cadeeecd0d8be2dd`  
		Last Modified: Sat, 17 Aug 2024 01:24:35 GMT  
		Size: 11.0 MB (10982873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39beac17021b4ec51b652179fb388e7e59592ce3f5ed20929fdbf26ef4ec509`  
		Last Modified: Sat, 17 Aug 2024 01:24:49 GMT  
		Size: 61.1 MB (61055242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:587093fa59e291b2e93393714dd0602a3b5832fc8f0b2eb6f026567c722e3807
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115924321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c280a99103ef064c559961e89984563474d74e528b43846ad7157dc36570490`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd820297f3a00612ecd6f1ec3bd3e61123757fbe396a2cfae8b72f4c9c3aa0`  
		Last Modified: Sat, 17 Aug 2024 00:45:41 GMT  
		Size: 12.9 MB (12942071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac4e3b1bd2a4b79796a1da959333bd0d81548cbdfc5a17698fecfed1c641eb`  
		Last Modified: Sat, 17 Aug 2024 00:46:02 GMT  
		Size: 69.7 MB (69666130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:36f6b49833d078f1d33ff183c902ec25b4ec5f1608a9d80ab42a1a2d2ca92503
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98042594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1d76f41b71565cc55898b6507e07c63598ce49867de9c22e757c2f297a969`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:39:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8558e11a11831e23888e185bc022adc3e2a26aaa954ba10de957e7cb3719`  
		Last Modified: Sat, 17 Aug 2024 01:49:35 GMT  
		Size: 10.7 MB (10690160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4161498da3a2456c6b02d48ff2531a9fa0ed9d922edc7bc5f5c812347f644991`  
		Last Modified: Sat, 17 Aug 2024 01:49:49 GMT  
		Size: 60.3 MB (60339016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:f94d4ac32b86b5e47c8309b8bde444d2b1ac185c515ee28ff4ebad588b0f21a5
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
$ docker pull buildpack-deps@sha256:a396fd7b825e12db08385ba54a8e5d17b12d7763e0b5db605ee5cccd236e6278
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250125255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5243157ef580dc6b962baf1d1e3cca36554b300e92223a811b2141027f9d4194`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:23:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:26:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d48c0031858d2d5110443ab36636bb43de1b4f9563d5121d289db6d7f72b40c`  
		Last Modified: Sat, 17 Aug 2024 01:32:18 GMT  
		Size: 39.5 MB (39461389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64250174469444d1b75872928fbe6818c56d6048cb5dca703b136af150046ee`  
		Last Modified: Sat, 17 Aug 2024 01:32:47 GMT  
		Size: 173.1 MB (173131517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a12f7b9a6f8b2f40a9d9efd6a7d42d7ba7f9fc908831857963574d2c1089e45b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217369666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a676edd37e9e7fa74a9ae9679a9e0087c55e5b10f6bc015b55fe1351b0e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:23:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facb95feeaeeb475846b3b20ee6a1f49fe09ff11e6be5c51044287df974edd6e`  
		Last Modified: Sat, 17 Aug 2024 01:29:51 GMT  
		Size: 7.0 MB (6992292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dac84cd042e2f25b48491d3dc0d9e796a7c229b7e09eb6f7e5368e97885a6`  
		Last Modified: Sat, 17 Aug 2024 01:30:07 GMT  
		Size: 42.2 MB (42244605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc3d603dc51fdb36b23fe9014cf77cf1634b7886703af66327a6a3222208086`  
		Last Modified: Sat, 17 Aug 2024 01:30:34 GMT  
		Size: 140.6 MB (140597719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:debf3598205a32dbb3829aba26eb6aae66c9a0d80ee126dc25ac1dfc2215956c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241399470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cccb2121d73f6ba7129795cc4a205fa76c2e70e5077a882d4d1aa8f2976e19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d7e3e6589ca2b01d191dcd38e16911631b1c1ecd6d6a1b19725adb25bcb33d`  
		Last Modified: Sat, 17 Aug 2024 01:25:35 GMT  
		Size: 39.4 MB (39382817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b3fa84bfaf4c88e61f4c2f8463313a09d480bee9d645c6c985bbed278ad01`  
		Last Modified: Sat, 17 Aug 2024 01:25:59 GMT  
		Size: 166.6 MB (166586020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:29b40fd42cc6f87f2bab315b49a247720758dd3b20daf66fafc0d8e3fad62e5a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271178540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03eb1be347df2cbf52a00aaaef1d912274de4d2dca1447953005d091a91145a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:38:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e29f857d015b0cbd97132074499724818f965d9a1d1390e861faf881b42a4`  
		Last Modified: Sat, 17 Aug 2024 00:46:46 GMT  
		Size: 8.2 MB (8190468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5792bb7235062f0d15f661a3f95bf8576db3f4ce19571f3c267126a3c7bd9069`  
		Last Modified: Sat, 17 Aug 2024 00:47:08 GMT  
		Size: 43.8 MB (43762057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a345e3cd75c476690515018f7406086ff6bc6b9d6d9143e614b5360d4f6c`  
		Last Modified: Sat, 17 Aug 2024 00:47:43 GMT  
		Size: 183.6 MB (183638371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5fed60b701ca50e50f9d91d1978511824521955643fe0bcb9791a0702314d9e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274995693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a4ab7dac9668b13a456ab8594ef91edc86d446b92d636316a277c14587c69d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Aug 2024 23:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Aug 2024 23:33:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:294ed87c40f8cf1413b3239e9975c38b12851c23334c529e90fa3e66d8f9f7e4`  
		Last Modified: Mon, 26 Aug 2024 23:46:16 GMT  
		Size: 27.7 MB (27710015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ace411d40322925822a30951a8290f84a11b834aff42c4227e9c888e6361`  
		Last Modified: Mon, 26 Aug 2024 23:46:02 GMT  
		Size: 7.1 MB (7100644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac83254f47c5a724e33abcf115362b29bfe72cd30c65493e9ac149d51093ee6`  
		Last Modified: Mon, 26 Aug 2024 23:47:08 GMT  
		Size: 42.3 MB (42311519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d94c75ef45ceefed0016875844a54b4a5e12e38e6ebb9250a26bac49f668f4`  
		Last Modified: Mon, 26 Aug 2024 23:51:07 GMT  
		Size: 197.9 MB (197873515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:970430e975f7fed83986a5dae6f95a27c5a4f5b6ead048ad2398e7750bc74f09
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223844496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e497765afc3c27c37895408c78c108f628e59ceeb542cc836ed3139da0e41536`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:43:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:45:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c437abab0275e6e3a6dc85400e2dd6035a546805afed5be0790bbe780fa2aa`  
		Last Modified: Sat, 17 Aug 2024 01:50:16 GMT  
		Size: 7.0 MB (7003356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43ea6d3e4350aa4d9b05bfac88decd19c457b21aa1f2b46407fd5895421b095`  
		Last Modified: Sat, 17 Aug 2024 01:50:26 GMT  
		Size: 39.4 MB (39416903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a20c48c231bd78419ceb6c8a4fe183a35d4402af1f5c9c03d0c6bc5cbfde34`  
		Last Modified: Sat, 17 Aug 2024 01:50:49 GMT  
		Size: 148.8 MB (148785734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:6c1c0223866007184103547fe530a16ec4866e76f951ab46d77f04fb5327778b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:901890331f06331c1caf4d640bc0399a918fcf967f2d09222118072fee68ed47
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37532349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0cce36c8ed8dedd75830a5c97e06db0c2f598b01af0e6de2a27eccab75b12f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4d25f50812748a1e7445db2eedb7a70b4be96b8af52c6db9c2768274649c862e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8487b734d1c640503adf958e48a743d5c0e4ce2e6964882eeb973729724761`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facb95feeaeeb475846b3b20ee6a1f49fe09ff11e6be5c51044287df974edd6e`  
		Last Modified: Sat, 17 Aug 2024 01:29:51 GMT  
		Size: 7.0 MB (6992292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f9cdcf11df92a79c36fbb45be15108fbeaaed05ebb445c20a63169f19d18f3c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35430633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e5393f0d4ce9c80a07a767186740b4a4235b067393a58080fca7c5806a44b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:225b091fa10b0a2cf0fe8996232873a82e3cbb68a1be60ab03424c969b3fbbea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43778112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f733f9ac26e356e2b82fd49785948dddfadd0f9bce2f00cdfbaeac48ca532245`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e29f857d015b0cbd97132074499724818f965d9a1d1390e861faf881b42a4`  
		Last Modified: Sat, 17 Aug 2024 00:46:46 GMT  
		Size: 8.2 MB (8190468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:31015f4795d4d614f41e9d19c75d23abdb5ac339d3dbb74d4e09eaaca5efdba6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8b253ea5d99eb7aef8bdd08de84376c39254e3c3f1753e73cda20919d3d524`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:294ed87c40f8cf1413b3239e9975c38b12851c23334c529e90fa3e66d8f9f7e4`  
		Last Modified: Mon, 26 Aug 2024 23:46:16 GMT  
		Size: 27.7 MB (27710015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ace411d40322925822a30951a8290f84a11b834aff42c4227e9c888e6361`  
		Last Modified: Mon, 26 Aug 2024 23:46:02 GMT  
		Size: 7.1 MB (7100644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:07790c7c9d9e68a7b881c7f56abc6f808b99b910e7a785f4ab77f9ff1e596342
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35641859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda44fc20438c945c9055592ea2a740fef4765074d09a0d730bda4e73044eec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c437abab0275e6e3a6dc85400e2dd6035a546805afed5be0790bbe780fa2aa`  
		Last Modified: Sat, 17 Aug 2024 01:50:16 GMT  
		Size: 7.0 MB (7003356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:c43e80c35315b693c7d14b4e9608895e28361237b35ac959ada11e533fc3660a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:698f64014507b56ee2d366b2a8a96c5cde7860defc92b291af6203f0b017496e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76993738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff9e0089988e6903f9eedb1f01c84f4c0fd6cd503dd3c9af67b82ad8ac3d60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:23:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d48c0031858d2d5110443ab36636bb43de1b4f9563d5121d289db6d7f72b40c`  
		Last Modified: Sat, 17 Aug 2024 01:32:18 GMT  
		Size: 39.5 MB (39461389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ce09b9f813c75be557f135c80174a3d9f72430076bcf68150bff69b7dae6eb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76771947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12b0f1c0b7272953ccc51b50f8dbf4aee9a7bbd7f9897eebb2bca87396de09d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:19:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facb95feeaeeb475846b3b20ee6a1f49fe09ff11e6be5c51044287df974edd6e`  
		Last Modified: Sat, 17 Aug 2024 01:29:51 GMT  
		Size: 7.0 MB (6992292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dac84cd042e2f25b48491d3dc0d9e796a7c229b7e09eb6f7e5368e97885a6`  
		Last Modified: Sat, 17 Aug 2024 01:30:07 GMT  
		Size: 42.2 MB (42244605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:efab8f1cfdb230f6e65f3dec3532cea57049d37b987b44bc7a9155e1703f4d12
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74813450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd51ce3b8f9d1c03500aa82e6f0e2bb3198321cccad3546e69ae9f4a551a2d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d7e3e6589ca2b01d191dcd38e16911631b1c1ecd6d6a1b19725adb25bcb33d`  
		Last Modified: Sat, 17 Aug 2024 01:25:35 GMT  
		Size: 39.4 MB (39382817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c2ff96617d783ada9cb33c533847c5b23aa55acff44899f15aedae650b514a4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87540169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2444144ae15c8970970bf8799ba611cbd99cf51034436dc7d775fd844ae86df9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 00:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e29f857d015b0cbd97132074499724818f965d9a1d1390e861faf881b42a4`  
		Last Modified: Sat, 17 Aug 2024 00:46:46 GMT  
		Size: 8.2 MB (8190468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5792bb7235062f0d15f661a3f95bf8576db3f4ce19571f3c267126a3c7bd9069`  
		Last Modified: Sat, 17 Aug 2024 00:47:08 GMT  
		Size: 43.8 MB (43762057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6e3db9770d82d45db88df1d36723ce265c7965fc8c6606eacd80eca91ba603e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77122178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b223cbdb8c5546ba9ed89b715ae297a96f33bb77038e2e6f8224802562fe354b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Aug 2024 23:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:294ed87c40f8cf1413b3239e9975c38b12851c23334c529e90fa3e66d8f9f7e4`  
		Last Modified: Mon, 26 Aug 2024 23:46:16 GMT  
		Size: 27.7 MB (27710015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ace411d40322925822a30951a8290f84a11b834aff42c4227e9c888e6361`  
		Last Modified: Mon, 26 Aug 2024 23:46:02 GMT  
		Size: 7.1 MB (7100644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac83254f47c5a724e33abcf115362b29bfe72cd30c65493e9ac149d51093ee6`  
		Last Modified: Mon, 26 Aug 2024 23:47:08 GMT  
		Size: 42.3 MB (42311519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d680df10b2d49e7e257e6ce7fef8083c386873a5d9176e4f0e4202aa09f9d231
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75058762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3b6a80a663c6b40f8e3fcf49fb64d1803dd93a4689404de3be6122cbc03dd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Aug 2024 01:43:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c437abab0275e6e3a6dc85400e2dd6035a546805afed5be0790bbe780fa2aa`  
		Last Modified: Sat, 17 Aug 2024 01:50:16 GMT  
		Size: 7.0 MB (7003356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43ea6d3e4350aa4d9b05bfac88decd19c457b21aa1f2b46407fd5895421b095`  
		Last Modified: Sat, 17 Aug 2024 01:50:26 GMT  
		Size: 39.4 MB (39416903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:3482f48a94e991a648afa7e928a52800e8d9de9135b7cdf1e0afd895f2e0e1dd
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
$ docker pull buildpack-deps@sha256:36c2f5ea2f2ed1af1a446e2a4b9c0581b2e9f6426c9c666c302f3f9da33d9233
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349024496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68e5df27df86c2708cfa83cb52ccb6743a7e33e15c08e881e1a7b139e17eaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9f466c772c63c0e404781bd892c92479011664bf06f3cef798537d746b179c6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316100401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493e5bda9d497e34a2368597973d59f8726156a38ca2253594f5cc160dbcc44`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29df05d41a6c52dd0e5bf38b1bd02aabd071cdfc47e5db769d4f8027cbce9b07`  
		Last Modified: Tue, 13 Aug 2024 01:30:40 GMT  
		Size: 184.5 MB (184530610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14bef58de028be12d34b7d805db521356633a00a79f137bb9f3b40507b15c1cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301543748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a3d866e963713e2b0df1ca898afeec6d371ecb89003a9583c5eeeabe181b8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf1b5402e12f0e97f96b3da218271b7caf2abf4a321ce82a42bedc2d72eb82`  
		Last Modified: Wed, 04 Sep 2024 22:36:55 GMT  
		Size: 175.2 MB (175209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86e5ce1c1f020479b72379683bbaaba7231a8116d5e7c58f2296616614edfa2d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339829397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71f840d8ec66950efb66641927297df50dfd31df6ac0fca91b03f94b6dcbbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:02:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c2a8d94613f34ce7d0ac4fd4e51800d8f4aa8a0bc9347fe5c8436b4c3bd5`  
		Last Modified: Wed, 04 Sep 2024 22:08:46 GMT  
		Size: 202.7 MB (202652028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c74dfe011eb174893ece8c3425af9325b29bcf3b255dc6e801e51559d7e4fc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351614656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bd62f9c712d1e81e60de9dc0a2e3a0204625ac0827903ce83fe542f65e3bd9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:06:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:80c1fa486a8fe97ada53cf595bbf926961ccd26376ac7b955e202996f7c3fcce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325968669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ce2a7a0bc3c2b559803f3b5f224da10915c34d06666b56f5c7c5398f56493e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93661e8bade5668baa650e17db139abcf2b722965a5fbccb9f55952cf3a58f`  
		Last Modified: Tue, 13 Aug 2024 01:34:16 GMT  
		Size: 189.8 MB (189802742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e1e4dc245c2aa0f0dadb1aced70100a855dbb67c14f3ea00f313201d7391b80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363098887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199ffe8f176fb39cd04f4be9dc7085de14b523d0334dab77db8947fe524ccd88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:22:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:245b9b0711a7536d1e01d84674d3150ed436ded567d718c318ed6f0991c7fdb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318370851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11952f41cd8b223618a6668fc853d395c9ec9cbe84e9f8096e511a00a6696512`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:d1efe49d2a055c28dc6ccb292899eec33018a29fe267765b43a41f10eb5865e4
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
$ docker pull buildpack-deps@sha256:dbfee7e7ee2340b0d6567efd3a8a9281ce45ee78598485b4d7a7f09fe641811a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279787125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c54fa271c5fb3ca0e18e8011847ed2e9cd8c033b1b6ffc67eb41e9f18193a65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:30:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1ca6bfd59b4127ffec4664a8d1e54ea862180100d40aeb40be3f042b8780af`  
		Last Modified: Sat, 17 Aug 2024 01:32:56 GMT  
		Size: 13.6 MB (13615674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5776cc91e40203afa47aee5918fda211d15a380be379e60770d3186c2bbdfa`  
		Last Modified: Sat, 17 Aug 2024 01:33:10 GMT  
		Size: 45.5 MB (45476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe981aa2513ef31d687e87f7466c92065fb22c8c3a1f3491b89b552b1ad65fb7`  
		Last Modified: Sat, 17 Aug 2024 01:33:42 GMT  
		Size: 190.1 MB (190127690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3fe36aff5ed130ddfde72ab3e8f2ff5a91b142f9b986e6703ab30e426fa2109c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240043505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b943ca2d91c0f7fd97f07b9a99922c68242be969ceae8cf5c7d6fe8fe07ef42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:28:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c6e3ee23495dde6aacd7387cda5d097d12375226029008e2458cbfa9ed0d6`  
		Last Modified: Sat, 17 Aug 2024 01:30:43 GMT  
		Size: 12.8 MB (12773383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb96a6a812e45055b7676e783359615606d9732634a27fcc8e5f90dba0cdc38`  
		Last Modified: Sat, 17 Aug 2024 01:31:00 GMT  
		Size: 49.0 MB (49021511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d8b9c6bc43d5558a2b951ce712a06393e8335c8e10d57912e67d7f52176a2`  
		Last Modified: Sat, 17 Aug 2024 01:31:28 GMT  
		Size: 150.6 MB (150559371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f454e252cf6d2a1fd13ee819afb58768a6510bd1b05c8c2ea7e5f188c491ac1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270882007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd3d542d4445328bb8f18374ebddb0f5997669f387947b7c37d277cf84c0a69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:23:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a012413ccee10b0979cc0a8a4dbe55d3b3d7da3ab29297f5f9c123b2b126a4`  
		Last Modified: Sat, 17 Aug 2024 01:26:08 GMT  
		Size: 13.5 MB (13452136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3fc2143112f81cac57d899b6b74e9823eacdb070d57fe48697e0476d5b7922`  
		Last Modified: Sat, 17 Aug 2024 01:26:22 GMT  
		Size: 45.4 MB (45429639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fd0de2c4b08430014c443872339edde35b841e197e3f9700b472c466a61430`  
		Last Modified: Sat, 17 Aug 2024 01:26:47 GMT  
		Size: 182.1 MB (182090203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cc5114d6a58e74589c75ced266bf04b778c33f883d50b326435d025a0ee02de3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299140106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3366172af3c194b5390ab31a9a6a902e332eb1ec203282a31dcf787d5a188d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:44:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b02f58c3bb9b5e807e488d763aebfd412e5c890fe7395af264f03013905316d`  
		Last Modified: Sat, 17 Aug 2024 00:48:14 GMT  
		Size: 50.7 MB (50713751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ad33d7385c0e28e8c738c1308b8fa4b34b109adf7fd7fd112f9d0cd58de69`  
		Last Modified: Sat, 17 Aug 2024 00:48:54 GMT  
		Size: 196.8 MB (196800287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:343ce2a2f7835b6e472455fc20d62f4b1bc0a8ba882302865daa7e88d945cc23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342710842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12de875f5f9606da9fee429ae26a9abe9f14926b260f6ce8e88bfa8310c546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:39:04 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:39:39 GMT
ADD file:75a3b8c8bc557fdb66bdc49a2a84206986fe15571577feb7dd59c28963aebbe1 in / 
# Thu, 01 Aug 2024 14:39:41 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 26 Aug 2024 23:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 26 Aug 2024 23:44:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7cf048cdc1e6ca12f1a2101771d1217b7a6c3a2045516b5d28e4ff96223fa106`  
		Last Modified: Mon, 26 Aug 2024 23:51:40 GMT  
		Size: 31.9 MB (31898096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea2c157a2f80b8dae691e1a22d4a573cb68674124557f3dd115c9d90a0ed3b`  
		Last Modified: Mon, 26 Aug 2024 23:51:31 GMT  
		Size: 16.4 MB (16425854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52773e5ffae3bd09a6127cf2a4d2a1f83184ff591ae56ece2f1e530020bed073`  
		Last Modified: Mon, 26 Aug 2024 23:52:35 GMT  
		Size: 53.9 MB (53929997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3ef92e2f61ba657d4f35753d47bd810ffbacf0c0fccd43bb62ee4446badbb9`  
		Last Modified: Mon, 26 Aug 2024 23:57:07 GMT  
		Size: 240.5 MB (240456895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ba2226ac5d3ba5e49f1642fc0dcc05023352cfbbaa010cfedefa131876e99820
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262190525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836608c2e7df5618cab581fc05e38837074a184a85b1db14bc487d1c659910df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:46:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:48:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042bd266644c5e20fcd21cd963b6af3a4f42327bce19ddb3c7f6be5cf1465c5`  
		Last Modified: Sat, 17 Aug 2024 01:50:56 GMT  
		Size: 15.0 MB (14988257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d49ef9b9b276d1eaec35ac35644a2dec74931b57d891ca0cf93f7dc38d487`  
		Last Modified: Sat, 17 Aug 2024 01:51:08 GMT  
		Size: 47.1 MB (47114045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0769f3c11079252bed91efd5483db844a62961322eddaf3d249ad00da37b6`  
		Last Modified: Sat, 17 Aug 2024 01:51:33 GMT  
		Size: 169.4 MB (169395899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:77996a99be212be2be1c121960fca37fc891247b1266b604662c50bddcf89372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:79dd12360d2c69fb1f4f12c8f3d17f7c9f42e23a7c442b4415f50e8ebd77014d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992a8debfe0bed9089eb69a260383021bce2ef2bc09ad4b816b99cf6b5c26572`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1ca6bfd59b4127ffec4664a8d1e54ea862180100d40aeb40be3f042b8780af`  
		Last Modified: Sat, 17 Aug 2024 01:32:56 GMT  
		Size: 13.6 MB (13615674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6ef36dc65396dfa5e2211df2d441eb3a1d376744fc0ad7c44eb460646487b72
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40462623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc46af37225001abb4475256b54906ad24be323206fe6aeafee63a4e15465be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c6e3ee23495dde6aacd7387cda5d097d12375226029008e2458cbfa9ed0d6`  
		Last Modified: Sat, 17 Aug 2024 01:30:43 GMT  
		Size: 12.8 MB (12773383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eb483f89c5551848b2bdb2a113d25d70324dc18c8e2a30ecff379d780a720402
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43362165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6650bb4f0519da0766241c5686f2c9a2236edb645660c9cc8adf9b384774c6dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a012413ccee10b0979cc0a8a4dbe55d3b3d7da3ab29297f5f9c123b2b126a4`  
		Last Modified: Sat, 17 Aug 2024 01:26:08 GMT  
		Size: 13.5 MB (13452136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:939db20dfdccb4508129df097660aa6b8b1b74b8e5a9235f04e6e7bd8bdec00a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51626068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a407552833b5b43c46a6ebec6a71906f514b2f383acf027d8ed2aec6b40ec09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6333be5c165a9c25f7432777d2f5c947e6a2f52dcd21449c2084d6a2ac5c1216
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48323950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c345e12c9db2111f673a3511723995d50c278fed4f44b2d38e4869a67103d81b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:39:04 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:39:39 GMT
ADD file:75a3b8c8bc557fdb66bdc49a2a84206986fe15571577feb7dd59c28963aebbe1 in / 
# Thu, 01 Aug 2024 14:39:41 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7cf048cdc1e6ca12f1a2101771d1217b7a6c3a2045516b5d28e4ff96223fa106`  
		Last Modified: Mon, 26 Aug 2024 23:51:40 GMT  
		Size: 31.9 MB (31898096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea2c157a2f80b8dae691e1a22d4a573cb68674124557f3dd115c9d90a0ed3b`  
		Last Modified: Mon, 26 Aug 2024 23:51:31 GMT  
		Size: 16.4 MB (16425854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:61b6032f68e20dbce644cd1233623d2f60f0c6930dc5063d4ac064ea8d9c50ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45680581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6014e9474dbcc7c8c553d72aafbbe058ff7411a6971f5f6fff6f253a3e34bf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042bd266644c5e20fcd21cd963b6af3a4f42327bce19ddb3c7f6be5cf1465c5`  
		Last Modified: Sat, 17 Aug 2024 01:50:56 GMT  
		Size: 15.0 MB (14988257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:bed3d809d5cbccf0f5f9ed8b0930d6d73e974bb00c520050e2fddf1734108eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:534ad44c162160c9365023ed328da30f02c5b771e649fc37581a9ba61ced6d19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89659435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771021b2c4cdea239fa2c1a6e7d1f2f770e7838d65795ce316a09c8388984466`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1ca6bfd59b4127ffec4664a8d1e54ea862180100d40aeb40be3f042b8780af`  
		Last Modified: Sat, 17 Aug 2024 01:32:56 GMT  
		Size: 13.6 MB (13615674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5776cc91e40203afa47aee5918fda211d15a380be379e60770d3186c2bbdfa`  
		Last Modified: Sat, 17 Aug 2024 01:33:10 GMT  
		Size: 45.5 MB (45476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:246cbc5056ad0bb88b99598f13c40b5457206cc577a5a25f4dca5dd6916fc323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89484134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b610a682eb0a03418ed50058a521c1f1953e2581b96a929de0f73c7b8a083d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c6e3ee23495dde6aacd7387cda5d097d12375226029008e2458cbfa9ed0d6`  
		Last Modified: Sat, 17 Aug 2024 01:30:43 GMT  
		Size: 12.8 MB (12773383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb96a6a812e45055b7676e783359615606d9732634a27fcc8e5f90dba0cdc38`  
		Last Modified: Sat, 17 Aug 2024 01:31:00 GMT  
		Size: 49.0 MB (49021511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6600f12108c07eb81d530685c8bed0f3ab19746a8d7b4d8c021eb8434e82d2c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88791804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e56eb0060a581c8f2270b08792b38f5fbcb79b6698bb8b0a1d62cd4cc4d4f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a012413ccee10b0979cc0a8a4dbe55d3b3d7da3ab29297f5f9c123b2b126a4`  
		Last Modified: Sat, 17 Aug 2024 01:26:08 GMT  
		Size: 13.5 MB (13452136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3fc2143112f81cac57d899b6b74e9823eacdb070d57fe48697e0476d5b7922`  
		Last Modified: Sat, 17 Aug 2024 01:26:22 GMT  
		Size: 45.4 MB (45429639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd44cea5713601b9d67059c57e116e28b331fadcddb64dffd60f12cedfc40923
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102339819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295ecb5a3e55316f1ba417d43ce139c5137df9033cf99f943ab4dd924ecbb00d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b02f58c3bb9b5e807e488d763aebfd412e5c890fe7395af264f03013905316d`  
		Last Modified: Sat, 17 Aug 2024 00:48:14 GMT  
		Size: 50.7 MB (50713751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ceea6ca1c43481f76732c7d3e14bd92c2d6336e332dd5f7d1905ce679cbc7f0b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102253947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03df7edb24fd621f7b915bf4aa8675858e7392e04153e0cedec1fa8015475ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:39:04 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:39:04 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:39:39 GMT
ADD file:75a3b8c8bc557fdb66bdc49a2a84206986fe15571577feb7dd59c28963aebbe1 in / 
# Thu, 01 Aug 2024 14:39:41 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 23:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 26 Aug 2024 23:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7cf048cdc1e6ca12f1a2101771d1217b7a6c3a2045516b5d28e4ff96223fa106`  
		Last Modified: Mon, 26 Aug 2024 23:51:40 GMT  
		Size: 31.9 MB (31898096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea2c157a2f80b8dae691e1a22d4a573cb68674124557f3dd115c9d90a0ed3b`  
		Last Modified: Mon, 26 Aug 2024 23:51:31 GMT  
		Size: 16.4 MB (16425854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52773e5ffae3bd09a6127cf2a4d2a1f83184ff591ae56ece2f1e530020bed073`  
		Last Modified: Mon, 26 Aug 2024 23:52:35 GMT  
		Size: 53.9 MB (53929997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0fed4047a264089ebbfaf4f5afee2d54efa50b339ff5f636b50aa069e455e22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92794626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c19cb866a87617680f1f7b8f5e14167811acc2f6e6173d92d75490d48610dc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 01:46:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042bd266644c5e20fcd21cd963b6af3a4f42327bce19ddb3c7f6be5cf1465c5`  
		Last Modified: Sat, 17 Aug 2024 01:50:56 GMT  
		Size: 15.0 MB (14988257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d49ef9b9b276d1eaec35ac35644a2dec74931b57d891ca0cf93f7dc38d487`  
		Last Modified: Sat, 17 Aug 2024 01:51:08 GMT  
		Size: 47.1 MB (47114045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:a6ae1502d0a7478947fd44eaf824483cd394a3a3a18015cb922c15de1e24b9e0
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
$ docker pull buildpack-deps@sha256:10a4036dfab922ead2cfebd38ad6880fd220be472d07b0ddf78428a548acc74f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322639503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab79b6993cafa55d4bb27f42d4a7d9151d8ff09fd9b00803dff1a6d0d061fa6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:57:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:641f090b8ccaa18cb371821c1cf43252189d3c11741ed51e1fada95c2ee9f288
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295537834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6d84aa0143aba03b59a838196830f2757eca2b5e1c8d03af86ebbffb96c511`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc22013229b56309440bd8fc1d5ea5676b191eef21e7b46a13f701910c56462`  
		Last Modified: Tue, 13 Aug 2024 01:31:10 GMT  
		Size: 52.3 MB (52329471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d1eab0e56c7f5eda9931e89b45d4088957214e10070dd831c5879c06fffcf`  
		Last Modified: Tue, 13 Aug 2024 01:31:46 GMT  
		Size: 175.2 MB (175244246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:803b714c506cda16406db60e38e9dc395c9830311d7c78ba044e1b5e4f867072
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283246496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f5954c9e1191853abacb6effda18c4b5bc3590eb3b29680c31b0377ec40f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:31:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a810222c5e9f2cbfb1260daae6fe81f9c63f9fa8cad05812e717e0135194dd`  
		Last Modified: Wed, 04 Sep 2024 22:37:24 GMT  
		Size: 50.6 MB (50616939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae26722d7d3c0994148ae4ede7eb08ae409fa7ac05c21ff66d41b5f7966fcad`  
		Last Modified: Wed, 04 Sep 2024 22:37:57 GMT  
		Size: 167.5 MB (167509349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e6ad79369b89f3b7e1d2a7a488db0f943067bcec96f234fde8be4296e62d5811
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314276579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a407b93f2f1b9c154892204f16a039161bedf6e8dccb5d4f7951145491f8263e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:04:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2c74c1774e448d6bb324968dd639df704566af4ae9461a86ec79cc6e8de709`  
		Last Modified: Wed, 04 Sep 2024 22:09:38 GMT  
		Size: 190.0 MB (189961799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4f3ebc102ec78f80d2b3055e46bc6df3d9d30bd344701f75fc79520382f5685c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328222990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef63590d9618b3491dd4dffe9c1a4523662c21fed4e57f84fb1e63f1f72bc5fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:09:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29843169a9c8306d94c89194ed26f3e75a8d2afa2d64a020ecbfd7f77998e397`  
		Last Modified: Tue, 13 Aug 2024 01:16:03 GMT  
		Size: 200.0 MB (199953236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:99b1989c136bc87e0ebd9086d96c27cc952fdf0ae2c9ab102e21d08a805ec990
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301518540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597a7a2e07a11e8dc70a7ae64312a4251e2097851bf68687fbb193c706ed0585`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:11:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b3474926636ee8b68ffaabc4b0327c4331cc3894af8f568c64d5f6f1d8594`  
		Last Modified: Tue, 13 Aug 2024 01:35:20 GMT  
		Size: 53.3 MB (53310999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acdb857f86d97c41d9b15b80df1ae493a4f9aa861236fc1b5fbf24ed5257567`  
		Last Modified: Tue, 13 Aug 2024 01:37:17 GMT  
		Size: 179.2 MB (179162196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4327d8a1a81e9755a664e3e15772b180a74b77c376c7d1ceccfdfb87a681bb0a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330991662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745b30ddf4d9d5cd2ce026ff4115c1d083935043473f115237dce720f58f05c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:26:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f036d67ca6dd9f8302ee75fa7409b9e24f1557528c725d1b15a5d8d019aae30
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296102116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c67476fdcfa6533a7f193a889a8ab07789f3354f024f764300e29ebeaf7a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:3708731f454324d6f2a7d2f25e37549896564b18b2907268bbbf168f6e5af72d
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
$ docker pull buildpack-deps@sha256:b2ab43637316a966d7564590785da3116fae87b52b907a5902fac9ea50229dde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466b383277cf6493fa742bf3fb69e36fb7f73ca32ad5144e04b152c941c323a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:95dfb0ec397c71c94c6e076ecb5346340f3dcf4327daa9174c5ba8e40a9d3922
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395d531798cd6c5aa61f96c696b9339f9a6b5fe4519527ae61f07c3a4dd8919c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e7afdad0f3b3df78a5cf51155a52d76832932cd6e03f28fdc574553d70cbd697
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3676be8e05fff3206a23ec525511e61d914a13bdfc8f61c6e84b939e9f3d70a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9f6af9c3ed8f6d7f676495af771260c9613758c38202ce10c30b9eccc2cafdbe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69481331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea0b2da908ed00a3825a18f9acd4a1898d9a20bf6ce8b93885508d458a292e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:11c49d08efb516426e63b794ff0a6a3e6f7d6ca47101c8a0a1382390ddfe0a41
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72342047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e404efea07746cc36cf3c48082a8023e994f30b3e282181c50de52ab22fc787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2e53d71d4de748cbbaa71f785bc60badead1c7dbabe66ae888229af3fbad5d15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69045345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8199f996ed824b9d6d1c8620a66af2fa0254ee49022ba7aa7636e656d9df13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:34ae04276fc096d665517bd951570adf94b0e304739c1cb82528af95fe9363fa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d18f0b36ae6d2807784af58b7b7b01c29288b1a28d21b4f161f88b4d5e801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:34e92b89bcad65835615a813c2e92ddd58c4398b8bb73619ea899ff33ecf2e16
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed06a5a153c1e116f2a080896ef906396f2d8d41d9d263c6de0d56a8667971e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:45f5e141493a46219849c6f6acce6edc74e5804b4650f0a40ee16adc9bd5baef
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
$ docker pull buildpack-deps@sha256:4aef53b9a2eae41c83be8f573280b21013c421e704b19b08312173d0e3e35573
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125571750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b31b3c521a9d88d81aa84171eba30d1f9b198944fdff4b09f8c830a8751dc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a86730fc51beab973cb8add78f2a7e58deebff1e672c01d62614821d77a79a90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120293588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d361f615568448e949e16d27136fe91cd71e9fa15a0c10306291505053e8b45a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc22013229b56309440bd8fc1d5ea5676b191eef21e7b46a13f701910c56462`  
		Last Modified: Tue, 13 Aug 2024 01:31:10 GMT  
		Size: 52.3 MB (52329471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce3b9e370af68730a4b51563bd8e8bdafce6d4eff06b4c3bab7af18aed7cae97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115737147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7d917904ba0aba7a811d8927b48c9d24febc228111d2b66aeab0bedbedc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a810222c5e9f2cbfb1260daae6fe81f9c63f9fa8cad05812e717e0135194dd`  
		Last Modified: Wed, 04 Sep 2024 22:37:24 GMT  
		Size: 50.6 MB (50616939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:25055f990335dc5e442f1da22b05a2229bfa4e780330493c9fc1a0b91c4d36b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124314780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058d4847d703ccb14c228bd019b880f4a587bdf25cb89d195fc24363bdea5c75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2c3044d7a286ae2a788c5b37f5bd2fe6aa0ffbc115851050defffac0fd544962
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128269754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6dbb003a1a505f2070fde5fd98afdca9b926fea0fee1d727d782182c96a174`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:35b801921e609d3209dacf1b5ba52b01de7c3aa9e8aa02c6391d36341e616684
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122356344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcab7119b603616470e424761bd314b03772c99f37bb1c28be22208d5e17e2ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b3474926636ee8b68ffaabc4b0327c4331cc3894af8f568c64d5f6f1d8594`  
		Last Modified: Tue, 13 Aug 2024 01:35:20 GMT  
		Size: 53.3 MB (53310999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b24b3a40397e5e4780ec4987a4c5de21b5a10aed81c711c231d6debb8669d609
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221000ca1ce797c56fce59ac01ef1cd91a243101b30d6d0fec00980d1226a63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3946705950289b1cd5ee35a7981aabd8a53eafc5e536516a12c29dcb83bc7205
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123041240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c52f640c0a850aadaaf7abcdfb8230a8322f73ee3c1e5c69a140e8d7e315c26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:e2ea1bc81a724065d5629534f53d30f60729c4576001bc066aaf56e300ea237f
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
$ docker pull buildpack-deps@sha256:68e358c3c05d520af01b674163e1f5d31a6172366ed0352550d4b5f4001cdfd9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137757873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2581f163f0552bbce9b3a5d33ec03b5f75be04876ea325c1f0a2f936f293fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1d2cb11ccef3f86147133f3dde474766ccae22d038c1498ade71e3d9505fe665
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131569791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efbb3e4bc9ebc13547c5d9944bbe33ee0a59fcfef91a5535a2fc4c3527826e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ef757fc27d5b94c652221e08501ca120f44bc94bcc3eb9b3130b28f91307c18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126334298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833eb6fd43fd38ce68fc4749a0272945c863058498498304d502e076b86aa650`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c0796108d4f0bb51a454428f5166df78cc3e40136a7d253ac1d8beeb85f734e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137177369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0013d72146ac385cfbc7a7ab43109e4916a8e8fba1e0c7aeaad85545273d89a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fc24d91b13db9bea6198bb18d275403768ca62332ea9815b3e91b87bda5b6ec4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128efb528b94818265ba8257926d66c6c6ded4a2257a29e6bf86f4ad39ef4ecb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4d1ee8e4bdbe8b07ec10c0d1115f4e722abb614ca2123f5524e48c3b653f8451
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e0fe59d2d5ca07f6a297b61740fb334b836d66fdab89d2d1c3ae797d7a8cfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67fb44179c22a0a46e18108147c764d2096f18d571fd9b0b90c37a493a55701f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a399ae7695be551ea659c15ec8842777bf6d4db45eca491da16667270d6fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:732c22618cfcd4e8ef5da95054a577ddec7f874e23557a128b01813304bd6048
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ae05d5608df2ce534b0015ec009bbac71560883de2290f6691dcaa8a9588d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:be63c64ee3fd7e0fa9d9330932a9bd46435e015ec6a6f5c1a13715580abfff5c
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
$ docker pull buildpack-deps@sha256:95636449c78c5311c92bb5c04cb71ca71e321e62d9ba7f340496a3e8ea1b6613
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364424180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0886d8c654ee90cd57e0951a093439e8008935828f019928689ca1c412fd23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac0b2d691022b6e9d2a4261f3c3547b5863197743e9544f77779e589aa6a9`  
		Last Modified: Wed, 04 Sep 2024 23:03:29 GMT  
		Size: 66.2 MB (66214670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6946879d70176adc3ffb5837bbaa51b79bced4142aae63dfbde91e5c47b690`  
		Last Modified: Wed, 04 Sep 2024 23:04:03 GMT  
		Size: 224.5 MB (224549385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d01e97fce87eb39b36f37f8aa45312b5a11da5fe5cca14f145171bd8242a1cad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0658cfb7a474590e1994b4a562fa6dabef9db569cd315e4dc4af819218edc3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff253c8c9180c53a680ac594e0b90ace399416d9f322bef4f9a66e3d0fe0c5af`  
		Last Modified: Tue, 13 Aug 2024 01:32:17 GMT  
		Size: 63.7 MB (63717307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e89c01125ee82ab0aa0af47c3526f7864fc2f07adc19ebfe1e2b58061dbb7b`  
		Last Modified: Tue, 13 Aug 2024 01:32:53 GMT  
		Size: 201.3 MB (201294728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:37b6810fa3d1d732d30766846909d30dfab637c900f47d30c4ae3280dfd8c9db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314706112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb90709c7a5e58c2a0ebff4d085a2cfed0066899451050ce3039cd3c67da182`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:33:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b337ebc4882ba5bf1b4d0ef428653fa3a9963e209aefc6227386f1a76b3176`  
		Last Modified: Wed, 04 Sep 2024 22:38:28 GMT  
		Size: 61.1 MB (61148386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f918449aecbe1b94d67117d739aece3a6bc2dc9aea2eecff37a6d4a68cf059`  
		Last Modified: Wed, 04 Sep 2024 22:39:08 GMT  
		Size: 187.1 MB (187105286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e67fb06f6e500129e26b9720fda34f641d39d6830faaee85458a3f5ad6243ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358192533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1708ee9622d0dde1a503c07b7ed6ad4bb182e70bbb6bfd19eef2b2e5d6328b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:05:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ed4283c0e34c1b3349c61e47afaf58a71aecea82db8aee69f2c8a865f8c6e`  
		Last Modified: Wed, 04 Sep 2024 22:10:04 GMT  
		Size: 66.2 MB (66237648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef4fa35fa4ab50f808bb497d29332afec951c4bcb10c0dd0d72bbb720a7932a`  
		Last Modified: Wed, 04 Sep 2024 22:10:32 GMT  
		Size: 218.1 MB (218109327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04cd0e8012a7b0a927453540343a58c40ce7422329b38254cc3e2c0fa5709eb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.2 MB (370192161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a14e845327d478743cc97f4cad35b0845c843799f0201dcea0ab4a3d804b16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:11:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a203d729458242dda28f4795cf80bb88746084ccdc8cce21ba2acd7dcaefb3`  
		Last Modified: Tue, 13 Aug 2024 01:17:23 GMT  
		Size: 226.9 MB (226923306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3b99b1a614b2627c2ee392abf6cec24d6e709a64ff2660fa5dfcff701541b014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343104341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e38cadba3b728e3cc3d2698789e9a516b7fff066fe5de0170975495cb00f8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:21:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b82974da5a3d69a6ca94388b0a3f14e1fe28ce4d21ef9f4032d841f5325b32`  
		Last Modified: Tue, 13 Aug 2024 01:38:31 GMT  
		Size: 65.0 MB (64998376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b138f1bac27906feed7c16ced7bfda41230bd94f4e3fa7fa461b5d556cca85`  
		Last Modified: Tue, 13 Aug 2024 01:40:49 GMT  
		Size: 205.6 MB (205575439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad4b04250fc6a8dfb76563542cd67b13c68bb161c5ae1e30e1821818f90a5ef6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.8 MB (375834614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662c9bbbe195ec285293da4dbb7e93e9ede726496a2364e6f9523f561594b7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172a0ce16e36a34ff88a2732bbe6037759cb39c60616bd29dbc966d3bb79ec3`  
		Last Modified: Tue, 13 Aug 2024 01:37:28 GMT  
		Size: 71.4 MB (71359436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c40f2aa6297d7f1a7d0c5c01d5abdbc3208369127949982cb6b44835f9e6370`  
		Last Modified: Tue, 13 Aug 2024 01:38:08 GMT  
		Size: 224.6 MB (224601465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1f0fb710e4c77f45c369961d8f5ad1b5c3c2d6d6637879b7f0ee0cec7a11e1e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443858778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13763f9c3914a92f12e358871f27bfd1ee3de1d1a8f20a4e5a9c057826caed09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65deb42d9c749a528063c18ed3482c3235a8863523f7fc5d895330b910edd50a`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 65.5 MB (65455674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a959a2b7a253bddaf7fd68b258fe0255968fc0d4f52643281e2ac2de68e19e6`  
		Last Modified: Tue, 13 Aug 2024 00:53:51 GMT  
		Size: 307.3 MB (307284095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:82d3e113ccf2880c3912b85e42057ceef574bf3adbe52c37b776b906b69dd473
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342028696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984dfc489e1f8db6f7dc2248ab5d807b1457996661c87373f320a97a40a6e041`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:21:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c43737168f685110fa0a3c4ec68bd02aecf241fa770d30b263bb78a2ad0f70`  
		Last Modified: Tue, 13 Aug 2024 01:26:30 GMT  
		Size: 67.3 MB (67269243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9eb516daa4ac7451bd5504522258db8cda9841d72e9c32f295c166a2ea370d`  
		Last Modified: Tue, 13 Aug 2024 01:26:57 GMT  
		Size: 200.7 MB (200715920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:4ad0482e3f6e8fe8d8e33e5f70154a64998fb0ced072db19a0e8050d823f9fd1
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
$ docker pull buildpack-deps@sha256:ec2e4ba708bbdf5e0da6788d027041c767bf9165a08a035f94c515e93f12073f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcf1fb70b329c7b917257747d7b2aa74ae8deba8bd35228162e9fc2d3b14dec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f7b8be926f1bd951849a9c75815f36d1c7e532df7497cde939244a305ea7f090
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69311252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34583e63b9066ab656cf7f884c618cf83e0903e526aec63de39a9e145253044`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:51f16b2b3c891eca8cefaee1e8f70cf3c8e049d4feb44152aaf3b4d2221ef4c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66452440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ee032b74216acc8825fd7595e837b592eab1b9ad1444d64b0e16ff032a039`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e75ffb7a2e7f4ad78b5eaaf80f80ceee80cbd1c4b9a765b3eddd34c903a3b5f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73845558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea665e856755fa51885b312d1ce870241400d83b9292e1f1436b26cd6b56621`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cb5e40a7be972b1172bafa92ab71f6a08c143e06b0981336a4bc4d8af23400cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75244435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d80a37e21c9e25d3737094c1c4b40886ed52181492e44fdc9dfbddf970ee8f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84b61ff5dbbeb62166e032082928afcd108dec8f874958c9c8dcf6799ca93767
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72530526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c4826139623ef2ef60d33d9f29bae5ba7e34385f1be56999cb44c59b995631`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c4be7903db01dfd7116ff52391f931caac99a1be00c70abf81dd84b7d4272b4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79873713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d224a800248ee906a9bc5cb5a7b1509c10a69fb16353a6773e668aba67d0956`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3215f819f7c134ef7f6419c2df43620029c30939b449a8d4cc7c62d3a946e8aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71500653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efed2f8783057bc14f79d6c2b2bd765819525f1d9769e0423b347a7d07e51f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5d604130680eacd1da47d3bc2917df80e404d80e5f62bf34ea52ddaf846a16b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74043533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39594b5c80df5065e24356bf1588fda37b42791ffcde078d45147ead22f0ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:d4f5dc5df3b19766ea24a3ca1399822f55f43ea67560ca6058df3fe558b49912
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
$ docker pull buildpack-deps@sha256:bfbeceb6f6ba6391d6267f489ea26bc2f67a55ddd1d74db872565ccadad3eead
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139874795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f69fc30003a7b48eb1d4b267523478260d578d8bb232cc6cdeddb9228c6c6b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac0b2d691022b6e9d2a4261f3c3547b5863197743e9544f77779e589aa6a9`  
		Last Modified: Wed, 04 Sep 2024 23:03:29 GMT  
		Size: 66.2 MB (66214670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ed6500bcaea8b4c9ef0e46757565bc33aa4560e04e9b55175c0f215c480362f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133028559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ab093fb96c9708f9b4d2373530572077367c2ba35bfc1989e780f50b8e07aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff253c8c9180c53a680ac594e0b90ace399416d9f322bef4f9a66e3d0fe0c5af`  
		Last Modified: Tue, 13 Aug 2024 01:32:17 GMT  
		Size: 63.7 MB (63717307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:58eef75c65666ab0c1901a5ed3926cc420503406798bf43b3bcfb595fdca219a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127600826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5592be70d2653aafa4fd4e8efb48fae22c8c7c92d8c9b0a0073e302f0f939`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b337ebc4882ba5bf1b4d0ef428653fa3a9963e209aefc6227386f1a76b3176`  
		Last Modified: Wed, 04 Sep 2024 22:38:28 GMT  
		Size: 61.1 MB (61148386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ecd47ce655417046236fa338583989e36ecc53f867d47933265582e908a1447e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140083206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e972b8a71ab393c2c9304c58adf31611d2c570c44fcec1db32f605084068bc15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ed4283c0e34c1b3349c61e47afaf58a71aecea82db8aee69f2c8a865f8c6e`  
		Last Modified: Wed, 04 Sep 2024 22:10:04 GMT  
		Size: 66.2 MB (66237648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01cdcc374f72d44626207be32c439902b464c3d3d658b27a0c29d7107189d7aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b9cc4d75bad83ca4b442ce53584ba2058d9f735654e1925bd4e3b30136adf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0bbb7d3555c5e266def6f06d169472398be0bfe917c38b3861dc1d36d788c967
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c85203536db60a8c20cdb824e4db7bc726e1e864a68108be5e92465d9919731`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b82974da5a3d69a6ca94388b0a3f14e1fe28ce4d21ef9f4032d841f5325b32`  
		Last Modified: Tue, 13 Aug 2024 01:38:31 GMT  
		Size: 65.0 MB (64998376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4340b676a86c741205c6828d4978c183a33ab7cd51f670f731933698f6a24e2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151233149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358365cff60f4d16d7e2fab1ad5aec512ecfbe089679bd2d3b779001ce4f541d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172a0ce16e36a34ff88a2732bbe6037759cb39c60616bd29dbc966d3bb79ec3`  
		Last Modified: Tue, 13 Aug 2024 01:37:28 GMT  
		Size: 71.4 MB (71359436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a94c313135c49432dcc25f79928b6432dbe57b3358b23fe6f8e2731e7a13cee9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136916590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789762e26029931eda37c3b67f68f8756948dc5bce4177216ab908a7803afe0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a7954253b1f3af858d514d5a50598aad4e02214e66bf45ff119714d2d5fd0`  
		Last Modified: Wed, 04 Sep 2024 23:08:21 GMT  
		Size: 65.4 MB (65415937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cb088f2d9bfba6b06089622747309a8a3e0272d0daa567059097be31e6d8c85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141312776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af870be03c1edab12a17bc767ce71cf4be64f10112ebde559f5afdea8b9762`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c43737168f685110fa0a3c4ec68bd02aecf241fa770d30b263bb78a2ad0f70`  
		Last Modified: Tue, 13 Aug 2024 01:26:30 GMT  
		Size: 67.3 MB (67269243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:3482f48a94e991a648afa7e928a52800e8d9de9135b7cdf1e0afd895f2e0e1dd
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
$ docker pull buildpack-deps@sha256:36c2f5ea2f2ed1af1a446e2a4b9c0581b2e9f6426c9c666c302f3f9da33d9233
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349024496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68e5df27df86c2708cfa83cb52ccb6743a7e33e15c08e881e1a7b139e17eaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9f466c772c63c0e404781bd892c92479011664bf06f3cef798537d746b179c6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316100401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5493e5bda9d497e34a2368597973d59f8726156a38ca2253594f5cc160dbcc44`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29df05d41a6c52dd0e5bf38b1bd02aabd071cdfc47e5db769d4f8027cbce9b07`  
		Last Modified: Tue, 13 Aug 2024 01:30:40 GMT  
		Size: 184.5 MB (184530610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14bef58de028be12d34b7d805db521356633a00a79f137bb9f3b40507b15c1cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301543748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a3d866e963713e2b0df1ca898afeec6d371ecb89003a9583c5eeeabe181b8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf1b5402e12f0e97f96b3da218271b7caf2abf4a321ce82a42bedc2d72eb82`  
		Last Modified: Wed, 04 Sep 2024 22:36:55 GMT  
		Size: 175.2 MB (175209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86e5ce1c1f020479b72379683bbaaba7231a8116d5e7c58f2296616614edfa2d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339829397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71f840d8ec66950efb66641927297df50dfd31df6ac0fca91b03f94b6dcbbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:02:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c2a8d94613f34ce7d0ac4fd4e51800d8f4aa8a0bc9347fe5c8436b4c3bd5`  
		Last Modified: Wed, 04 Sep 2024 22:08:46 GMT  
		Size: 202.7 MB (202652028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c74dfe011eb174893ece8c3425af9325b29bcf3b255dc6e801e51559d7e4fc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351614656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bd62f9c712d1e81e60de9dc0a2e3a0204625ac0827903ce83fe542f65e3bd9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:06:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:80c1fa486a8fe97ada53cf595bbf926961ccd26376ac7b955e202996f7c3fcce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325968669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ce2a7a0bc3c2b559803f3b5f224da10915c34d06666b56f5c7c5398f56493e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93661e8bade5668baa650e17db139abcf2b722965a5fbccb9f55952cf3a58f`  
		Last Modified: Tue, 13 Aug 2024 01:34:16 GMT  
		Size: 189.8 MB (189802742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e1e4dc245c2aa0f0dadb1aced70100a855dbb67c14f3ea00f313201d7391b80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363098887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199ffe8f176fb39cd04f4be9dc7085de14b523d0334dab77db8947fe524ccd88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:22:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:245b9b0711a7536d1e01d84674d3150ed436ded567d718c318ed6f0991c7fdb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318370851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11952f41cd8b223618a6668fc853d395c9ec9cbe84e9f8096e511a00a6696512`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:cea44adf4ea624da69e217dfae13d27f9f828cf037d24aa37f3a4c50fe20899a
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
$ docker pull buildpack-deps@sha256:66e568a0a9e5131643f75cea2fe66c8b45cc0395469455b5769ec2f051ee687b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73609855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f970a070b94afe24b57c75affd184376a5184f3f89257081f38f470e378ff16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0a6ef7c61de7721a295dca8e97bb78d27624162034e64abae614b705e4bf4ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09194f0040c080f5fb56b3fb0339a44e743b1cae3ac4748998b7f95c3f2f8f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5f2f9b35615c65ef5907c414739f3c797f3ffed0d930f9dd7b804fb44c6e2f8a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1be3ba03c082f27c71f0ab4f19490077884e870604189d30b5c0a62f4a604e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3ecd6e86b392efaaa7b0ccfc022e224fe6542a1c5a76865b63fbe3362af4e489
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc916e017c53b1c9e80e6ca1d4977005c6f31a98c64fbd683dc49f98c0bfc9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3612c7ccf08d122ee492ab85372b19fe18a7d7337341fd6e764344a2f97ab2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3502433f1c3c8c63799bd241a5a37328bb670138e1bf9b65d74a5bc3dd77d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a7e5923179ad67002f2ec52fcd93777b208ca200fc7fee6b29292272c2d6055a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf523351470d1a274a71d138a0bb979a64003bf292dee5c995f91d7cef45020d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:15bebfb1ce6517765581a89c1270a3039857497f5393a3a53eb55a6cf6c3b9e9`  
		Last Modified: Wed, 04 Sep 2024 22:23:29 GMT  
		Size: 49.6 MB (49562002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2220e2c6ab360be293a3568d8fad1b242e41ac727fbfd337305f9bda60d806`  
		Last Modified: Wed, 04 Sep 2024 23:12:52 GMT  
		Size: 23.6 MB (23647328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2afd8ac0056f6339cd6e120016dddf7da8b0d0b9bb1bf8b4fb224030c8327179
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08af492de9c4b4dba33292c74f6d83a0bb23f4706dbcc91dbd7fa16d7384722a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a34981c40380a750bf180a238c928fd2c0d4d850401ab232c5522418f5917fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e55127375c42a52b0cdff321d3068ce4218382ea8fff382d9c06f2bb5e4ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:e2ea1bc81a724065d5629534f53d30f60729c4576001bc066aaf56e300ea237f
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
$ docker pull buildpack-deps@sha256:68e358c3c05d520af01b674163e1f5d31a6172366ed0352550d4b5f4001cdfd9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137757873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2581f163f0552bbce9b3a5d33ec03b5f75be04876ea325c1f0a2f936f293fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1d2cb11ccef3f86147133f3dde474766ccae22d038c1498ade71e3d9505fe665
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131569791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efbb3e4bc9ebc13547c5d9944bbe33ee0a59fcfef91a5535a2fc4c3527826e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ef757fc27d5b94c652221e08501ca120f44bc94bcc3eb9b3130b28f91307c18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126334298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833eb6fd43fd38ce68fc4749a0272945c863058498498304d502e076b86aa650`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c0796108d4f0bb51a454428f5166df78cc3e40136a7d253ac1d8beeb85f734e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137177369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0013d72146ac385cfbc7a7ab43109e4916a8e8fba1e0c7aeaad85545273d89a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fc24d91b13db9bea6198bb18d275403768ca62332ea9815b3e91b87bda5b6ec4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128efb528b94818265ba8257926d66c6c6ded4a2257a29e6bf86f4ad39ef4ecb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4d1ee8e4bdbe8b07ec10c0d1115f4e722abb614ca2123f5524e48c3b653f8451
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e0fe59d2d5ca07f6a297b61740fb334b836d66fdab89d2d1c3ae797d7a8cfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67fb44179c22a0a46e18108147c764d2096f18d571fd9b0b90c37a493a55701f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a399ae7695be551ea659c15ec8842777bf6d4db45eca491da16667270d6fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:732c22618cfcd4e8ef5da95054a577ddec7f874e23557a128b01813304bd6048
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ae05d5608df2ce534b0015ec009bbac71560883de2290f6691dcaa8a9588d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:21284940c2374059cb30efa7b4197d3f4db6cd7325d66d4f5ea1ba2460906fb2
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
$ docker pull buildpack-deps@sha256:2e0df549474cde4893562be6627df41a95fd13695938a1305036a9e592080402
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365317086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99399255020f608381fbb243b8de7cc3f3d6f522ffab1eeb144a4afc3acb4205`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:00:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4176ccfc0b61583df03b9466a003ee06066c08fa17db7930744efc514570`  
		Last Modified: Wed, 04 Sep 2024 23:04:30 GMT  
		Size: 66.2 MB (66217850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22db95340ceebc1ccc73cd678fb695dbe369c7b73e767635573b134360781e5`  
		Last Modified: Wed, 04 Sep 2024 23:05:04 GMT  
		Size: 225.5 MB (225456365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:372f3e5f923b3c9277d390fe4e250d110f3b11b156b8f867e26a53b8d16e22b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328384281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945d8c80524783749b323d4b3de423ca771a4cbf28f1bd12015f8d25a9c128fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:29:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24383425ce336421fbfcfd0e62dfaba17636c030330599590ab7b5d8e4e149af`  
		Last Modified: Tue, 13 Aug 2024 01:33:22 GMT  
		Size: 63.0 MB (63001460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f582246bcb8be76eb91cfe4ce1a465ccf5994c61db67417139e45c601e3c77`  
		Last Modified: Tue, 13 Aug 2024 01:33:56 GMT  
		Size: 196.1 MB (196070350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d3d119cda38974d83c93ecf47180a360ff6120909f8405cfe2a0cbadc2d35e85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315485099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c7471066cf547315214b5bf0bb4212a6b639793d45c16dbccc66cd51c85ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:34:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:35:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1cd9b83eb6a11fc2bfd0f145ae9fc8ee9f0d5564e3b28a008f43b172b63a83`  
		Last Modified: Wed, 04 Sep 2024 22:39:38 GMT  
		Size: 61.2 MB (61150667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017488a8ae5b0d46810348f43cbf30520604b3a267121b90af6e524919714e05`  
		Last Modified: Wed, 04 Sep 2024 22:40:10 GMT  
		Size: 187.9 MB (187900232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c99ec2fa97aa47a20c15cf639b779ebb08cb6e5f056db4b4276cac8a1db4f39b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359147411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61207ab7b0b70524f64b4fbb024945fb60a7cb06b97c05fc54b41b863a36a30b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:07:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65145a9285af4b5bbebcc4c38c65635bf19540a153981b2e047fbfcce92216d`  
		Last Modified: Wed, 04 Sep 2024 22:10:56 GMT  
		Size: 66.2 MB (66237440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0622095ce10919ff1fbf55116995eedcefb2cf63a53958394e3cbff13298e3df`  
		Last Modified: Wed, 04 Sep 2024 22:11:23 GMT  
		Size: 219.1 MB (219080820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eb8bff1d818def7a2f22ea0f49a8685fa94b9917603df0642628116b1a30c508
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363874327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70deb4dfacb021a563799df9a83678c946ed3a56efb8cb6244b5b2d6af11605e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee207a11e4a6de69d2bf4707298d7d6291e3b054d299d2964e51c9aef6ee01e`  
		Last Modified: Tue, 13 Aug 2024 01:18:43 GMT  
		Size: 221.5 MB (221526932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dd86ea6c1ac9d97509fc8c6cef961e973a70cf96f7c6565f728f0ea3a5a6ef38
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336783254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aaaba46df956f56bf02443e502c95ff15056e15d393234240249863a0a8fcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdca8b68360b0ebfce94a5c7ac25e6db987b2b2549ef1754ae12e7585a9c801`  
		Last Modified: Tue, 13 Aug 2024 01:42:04 GMT  
		Size: 64.2 MB (64197669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c951d6341f7b059bae3179565d39537533ee9d1986dfece9e6cb00b078c7baf`  
		Last Modified: Tue, 13 Aug 2024 01:44:19 GMT  
		Size: 200.1 MB (200133839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4aca54aec2a39581f95720c64add62fc87f05385a0f0d8289d642c7dca305951
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369591381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34508033db8d878c42ea36ae34d2f22f18d7f9d8695b72677885ce12e9a19cdb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:33:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29987d85cabed87e33bd1473f10a5dec4eb0ac635560351ca53022c9a377d1b8`  
		Last Modified: Tue, 13 Aug 2024 01:38:38 GMT  
		Size: 70.7 MB (70650978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e76965f731d3de981bcbaeb56b632d6f3eb13dd717e940d77f4cb915c60811d`  
		Last Modified: Tue, 13 Aug 2024 01:39:17 GMT  
		Size: 219.1 MB (219082484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5ea10cfbc99a625868cf640c06034bf2c011a3e5265f907af2a182e868de2286
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334655383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96cc6e5e18b227d264f00ed7829ee6a12fe76afdbcee2660ab8338bfcf3e309`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f762934c1c39d2dca0d862589e99bc991c7536f69a6e4b21f744a0b7f131e`  
		Last Modified: Tue, 13 Aug 2024 01:27:20 GMT  
		Size: 66.4 MB (66449875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918a9be05d4e4860cc8177bb1e67262cc77b9ba0bc6a1bebfca990da01c64d5`  
		Last Modified: Tue, 13 Aug 2024 01:27:47 GMT  
		Size: 194.2 MB (194191367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:33220afa4172cf86e87b5c711be9017ac6ca2ffd7a29d916a059eac7d36121b6
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:daadf1decd2f26e479246d7fdc37deb03276b82e9df4a5c14769b8ed6200bb01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73642871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f5344b74da57c1aec89106c34972ab25c2c2bd7051723c6fa1c58e57ea9877`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:74a6d5c9024d72b7884bf858c33e518a1543ad7d7efb7edaf5e835a5cfdf8fac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69312471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccc470cd309502af687f9b3a2bf5569a07ac66f2f48fef3e0f34bd5bb62206d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:80599527d38f3f9a9d793aae25040dc1718bfdc2391b265842bf358dd867fb6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66434200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9618994342680a65b4bd70af330513c59f58b90b1979bcccbcd27e48a8e93b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df1b58b717328f01a3319f41400cb48c12ea81760537ed99307bdbd2b9696f7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73829151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8952df3538af05ac37f9c33f6947b1d08bd149d5179bf1575d8ef3dc1a5270`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5d4fec0eb7d196988a99411e3ceb68545272536f7c53235a2c611ec0d9ecd380
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75222611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cf295bc53b37cf4460d54ffcde842606c4ed9ef6385b5b153980e8310264e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15f4221d0909a0a194569119853ff29658dc1f889737b850287710eea385be9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72451746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c21850609b583715012b80582f592f169ead5c14fa3533424ba84be9efd2b5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3bce3224a9ba2a7d7a2cb0c7f63972f5b9da48d9a06cd80cb52215aad19bca96
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79857919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5b17d7afcbb3df3e911dcec159e948d29c4cc333f4c25c7ef7826182f426b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d3b907b51131d5d2b70343e955daeb1d39c52afa545332bedd50924f6e57560a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70873705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f7d9fcb1032a127bae5c6f5d1b116341dd27b2dc10788c5f24d37adeb9402b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:13:20 GMT
ADD file:83cbcb6055e53dd5bbbdb284d5c1129bd8ef0b02c2f174e4bad8a86a9a470700 in / 
# Tue, 13 Aug 2024 00:13:22 GMT
CMD ["bash"]
# Wed, 14 Aug 2024 18:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:664f4e8f311a644728086c0fb1ccd2a113bc5c8af1174d6b42e68ae243e81646`  
		Last Modified: Tue, 13 Aug 2024 00:18:53 GMT  
		Size: 51.1 MB (51127228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291979be21ad443cd3fd97607b813c6af48dece7333db3d66cb6aeba7d3399db`  
		Last Modified: Wed, 14 Aug 2024 18:10:32 GMT  
		Size: 19.7 MB (19746477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f204e1391edd06914c2eb6ab6bd9d83380b14aed0842bfed5c8e1c04ddc2bb28
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce202fb8d3590d31c47d7b239b0472150c735cb7bdd5ff6baa8e017741285e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:0839efe8fe1c251fb0cda5f282af278d1f6156f55488fcb4519abc789f650f08
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
$ docker pull buildpack-deps@sha256:29bb535be7889f365c5cdcf4f762b72331f494093a8e2f8541001061bc6eff44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139860721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecd6784cc90fdaa1b0f5c5a698d3cefcd3cf85015c2a3d64dac0db55d8a3ce9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4176ccfc0b61583df03b9466a003ee06066c08fa17db7930744efc514570`  
		Last Modified: Wed, 04 Sep 2024 23:04:30 GMT  
		Size: 66.2 MB (66217850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f0b187f8f18714df9e991a656fc0f2a80c8327ac62e2f23dd70080ef83f1c6b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132313931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0011ffd5c1b4dcb144acdf454a18478ec58e58d0b76ef7093462465ea818eed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24383425ce336421fbfcfd0e62dfaba17636c030330599590ab7b5d8e4e149af`  
		Last Modified: Tue, 13 Aug 2024 01:33:22 GMT  
		Size: 63.0 MB (63001460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:814f909e0107c28965b9fc7d714165707b3293bdb51d8808af1568ec429e7162
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127584867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e3e824d53cd5d5c10370cdeaa86292ebf9a8c760469def252bbe313ed99a0a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:34:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1cd9b83eb6a11fc2bfd0f145ae9fc8ee9f0d5564e3b28a008f43b172b63a83`  
		Last Modified: Wed, 04 Sep 2024 22:39:38 GMT  
		Size: 61.2 MB (61150667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:449767f242c02fcefd2da777a6b7572bfc25ffaba7a5dd22990868bea2b905c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140066591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ded28d1c88b687b49ff8d990c7368685ce1fd35e36a692f9ad5db9175957980`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65145a9285af4b5bbebcc4c38c65635bf19540a153981b2e047fbfcce92216d`  
		Last Modified: Wed, 04 Sep 2024 22:10:56 GMT  
		Size: 66.2 MB (66237440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:acfc21a933b61a511a40057c2cd17da39e0b250e421dcc7aa725078e2e542d2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142347395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26dfc06fb060f82a67d251678866e3eff820033e7c7b1d4ef017858d28fb594`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae61694adb073775cdca4573dfd33ebc664d11ca9805f83c9752262aa3e8593d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136649415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0878904dabe9eaaf284de551155f435f7591349d2dacf355819778e21f5e4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdca8b68360b0ebfce94a5c7ac25e6db987b2b2549ef1754ae12e7585a9c801`  
		Last Modified: Tue, 13 Aug 2024 01:42:04 GMT  
		Size: 64.2 MB (64197669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:217a265206c1665bace140bae895d8f0389cd1108784b49ae025ee581832f9ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150508897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef248ce0249576f6a1898b164e41333a4b6f5ceb2040c1a2fa58d257f7eacf48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29987d85cabed87e33bd1473f10a5dec4eb0ac635560351ca53022c9a377d1b8`  
		Last Modified: Tue, 13 Aug 2024 01:38:38 GMT  
		Size: 70.7 MB (70650978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59b4aa62accf6e07b2b7fb794fc05cacd6275d29ce1f60320c53774d3d540cb4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140464016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e510155ef48c59718ba45b79ed24018f4f20b5be7f993ced3cbc8095bcd5a348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f762934c1c39d2dca0d862589e99bc991c7536f69a6e4b21f744a0b7f131e`  
		Last Modified: Tue, 13 Aug 2024 01:27:20 GMT  
		Size: 66.4 MB (66449875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:21284940c2374059cb30efa7b4197d3f4db6cd7325d66d4f5ea1ba2460906fb2
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
$ docker pull buildpack-deps@sha256:2e0df549474cde4893562be6627df41a95fd13695938a1305036a9e592080402
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365317086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99399255020f608381fbb243b8de7cc3f3d6f522ffab1eeb144a4afc3acb4205`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:00:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4176ccfc0b61583df03b9466a003ee06066c08fa17db7930744efc514570`  
		Last Modified: Wed, 04 Sep 2024 23:04:30 GMT  
		Size: 66.2 MB (66217850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22db95340ceebc1ccc73cd678fb695dbe369c7b73e767635573b134360781e5`  
		Last Modified: Wed, 04 Sep 2024 23:05:04 GMT  
		Size: 225.5 MB (225456365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:372f3e5f923b3c9277d390fe4e250d110f3b11b156b8f867e26a53b8d16e22b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328384281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945d8c80524783749b323d4b3de423ca771a4cbf28f1bd12015f8d25a9c128fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:29:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24383425ce336421fbfcfd0e62dfaba17636c030330599590ab7b5d8e4e149af`  
		Last Modified: Tue, 13 Aug 2024 01:33:22 GMT  
		Size: 63.0 MB (63001460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f582246bcb8be76eb91cfe4ce1a465ccf5994c61db67417139e45c601e3c77`  
		Last Modified: Tue, 13 Aug 2024 01:33:56 GMT  
		Size: 196.1 MB (196070350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d3d119cda38974d83c93ecf47180a360ff6120909f8405cfe2a0cbadc2d35e85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315485099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c7471066cf547315214b5bf0bb4212a6b639793d45c16dbccc66cd51c85ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:34:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:35:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1cd9b83eb6a11fc2bfd0f145ae9fc8ee9f0d5564e3b28a008f43b172b63a83`  
		Last Modified: Wed, 04 Sep 2024 22:39:38 GMT  
		Size: 61.2 MB (61150667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017488a8ae5b0d46810348f43cbf30520604b3a267121b90af6e524919714e05`  
		Last Modified: Wed, 04 Sep 2024 22:40:10 GMT  
		Size: 187.9 MB (187900232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c99ec2fa97aa47a20c15cf639b779ebb08cb6e5f056db4b4276cac8a1db4f39b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359147411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61207ab7b0b70524f64b4fbb024945fb60a7cb06b97c05fc54b41b863a36a30b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:07:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65145a9285af4b5bbebcc4c38c65635bf19540a153981b2e047fbfcce92216d`  
		Last Modified: Wed, 04 Sep 2024 22:10:56 GMT  
		Size: 66.2 MB (66237440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0622095ce10919ff1fbf55116995eedcefb2cf63a53958394e3cbff13298e3df`  
		Last Modified: Wed, 04 Sep 2024 22:11:23 GMT  
		Size: 219.1 MB (219080820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eb8bff1d818def7a2f22ea0f49a8685fa94b9917603df0642628116b1a30c508
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363874327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70deb4dfacb021a563799df9a83678c946ed3a56efb8cb6244b5b2d6af11605e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee207a11e4a6de69d2bf4707298d7d6291e3b054d299d2964e51c9aef6ee01e`  
		Last Modified: Tue, 13 Aug 2024 01:18:43 GMT  
		Size: 221.5 MB (221526932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dd86ea6c1ac9d97509fc8c6cef961e973a70cf96f7c6565f728f0ea3a5a6ef38
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336783254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aaaba46df956f56bf02443e502c95ff15056e15d393234240249863a0a8fcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdca8b68360b0ebfce94a5c7ac25e6db987b2b2549ef1754ae12e7585a9c801`  
		Last Modified: Tue, 13 Aug 2024 01:42:04 GMT  
		Size: 64.2 MB (64197669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c951d6341f7b059bae3179565d39537533ee9d1986dfece9e6cb00b078c7baf`  
		Last Modified: Tue, 13 Aug 2024 01:44:19 GMT  
		Size: 200.1 MB (200133839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4aca54aec2a39581f95720c64add62fc87f05385a0f0d8289d642c7dca305951
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369591381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34508033db8d878c42ea36ae34d2f22f18d7f9d8695b72677885ce12e9a19cdb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:33:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29987d85cabed87e33bd1473f10a5dec4eb0ac635560351ca53022c9a377d1b8`  
		Last Modified: Tue, 13 Aug 2024 01:38:38 GMT  
		Size: 70.7 MB (70650978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e76965f731d3de981bcbaeb56b632d6f3eb13dd717e940d77f4cb915c60811d`  
		Last Modified: Tue, 13 Aug 2024 01:39:17 GMT  
		Size: 219.1 MB (219082484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5ea10cfbc99a625868cf640c06034bf2c011a3e5265f907af2a182e868de2286
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334655383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96cc6e5e18b227d264f00ed7829ee6a12fe76afdbcee2660ab8338bfcf3e309`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f762934c1c39d2dca0d862589e99bc991c7536f69a6e4b21f744a0b7f131e`  
		Last Modified: Tue, 13 Aug 2024 01:27:20 GMT  
		Size: 66.4 MB (66449875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918a9be05d4e4860cc8177bb1e67262cc77b9ba0bc6a1bebfca990da01c64d5`  
		Last Modified: Tue, 13 Aug 2024 01:27:47 GMT  
		Size: 194.2 MB (194191367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:33220afa4172cf86e87b5c711be9017ac6ca2ffd7a29d916a059eac7d36121b6
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:daadf1decd2f26e479246d7fdc37deb03276b82e9df4a5c14769b8ed6200bb01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73642871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f5344b74da57c1aec89106c34972ab25c2c2bd7051723c6fa1c58e57ea9877`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:74a6d5c9024d72b7884bf858c33e518a1543ad7d7efb7edaf5e835a5cfdf8fac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69312471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccc470cd309502af687f9b3a2bf5569a07ac66f2f48fef3e0f34bd5bb62206d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:80599527d38f3f9a9d793aae25040dc1718bfdc2391b265842bf358dd867fb6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66434200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9618994342680a65b4bd70af330513c59f58b90b1979bcccbcd27e48a8e93b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df1b58b717328f01a3319f41400cb48c12ea81760537ed99307bdbd2b9696f7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73829151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8952df3538af05ac37f9c33f6947b1d08bd149d5179bf1575d8ef3dc1a5270`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5d4fec0eb7d196988a99411e3ceb68545272536f7c53235a2c611ec0d9ecd380
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75222611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cf295bc53b37cf4460d54ffcde842606c4ed9ef6385b5b153980e8310264e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15f4221d0909a0a194569119853ff29658dc1f889737b850287710eea385be9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72451746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c21850609b583715012b80582f592f169ead5c14fa3533424ba84be9efd2b5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3bce3224a9ba2a7d7a2cb0c7f63972f5b9da48d9a06cd80cb52215aad19bca96
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79857919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5b17d7afcbb3df3e911dcec159e948d29c4cc333f4c25c7ef7826182f426b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d3b907b51131d5d2b70343e955daeb1d39c52afa545332bedd50924f6e57560a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70873705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f7d9fcb1032a127bae5c6f5d1b116341dd27b2dc10788c5f24d37adeb9402b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:13:20 GMT
ADD file:83cbcb6055e53dd5bbbdb284d5c1129bd8ef0b02c2f174e4bad8a86a9a470700 in / 
# Tue, 13 Aug 2024 00:13:22 GMT
CMD ["bash"]
# Wed, 14 Aug 2024 18:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:664f4e8f311a644728086c0fb1ccd2a113bc5c8af1174d6b42e68ae243e81646`  
		Last Modified: Tue, 13 Aug 2024 00:18:53 GMT  
		Size: 51.1 MB (51127228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291979be21ad443cd3fd97607b813c6af48dece7333db3d66cb6aeba7d3399db`  
		Last Modified: Wed, 14 Aug 2024 18:10:32 GMT  
		Size: 19.7 MB (19746477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f204e1391edd06914c2eb6ab6bd9d83380b14aed0842bfed5c8e1c04ddc2bb28
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce202fb8d3590d31c47d7b239b0472150c735cb7bdd5ff6baa8e017741285e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:0839efe8fe1c251fb0cda5f282af278d1f6156f55488fcb4519abc789f650f08
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
$ docker pull buildpack-deps@sha256:29bb535be7889f365c5cdcf4f762b72331f494093a8e2f8541001061bc6eff44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139860721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecd6784cc90fdaa1b0f5c5a698d3cefcd3cf85015c2a3d64dac0db55d8a3ce9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4176ccfc0b61583df03b9466a003ee06066c08fa17db7930744efc514570`  
		Last Modified: Wed, 04 Sep 2024 23:04:30 GMT  
		Size: 66.2 MB (66217850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f0b187f8f18714df9e991a656fc0f2a80c8327ac62e2f23dd70080ef83f1c6b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132313931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0011ffd5c1b4dcb144acdf454a18478ec58e58d0b76ef7093462465ea818eed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24383425ce336421fbfcfd0e62dfaba17636c030330599590ab7b5d8e4e149af`  
		Last Modified: Tue, 13 Aug 2024 01:33:22 GMT  
		Size: 63.0 MB (63001460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:814f909e0107c28965b9fc7d714165707b3293bdb51d8808af1568ec429e7162
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127584867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e3e824d53cd5d5c10370cdeaa86292ebf9a8c760469def252bbe313ed99a0a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:34:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1cd9b83eb6a11fc2bfd0f145ae9fc8ee9f0d5564e3b28a008f43b172b63a83`  
		Last Modified: Wed, 04 Sep 2024 22:39:38 GMT  
		Size: 61.2 MB (61150667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:449767f242c02fcefd2da777a6b7572bfc25ffaba7a5dd22990868bea2b905c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140066591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ded28d1c88b687b49ff8d990c7368685ce1fd35e36a692f9ad5db9175957980`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65145a9285af4b5bbebcc4c38c65635bf19540a153981b2e047fbfcce92216d`  
		Last Modified: Wed, 04 Sep 2024 22:10:56 GMT  
		Size: 66.2 MB (66237440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:acfc21a933b61a511a40057c2cd17da39e0b250e421dcc7aa725078e2e542d2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142347395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26dfc06fb060f82a67d251678866e3eff820033e7c7b1d4ef017858d28fb594`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae61694adb073775cdca4573dfd33ebc664d11ca9805f83c9752262aa3e8593d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136649415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0878904dabe9eaaf284de551155f435f7591349d2dacf355819778e21f5e4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdca8b68360b0ebfce94a5c7ac25e6db987b2b2549ef1754ae12e7585a9c801`  
		Last Modified: Tue, 13 Aug 2024 01:42:04 GMT  
		Size: 64.2 MB (64197669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:217a265206c1665bace140bae895d8f0389cd1108784b49ae025ee581832f9ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150508897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef248ce0249576f6a1898b164e41333a4b6f5ceb2040c1a2fa58d257f7eacf48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29987d85cabed87e33bd1473f10a5dec4eb0ac635560351ca53022c9a377d1b8`  
		Last Modified: Tue, 13 Aug 2024 01:38:38 GMT  
		Size: 70.7 MB (70650978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59b4aa62accf6e07b2b7fb794fc05cacd6275d29ce1f60320c53774d3d540cb4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140464016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e510155ef48c59718ba45b79ed24018f4f20b5be7f993ced3cbc8095bcd5a348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f762934c1c39d2dca0d862589e99bc991c7536f69a6e4b21f744a0b7f131e`  
		Last Modified: Tue, 13 Aug 2024 01:27:20 GMT  
		Size: 66.4 MB (66449875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:be63c64ee3fd7e0fa9d9330932a9bd46435e015ec6a6f5c1a13715580abfff5c
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
$ docker pull buildpack-deps@sha256:95636449c78c5311c92bb5c04cb71ca71e321e62d9ba7f340496a3e8ea1b6613
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364424180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0886d8c654ee90cd57e0951a093439e8008935828f019928689ca1c412fd23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac0b2d691022b6e9d2a4261f3c3547b5863197743e9544f77779e589aa6a9`  
		Last Modified: Wed, 04 Sep 2024 23:03:29 GMT  
		Size: 66.2 MB (66214670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6946879d70176adc3ffb5837bbaa51b79bced4142aae63dfbde91e5c47b690`  
		Last Modified: Wed, 04 Sep 2024 23:04:03 GMT  
		Size: 224.5 MB (224549385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d01e97fce87eb39b36f37f8aa45312b5a11da5fe5cca14f145171bd8242a1cad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0658cfb7a474590e1994b4a562fa6dabef9db569cd315e4dc4af819218edc3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff253c8c9180c53a680ac594e0b90ace399416d9f322bef4f9a66e3d0fe0c5af`  
		Last Modified: Tue, 13 Aug 2024 01:32:17 GMT  
		Size: 63.7 MB (63717307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e89c01125ee82ab0aa0af47c3526f7864fc2f07adc19ebfe1e2b58061dbb7b`  
		Last Modified: Tue, 13 Aug 2024 01:32:53 GMT  
		Size: 201.3 MB (201294728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:37b6810fa3d1d732d30766846909d30dfab637c900f47d30c4ae3280dfd8c9db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314706112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb90709c7a5e58c2a0ebff4d085a2cfed0066899451050ce3039cd3c67da182`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:33:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b337ebc4882ba5bf1b4d0ef428653fa3a9963e209aefc6227386f1a76b3176`  
		Last Modified: Wed, 04 Sep 2024 22:38:28 GMT  
		Size: 61.1 MB (61148386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f918449aecbe1b94d67117d739aece3a6bc2dc9aea2eecff37a6d4a68cf059`  
		Last Modified: Wed, 04 Sep 2024 22:39:08 GMT  
		Size: 187.1 MB (187105286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e67fb06f6e500129e26b9720fda34f641d39d6830faaee85458a3f5ad6243ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358192533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1708ee9622d0dde1a503c07b7ed6ad4bb182e70bbb6bfd19eef2b2e5d6328b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:05:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ed4283c0e34c1b3349c61e47afaf58a71aecea82db8aee69f2c8a865f8c6e`  
		Last Modified: Wed, 04 Sep 2024 22:10:04 GMT  
		Size: 66.2 MB (66237648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef4fa35fa4ab50f808bb497d29332afec951c4bcb10c0dd0d72bbb720a7932a`  
		Last Modified: Wed, 04 Sep 2024 22:10:32 GMT  
		Size: 218.1 MB (218109327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04cd0e8012a7b0a927453540343a58c40ce7422329b38254cc3e2c0fa5709eb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.2 MB (370192161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a14e845327d478743cc97f4cad35b0845c843799f0201dcea0ab4a3d804b16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:11:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a203d729458242dda28f4795cf80bb88746084ccdc8cce21ba2acd7dcaefb3`  
		Last Modified: Tue, 13 Aug 2024 01:17:23 GMT  
		Size: 226.9 MB (226923306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3b99b1a614b2627c2ee392abf6cec24d6e709a64ff2660fa5dfcff701541b014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343104341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e38cadba3b728e3cc3d2698789e9a516b7fff066fe5de0170975495cb00f8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:21:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b82974da5a3d69a6ca94388b0a3f14e1fe28ce4d21ef9f4032d841f5325b32`  
		Last Modified: Tue, 13 Aug 2024 01:38:31 GMT  
		Size: 65.0 MB (64998376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b138f1bac27906feed7c16ced7bfda41230bd94f4e3fa7fa461b5d556cca85`  
		Last Modified: Tue, 13 Aug 2024 01:40:49 GMT  
		Size: 205.6 MB (205575439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad4b04250fc6a8dfb76563542cd67b13c68bb161c5ae1e30e1821818f90a5ef6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.8 MB (375834614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662c9bbbe195ec285293da4dbb7e93e9ede726496a2364e6f9523f561594b7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172a0ce16e36a34ff88a2732bbe6037759cb39c60616bd29dbc966d3bb79ec3`  
		Last Modified: Tue, 13 Aug 2024 01:37:28 GMT  
		Size: 71.4 MB (71359436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c40f2aa6297d7f1a7d0c5c01d5abdbc3208369127949982cb6b44835f9e6370`  
		Last Modified: Tue, 13 Aug 2024 01:38:08 GMT  
		Size: 224.6 MB (224601465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1f0fb710e4c77f45c369961d8f5ad1b5c3c2d6d6637879b7f0ee0cec7a11e1e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443858778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13763f9c3914a92f12e358871f27bfd1ee3de1d1a8f20a4e5a9c057826caed09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65deb42d9c749a528063c18ed3482c3235a8863523f7fc5d895330b910edd50a`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 65.5 MB (65455674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a959a2b7a253bddaf7fd68b258fe0255968fc0d4f52643281e2ac2de68e19e6`  
		Last Modified: Tue, 13 Aug 2024 00:53:51 GMT  
		Size: 307.3 MB (307284095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:82d3e113ccf2880c3912b85e42057ceef574bf3adbe52c37b776b906b69dd473
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342028696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984dfc489e1f8db6f7dc2248ab5d807b1457996661c87373f320a97a40a6e041`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:21:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c43737168f685110fa0a3c4ec68bd02aecf241fa770d30b263bb78a2ad0f70`  
		Last Modified: Tue, 13 Aug 2024 01:26:30 GMT  
		Size: 67.3 MB (67269243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9eb516daa4ac7451bd5504522258db8cda9841d72e9c32f295c166a2ea370d`  
		Last Modified: Tue, 13 Aug 2024 01:26:57 GMT  
		Size: 200.7 MB (200715920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:4ad0482e3f6e8fe8d8e33e5f70154a64998fb0ced072db19a0e8050d823f9fd1
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
$ docker pull buildpack-deps@sha256:ec2e4ba708bbdf5e0da6788d027041c767bf9165a08a035f94c515e93f12073f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcf1fb70b329c7b917257747d7b2aa74ae8deba8bd35228162e9fc2d3b14dec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f7b8be926f1bd951849a9c75815f36d1c7e532df7497cde939244a305ea7f090
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69311252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34583e63b9066ab656cf7f884c618cf83e0903e526aec63de39a9e145253044`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:51f16b2b3c891eca8cefaee1e8f70cf3c8e049d4feb44152aaf3b4d2221ef4c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66452440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ee032b74216acc8825fd7595e837b592eab1b9ad1444d64b0e16ff032a039`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e75ffb7a2e7f4ad78b5eaaf80f80ceee80cbd1c4b9a765b3eddd34c903a3b5f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73845558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea665e856755fa51885b312d1ce870241400d83b9292e1f1436b26cd6b56621`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cb5e40a7be972b1172bafa92ab71f6a08c143e06b0981336a4bc4d8af23400cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75244435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d80a37e21c9e25d3737094c1c4b40886ed52181492e44fdc9dfbddf970ee8f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84b61ff5dbbeb62166e032082928afcd108dec8f874958c9c8dcf6799ca93767
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72530526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c4826139623ef2ef60d33d9f29bae5ba7e34385f1be56999cb44c59b995631`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c4be7903db01dfd7116ff52391f931caac99a1be00c70abf81dd84b7d4272b4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79873713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d224a800248ee906a9bc5cb5a7b1509c10a69fb16353a6773e668aba67d0956`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3215f819f7c134ef7f6419c2df43620029c30939b449a8d4cc7c62d3a946e8aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71500653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efed2f8783057bc14f79d6c2b2bd765819525f1d9769e0423b347a7d07e51f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5d604130680eacd1da47d3bc2917df80e404d80e5f62bf34ea52ddaf846a16b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74043533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39594b5c80df5065e24356bf1588fda37b42791ffcde078d45147ead22f0ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:d4f5dc5df3b19766ea24a3ca1399822f55f43ea67560ca6058df3fe558b49912
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
$ docker pull buildpack-deps@sha256:bfbeceb6f6ba6391d6267f489ea26bc2f67a55ddd1d74db872565ccadad3eead
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139874795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f69fc30003a7b48eb1d4b267523478260d578d8bb232cc6cdeddb9228c6c6b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac0b2d691022b6e9d2a4261f3c3547b5863197743e9544f77779e589aa6a9`  
		Last Modified: Wed, 04 Sep 2024 23:03:29 GMT  
		Size: 66.2 MB (66214670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ed6500bcaea8b4c9ef0e46757565bc33aa4560e04e9b55175c0f215c480362f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133028559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ab093fb96c9708f9b4d2373530572077367c2ba35bfc1989e780f50b8e07aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff253c8c9180c53a680ac594e0b90ace399416d9f322bef4f9a66e3d0fe0c5af`  
		Last Modified: Tue, 13 Aug 2024 01:32:17 GMT  
		Size: 63.7 MB (63717307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:58eef75c65666ab0c1901a5ed3926cc420503406798bf43b3bcfb595fdca219a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127600826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5592be70d2653aafa4fd4e8efb48fae22c8c7c92d8c9b0a0073e302f0f939`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b337ebc4882ba5bf1b4d0ef428653fa3a9963e209aefc6227386f1a76b3176`  
		Last Modified: Wed, 04 Sep 2024 22:38:28 GMT  
		Size: 61.1 MB (61148386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ecd47ce655417046236fa338583989e36ecc53f867d47933265582e908a1447e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140083206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e972b8a71ab393c2c9304c58adf31611d2c570c44fcec1db32f605084068bc15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ed4283c0e34c1b3349c61e47afaf58a71aecea82db8aee69f2c8a865f8c6e`  
		Last Modified: Wed, 04 Sep 2024 22:10:04 GMT  
		Size: 66.2 MB (66237648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01cdcc374f72d44626207be32c439902b464c3d3d658b27a0c29d7107189d7aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b9cc4d75bad83ca4b442ce53584ba2058d9f735654e1925bd4e3b30136adf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0bbb7d3555c5e266def6f06d169472398be0bfe917c38b3861dc1d36d788c967
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c85203536db60a8c20cdb824e4db7bc726e1e864a68108be5e92465d9919731`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b82974da5a3d69a6ca94388b0a3f14e1fe28ce4d21ef9f4032d841f5325b32`  
		Last Modified: Tue, 13 Aug 2024 01:38:31 GMT  
		Size: 65.0 MB (64998376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4340b676a86c741205c6828d4978c183a33ab7cd51f670f731933698f6a24e2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151233149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358365cff60f4d16d7e2fab1ad5aec512ecfbe089679bd2d3b779001ce4f541d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172a0ce16e36a34ff88a2732bbe6037759cb39c60616bd29dbc966d3bb79ec3`  
		Last Modified: Tue, 13 Aug 2024 01:37:28 GMT  
		Size: 71.4 MB (71359436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a94c313135c49432dcc25f79928b6432dbe57b3358b23fe6f8e2731e7a13cee9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136916590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789762e26029931eda37c3b67f68f8756948dc5bce4177216ab908a7803afe0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a7954253b1f3af858d514d5a50598aad4e02214e66bf45ff119714d2d5fd0`  
		Last Modified: Wed, 04 Sep 2024 23:08:21 GMT  
		Size: 65.4 MB (65415937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cb088f2d9bfba6b06089622747309a8a3e0272d0daa567059097be31e6d8c85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141312776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af870be03c1edab12a17bc767ce71cf4be64f10112ebde559f5afdea8b9762`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c43737168f685110fa0a3c4ec68bd02aecf241fa770d30b263bb78a2ad0f70`  
		Last Modified: Tue, 13 Aug 2024 01:26:30 GMT  
		Size: 67.3 MB (67269243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
