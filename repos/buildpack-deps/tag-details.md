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
$ docker pull buildpack-deps@sha256:ab3eb9b59d2b25be54d815162f150309fb31b5cfa3b8ddfa08b22c2992467fca
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
$ docker pull buildpack-deps@sha256:403e99cb3e6a44c9d67a55b500e7922a480feab2307f86c320f9c3d162e928cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37531440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ddac4e20573ec6610b0d0b10fa38fc6e3fd0e2c966e04ec32479da749b189f`
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
$ docker pull buildpack-deps@sha256:98b2accb4e17d922bb693b088fdb8684f5f16b60052b7afc2e7f536a999803cb
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
$ docker pull buildpack-deps@sha256:d576c9d3d2623a662f9147eafcf3d305cab76ea3b2f2811803b7a6ddcc5e6185
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282350393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5a0bf20163c749546f28feb8c6ea9c5e425f7005702c1c9895d04ae3a6ea23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345b5509344fd379350000c7ff7136f4bb9e0907683154a35e01c343d3aaa268`  
		Last Modified: Tue, 17 Sep 2024 00:52:12 GMT  
		Size: 45.5 MB (45477387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51503dd6ffc660c3a5cdfe4907a3f2bb56c131b33c0049777a99c9547d4d33e3`  
		Last Modified: Tue, 17 Sep 2024 00:52:49 GMT  
		Size: 190.2 MB (190244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7c8158415bfcc472b648151a318932f4cfe044041229bfcc0e1fda10f886e064
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (241997040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dfe2c00f04abf01ce6bafd5fcdf18ba0b4511afa6852b985dbab56398c74d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:36:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2411b9846cffe86b78ccc0ca0886e65974eebdb17ef941fd0ca8d1eac5aec`  
		Last Modified: Tue, 17 Sep 2024 01:42:59 GMT  
		Size: 49.0 MB (49027219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36b2f4a9e68f9e10270485abad7f4c1e7ec8abeaacfc1ba0fcf30408d609375`  
		Last Modified: Tue, 17 Sep 2024 01:43:26 GMT  
		Size: 150.7 MB (150677287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c6ed0dea25e024e9e2507254230750ff1e00e5423ef07bfc042b37be8fcb75b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273272442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36d2b0d0624beb046d241fcd7f52d980a863d7cc0fe39753355797167849326`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:23:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264b868c8f7995878c840df83362abf1620d913a715a5035f70e221e4c6c99e`  
		Last Modified: Tue, 17 Sep 2024 01:29:34 GMT  
		Size: 15.7 MB (15671052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b7e7ec07731d713e422c894a544b37e91f78cd6070be19a84193ceb2721a7a`  
		Last Modified: Tue, 17 Sep 2024 01:29:49 GMT  
		Size: 45.4 MB (45436225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b7aec9dda1e1b6b5ef7e69acc15bc8d0d208cdbf89898ab86a5046cc1f63f7`  
		Last Modified: Tue, 17 Sep 2024 01:30:14 GMT  
		Size: 182.2 MB (182211960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f66db98810f9414a05224f51a825d0fbb520cbf715adcfdb591df4ddda0f3762
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301420056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b56948e3c3a192f7459b0053798fb59c67fcceadccd8d8fe23ee0c53c3e2c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c162e72cd72ec90c41417f91a23cfce5a2b5820e5406899302bfea8ba48237b`  
		Last Modified: Tue, 17 Sep 2024 00:53:33 GMT  
		Size: 50.6 MB (50641952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b3d9da5a3b09573aa1743c12128740b6a301436f0d3ba2435ecdef70d9898`  
		Last Modified: Tue, 17 Sep 2024 00:54:10 GMT  
		Size: 196.6 MB (196641767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:963e4ae4e1c3226c12e980267912197fb63345626660613ef58b811c4f68f4b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332417808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5d16f2a6f41210556fc201c48c67a5f511c7a9bc76cf06d5407ea3b198ea1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:19:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ff4b62acbc4050fdf30112f7c0382ff10d99ecdd5fc869c02c029d9a9c27f`  
		Last Modified: Tue, 17 Sep 2024 02:37:51 GMT  
		Size: 53.9 MB (53938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719620108ad09e130bfae61573bb9a6d67dd3fba2631d277f5c686f678d0247b`  
		Last Modified: Tue, 17 Sep 2024 02:42:18 GMT  
		Size: 230.1 MB (230106094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3ee15b8da1fe9d0464f8361abe248664974bf58e7b2c30af91163c16c5c11ecf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264103990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7fba033f71ab0b7b0282d6e61e7ca416b5fb0948d5b78ae1eb0cfd43c7fbef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:24:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054f4588e2fa050fc15cddee8730098abc2d2c3a235c7296c6d7d50c4a7b4a36`  
		Last Modified: Tue, 17 Sep 2024 01:29:17 GMT  
		Size: 47.1 MB (47062470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f0c1001912d6749947e8b3ceda12389dbbe49519dcf8a58eeed2137e009fa0`  
		Last Modified: Tue, 17 Sep 2024 01:29:43 GMT  
		Size: 169.3 MB (169307256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:91ef35765e02629e169edf1e4b2f66644f6169da5bdace2ecbf1d676bf15ec20
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
$ docker pull buildpack-deps@sha256:5ca2897281b063ee5aee00397d461cd1c5fc63a7385b596758176a2d8c37c369
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46628635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0999cd855bf065bf57ef39f3fc4175a91e117a598a2cd9acfb4622289c560f77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7378fd8b9079c627cbf64e65e2cc05f4434545bbee435a0392ce6e61d3173d11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42292534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106e99ee95aefcfa2630c3d9ba65a826d8685c1c826d3d3dc2c3175b9b81aa9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1bd733d8f43eb3269a637b6cab53d1a4e82db1825115830611877692c9e2c642
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45624257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d22c81d768991f54c472bbd4aaa2eea54f3732e2fe82ca8cbe3d9cb2c0ab2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264b868c8f7995878c840df83362abf1620d913a715a5035f70e221e4c6c99e`  
		Last Modified: Tue, 17 Sep 2024 01:29:34 GMT  
		Size: 15.7 MB (15671052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad6152b94fdc26d3243e31944ad6bf88f2fe0e2bc487a198202cc02a68b1d1e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54136337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8850ca23b16189c702035ca8031796c2fd0330fa6314e0a1a29dc8af2004306`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a3718ec79f151ea424a0e2237cd6e1074348ed31dbc2fd83ada601b1997e0111
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48372793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb46e4e0a703fd6d8d1d23976dfd0072e7242a7b3fb99daf90da3d103a2d7ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:00ba728c2bdaa3c28520c2f2f3e309ace3751a0d290526d178071175db6debec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47734264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2bd27d12d23454fcb655a1b0d44b1033f1ac6ee97c980f48820646bbfd18c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:beaa7995dc76b74b97dcfd4bcf6f8e22c2534918c2466f79de6f7c34b84c1e18
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
$ docker pull buildpack-deps@sha256:38f6a114e794136a109f51b1b544436189cf0728dc677f0a754fc7b53fd03776
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92106022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3612b101e2f2bd264ed2b1b752cf2ac81648cda3d9b853bcddaa730076cc996`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345b5509344fd379350000c7ff7136f4bb9e0907683154a35e01c343d3aaa268`  
		Last Modified: Tue, 17 Sep 2024 00:52:12 GMT  
		Size: 45.5 MB (45477387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2bf76b1e82b3dceb7f4b1819fbe0fbe89dcbdc38587d5276953ef7b9ef439a5c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91319753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e60486b55682b93ba1011636395113b3f97ba6af8705b70b7756688821308fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2411b9846cffe86b78ccc0ca0886e65974eebdb17ef941fd0ca8d1eac5aec`  
		Last Modified: Tue, 17 Sep 2024 01:42:59 GMT  
		Size: 49.0 MB (49027219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3670648c790c06cfa89dc784325745024bd60f761abcdf8335113a1f65c31901
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91060482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc63eb103e1aa9de69bd39040dd7165fbcf8b826545b96e6b97ab7a5074c955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264b868c8f7995878c840df83362abf1620d913a715a5035f70e221e4c6c99e`  
		Last Modified: Tue, 17 Sep 2024 01:29:34 GMT  
		Size: 15.7 MB (15671052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b7e7ec07731d713e422c894a544b37e91f78cd6070be19a84193ceb2721a7a`  
		Last Modified: Tue, 17 Sep 2024 01:29:49 GMT  
		Size: 45.4 MB (45436225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9774db35e6c60cf531e99f6c1cba0b8fac37fffcc3042858d68629f11a48ff6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104778289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be963492fee0a35b2b10aa77ca5245bab5b109a1df21c1ed0c51f06b15aadfb6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c162e72cd72ec90c41417f91a23cfce5a2b5820e5406899302bfea8ba48237b`  
		Last Modified: Tue, 17 Sep 2024 00:53:33 GMT  
		Size: 50.6 MB (50641952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9ab5f2e960dc494c8f0f6f4b5a9abf7553fabe39237b72a405f1997f010adea0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102311714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46af3b83629fcb16320417a5af5fdd466e39a6869c8b022ad90479fa04eddb7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ff4b62acbc4050fdf30112f7c0382ff10d99ecdd5fc869c02c029d9a9c27f`  
		Last Modified: Tue, 17 Sep 2024 02:37:51 GMT  
		Size: 53.9 MB (53938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:950a32a40ed79336723c2dff02c75ddb043df2300c510f551ba1d608fde8bf8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94796734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d4ca34652c51504002797c1d31bb2cbe0a0707f536f53fad8242135249abe7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054f4588e2fa050fc15cddee8730098abc2d2c3a235c7296c6d7d50c4a7b4a36`  
		Last Modified: Tue, 17 Sep 2024 01:29:17 GMT  
		Size: 47.1 MB (47062470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10`

```console
$ docker pull buildpack-deps@sha256:a33244dbed25bac2b8d77db39b132651218e42c2e083c4697be1b857383f3160
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
$ docker pull buildpack-deps@sha256:d2f79a85662943a991c08570fae8d4254810f5c2eeb7095f0f29d5a2768995bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296419022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3ddbc388031d479fd74ae1fb6b94a993aef08140fa98d7510ebd8ac0d5eeab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:50:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebac33bb0b35e8874ec506bbc4ce286511296d30234e78372cf6cdb13cbb27`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 46.8 MB (46817542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ee46566cba794047eba87b2fd06bd5a82ab02d8851b283f9019c9fa520e4d`  
		Last Modified: Tue, 17 Sep 2024 00:53:49 GMT  
		Size: 199.3 MB (199256957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ba9afc0023cc915b7e3a8840b9d7ba2f8a97162240468a2dc9036a857d81202d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259494650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d130b4e8178104673f0b37b02aa5b8028ca898b96f9a8aa338a5f9291ee834`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:41:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc0b48238e77689d32490011b9eec7f8b42e661b5baadc8728d31db963ce0cb`  
		Last Modified: Tue, 17 Sep 2024 01:43:53 GMT  
		Size: 49.8 MB (49772451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d6a1034d6fff77d10d7026c062bf712997b493a0b03dc8e5202c87d041320e`  
		Last Modified: Tue, 17 Sep 2024 01:44:22 GMT  
		Size: 161.5 MB (161519377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a08ca8bc6ffcafaba7ab32e2016936f74b47e9c6ee780928db80ce8049710311
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289969552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d9c789cf9c6117f1376ed80ae327feeeefefb61cbb0f6d0387de8c31fe361f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:28:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6b6483c3ac4e3d3df1b1381200ba57b3548bddcc959674a665f97651815fd`  
		Last Modified: Tue, 17 Sep 2024 01:30:40 GMT  
		Size: 46.8 MB (46766606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ba8218c840b5d90dfec54e6a3ee71ca42cd01bb9354a1ddaabb66a28b091ac`  
		Last Modified: Tue, 17 Sep 2024 01:31:10 GMT  
		Size: 193.3 MB (193274154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47e3cb364c767ca79dcfdb7fa2b75236f9b7025117bb5f8bada7be12437ade14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313377841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f877860200083bf23b3a311cba3d2d13d59ed44cf54773f2408c1676d001348b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:51:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032b3cccdd32b4010c1af161c1a432b31b8a95216f55327e02c652bd9616d31`  
		Last Modified: Tue, 17 Sep 2024 00:54:43 GMT  
		Size: 52.2 MB (52154832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7270aa96f49220e8ef5b229b1e9419186895d510137b9798c40e07a17796a`  
		Last Modified: Tue, 17 Sep 2024 00:55:19 GMT  
		Size: 204.3 MB (204333367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b8de50a98489d37d99d315cf2bb8771efdb7cf7fea091eef922c49b4161fa536
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 MB (389023176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8032fabfec89a24ffed66b5a643c9ac7eff935f42ee7bfd8aed16d3f6a77156`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:30:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db76789a2225592ba3f2c14ad9b00436b5d8aa72d91ad76d779dbdb33026fb`  
		Last Modified: Tue, 17 Sep 2024 02:43:56 GMT  
		Size: 55.0 MB (54968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41f993555922f589e5a2ccb58922282904a47cf97af5b42a198c162bfb51304`  
		Last Modified: Tue, 17 Sep 2024 02:49:11 GMT  
		Size: 279.7 MB (279696107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:da575540d80014352eb7a82d8c0890b5981c80e05ad2bb3de565aba9fda57e74
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274112914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea4f841bd56b23e6f39d02c35c7b72bed1f4329638b429789994a1f5ea9b5d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:27:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3709c28ea82a54374ee542db4b1e24030f79925aa8d7be6969a213a51299ee8c`  
		Last Modified: Tue, 17 Sep 2024 01:30:07 GMT  
		Size: 48.2 MB (48228132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a474bb4f20a52b9d20b5366eba94d7644adfc04dd8c3970953a16989ee9b6`  
		Last Modified: Tue, 17 Sep 2024 01:30:33 GMT  
		Size: 174.4 MB (174412278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-curl`

```console
$ docker pull buildpack-deps@sha256:e6fe56081e67bacaab0dec44568054854e1f37f10e17c59bf27708e1643f4fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:24.10-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b49b76bb576b4b3fc4f23701ee0a02bbbcb8eae159af9437c5f38f8178785c6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50344523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d4f2a21fc37da45dbb4b161dce07c77ba261fc392b03124a232a0bf44f592f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e605c05d25df4b49d8af9efbf30347b162a511257129d36cfe24b8fe2d507f76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48202822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eadc3eeb0c6a0a6dbc8ba82bbf70611ffdfe5389b2121559df02ef1ce36fb65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e8422ed2ff67797ea95be593ab27072a9a86c6e691541b0a14387ef94d7bd0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49928792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7850bef05e6df56be681b474d0d64f52065492124b39597ba075e45a13998b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c31ef5cefc510370fd2e0d41f558d4a381ecade8e7168378ee6bc5d0309e33e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56889642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0792239655ab9185bcd0a45c457efa02d805aa08515f9b3acaaf76d9fbd01bf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4ae79cdb114f2861368f700eacdc4ad08777dae4bd3b8bd7881c81cb278039a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54358272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26aff06acb6b810e6e4af407d531b74793b840950c46f35059d219013ce2b59d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d60028eb750564e483916b83511cb71d3e7b2e370e71d4ca0822f1267d543266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51472504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638b81654880903527f80e0488e767bc50564d525c4615b1cf2d72d715e4e0d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-scm`

```console
$ docker pull buildpack-deps@sha256:e7a8f3c1918856b8dbbe6d6aca20652a01512da2c6aed6b46cc95f20872cfcf0
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
$ docker pull buildpack-deps@sha256:1dbfd363c7265b73108465a8d3d29f0f9f581cb47beaad4ea0b3401cc66bad85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97162065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11d235b4586dfae5f82c5113a4bcc2c2f300aec0770c713922eb195365e78a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebac33bb0b35e8874ec506bbc4ce286511296d30234e78372cf6cdb13cbb27`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 46.8 MB (46817542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:12a47b46a874c599524492f8c571093df7d2524b0181552b851ecab6e85524d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97975273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417cccdaf24873a75e31ece8146224d802f454a148b4956fb9e14499f69a4052`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc0b48238e77689d32490011b9eec7f8b42e661b5baadc8728d31db963ce0cb`  
		Last Modified: Tue, 17 Sep 2024 01:43:53 GMT  
		Size: 49.8 MB (49772451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:373b593b8fcc2bc70185776e5973a9dd7b5c0bfeb3249d6ea4471469f317f930
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96695398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57475d81c6eeec3edc4a5d1a241ba02add703605758ade1eb02d30ca7ac7593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6b6483c3ac4e3d3df1b1381200ba57b3548bddcc959674a665f97651815fd`  
		Last Modified: Tue, 17 Sep 2024 01:30:40 GMT  
		Size: 46.8 MB (46766606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d6c7636a492027cadedc80b2be66033e88bcb71afbfb869d1399a6e8bed8e49a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109044474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9076d4d7af26071c76e0e56979ffaf8e0a166374403bcb86b9496ffdfb4237e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032b3cccdd32b4010c1af161c1a432b31b8a95216f55327e02c652bd9616d31`  
		Last Modified: Tue, 17 Sep 2024 00:54:43 GMT  
		Size: 52.2 MB (52154832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e27480fb5658d17fcad2c1b7a265bc681a9957eb3fb549267852b8893976201
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109327069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11b0a5e81034dc297b460e20a85d5365a9774cc36218611effdb2c1134b6e47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db76789a2225592ba3f2c14ad9b00436b5d8aa72d91ad76d779dbdb33026fb`  
		Last Modified: Tue, 17 Sep 2024 02:43:56 GMT  
		Size: 55.0 MB (54968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:932d5e55c820ee37ded13972b2005a7d5a8b347daccda453bb92a0e6d55376fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99700636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d535f4dfc10d95fa40a20365b6ac144cf64260f38800c57559d0cd38ac0d61ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3709c28ea82a54374ee542db4b1e24030f79925aa8d7be6969a213a51299ee8c`  
		Last Modified: Tue, 17 Sep 2024 01:30:07 GMT  
		Size: 48.2 MB (48228132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:cb49daeebc6c078ad9e670382cdeff531fa04168c58933172f6dcd8b24ded702
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
$ docker pull buildpack-deps@sha256:8cf9eae37563c39a03d8b10a514b7ef02d5761aaf0546afd98a009180a79fedb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316142488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d77c14f11524ffaa6068d3a3f03eb263198db066fd37bf735169568fa17164`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:16:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bcb55460b2c2b07856962a4787935d0468bccb7c9dfa177433fa022f264f26`  
		Last Modified: Thu, 05 Sep 2024 00:24:55 GMT  
		Size: 184.6 MB (184553262 bytes)  
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
$ docker pull buildpack-deps@sha256:77880ab350ae8376ea67e1c07e6ec50225ed4adb050ec1ddf385028fd0eb9d0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351642567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c3b841cea75479af0775e87f568570666e00fa91f3eee2ba16f52a23e94e73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:13:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:14737c83f5b55bbada462ce86f67f71c256ff429e1c5b94a7f457569882993b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326003486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaa4c2efdc68becbf386c20c0a170c098a9f2d56689a5b569ffc816c1c143a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:54:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f8cb8fc9c5f50bae748d45f12febe8141263b15997a428733fa15f9121148d`  
		Last Modified: Wed, 04 Sep 2024 23:15:54 GMT  
		Size: 189.8 MB (189827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:16e9e53051615bb49ed45c50d26b19e6a3d624ad240d34c4787af1f52e2c160a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363138602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c01177f587771042c516c6f8cba97b8071fc9e9cc063bc3e87edc666e3e5bee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:03:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f161dd3959faa2f30fc05f50f11de2ff1ae36632b37e08822b40bdd9e596b6ad`  
		Last Modified: Wed, 04 Sep 2024 23:14:38 GMT  
		Size: 214.3 MB (214285993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22f500481e64f18d6090a9a5a37ce02943f8d5394252ad3cad48e8c4d32c1883
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001882b4a0aabecc2d9f853e96cadabde59f35f44ea56357deb7255d313c42d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18612060b30c9f1db538f5e79e46ea0534fafb1c79e714e74e11a1b56e69c56d`  
		Last Modified: Thu, 05 Sep 2024 00:00:45 GMT  
		Size: 183.3 MB (183289806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:3ce25ed8fe89738778796426084550ee9bc6f3da1081f73a271cf804b4cf9144
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
$ docker pull buildpack-deps@sha256:7391eeef017abf3dc7764528610e6334e284ff14f822b878ac2705e875ebd0f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70062429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab48ea956175da7a435b1258b74f1046ec646e218ef6b57ede31bdd4effcb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
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
$ docker pull buildpack-deps@sha256:85035f6dac04f641efde596e73116d0df38aa82798a45d89d6842315d499f58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8743c0a9eb82230d6f4ccd2ea96817b3753288a530312e5c8a8374b80904edb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

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

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:201b3d44b674e1ff8bac37b9b2064a502fef6557f821466253959ead71f332ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79264159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ef92d1203e95d5305ab675bfd01bba603da95ee5d9e91a5166014001e48ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d4640407bec198a10920cfe4f1e7c39f51d0f7347c498c1e7b4374ea57fa78b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71991388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d59091a65171d25d8f31d2f54baae3cf9a801ce554104397bc466fce40d284f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:b1a3fc06fef89bdb52574d1046a5a8e3fdc39fd710800bb42bc952eb38891fbc
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
$ docker pull buildpack-deps@sha256:f3a42de0dc2ce296f3b3b76ef08f7bdb77524a0a597fd1c044d54dd7341fedc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131589226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070a8135c422aaf7d325113dfcbc72baf6d75dff631f659fb2e1daed799e35ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
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
$ docker pull buildpack-deps@sha256:c2c1fed2fa16483d3c4c8c64cb0f011a7a6512676f9cb5fd21997e3767d0b983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141460953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e524eb07a1b6a66b919ec2c0f72b5ca9bcb6a0f68596051367ed1e10e3975c38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:88b5267bd9605330d451926120f1d6033450530ae93c784644161be024237557
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136176441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cfba6784ced9ecdf572656db14c53f8c6220edc2f9c6c15879796fdac5f1ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d36cb70e85bac41799ca9e2563b5d53a331f678c8103720bdffde2a95d1f6c02
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148852609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106eeee8b0ab29b3c4ed5ceeab253d274dffba6670ad6957882efadde371e1c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c5d375454de128aad302d578dc028cc0945b2a60f637c5eb10c3048e8aff1ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135142057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3655812cd43a04c6f0ef2bbc001576d9617038e288402e1f15b6b730b780e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:3745d0463037e69da15d81fdbeb85b59e067d59b067d7730e418da018a37037b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull buildpack-deps@sha256:0237bb3f18e55070cc4d4e66a86792632c663baf617d5d034d6342ecb3427c51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295525114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34973007d9e0c92743b32b3397dcaf8d9846a705e8daba2113613ae715f8d831`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:17:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:18:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a961b5130e4ecfa7355c211a605995662ab52f22cdedca888a80a28b50499`  
		Last Modified: Thu, 05 Sep 2024 00:25:23 GMT  
		Size: 52.3 MB (52329511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722539d9a39ccb4043e4974ec89b17b8abff2a5cab04be7be1490350d3f7a9a7`  
		Last Modified: Thu, 05 Sep 2024 00:25:54 GMT  
		Size: 175.2 MB (175237132 bytes)  
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
$ docker pull buildpack-deps@sha256:ba2485293d0b4dd77696e3be78c4223eaf4ea315a0ec5a3550c316472e2b7d51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328339549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85b99d068db2cb99bbdb1a45a847c9f74527919ceb431aebf617f2d11ae41c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:15:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:980aed3656d8ea3aeb8695a298c235944d7070f9c6b2dcaf8ee03e0b7a1565be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (331002231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f4f9f54d0a33d3464fc5cc29ceaab63860acfc146d6eca9267890d6b9b971`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:06:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e63690195c44ac7f50e33f6d43a6b8585cd9ff85300742a379786f04859b6f10
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296082589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7beeb0431d44f34876f0ef2249e7d13fb18d8516e0ce267ed6a0b740801037`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:54:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:d4e3f066cbb79d760e094a9a5fe70440072b9c15f523a39472cb5e5de308e20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull buildpack-deps@sha256:8ebfacf3feed4218f9e12eb5cee975a5057d03049a1b15398e9fb5a28fc1d300
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67958471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a482f2c7d653185b09ffd82af2b1df92db3b06ba2b6b043cd2a6ac064bc809`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
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
$ docker pull buildpack-deps@sha256:d16cccfcd14e808bcf3c48466f552d4fcab63c772f594f8a5c61db5aab84901c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2935c69dd2b84af5ebe6f9f2e14ff454980becd6ad019c271c4c1bbe20b766`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b0c44eec3cf0efabb2a856de91bc08e41348c65692be30a61a648130acb1a606
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75716340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531a5affad292f28c15e65049ce4833d4028619916ba23511818f7f815703a5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c4f581b3e295ad448ff126d8e1c343741cd89f99a5da30ec6876f5ccbb34616
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68959590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b95c547ebd20c6b67b00d60bb7f0519e8220ae8bebb7034450158166ba3a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:916f1e29fadbfdcf4aed52ff1cd3758582bdbfd623ceb69874267da932e86cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull buildpack-deps@sha256:4c06a74210a7db91364077a9fe7365bdfc7268d6fa80a6733eb28a3f3229b96e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120287982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20abbc49ec77360296bff031311d5f6240059920b40f7120d160d16ba9dac17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:17:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a961b5130e4ecfa7355c211a605995662ab52f22cdedca888a80a28b50499`  
		Last Modified: Thu, 05 Sep 2024 00:25:23 GMT  
		Size: 52.3 MB (52329511 bytes)  
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
$ docker pull buildpack-deps@sha256:13d18539ed3902e8a9231be49b3c307ff4e504fd3201e713ed0961852c8e26c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128374542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae664c7e3d74ee3cb5cffe33cf826fab872c7247fb3c282651de0b6440d0c861`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2ca5c5b72629d7a216236a75a039c247c5f99a00898a709135841789ed956ad6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134588881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729273c02ba56f0575a063fc72d9f178390fbb3fc105eb7cca37395aae6627b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bb349a664e79d4d97b88c7f9c8add42a6bfe343e0f210b07592ff7470cd46fb7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123034674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4664f6689b64ee9639f5528c7234e5537622fb2dfb1b3587f2c75a7e781ca43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:3ce25ed8fe89738778796426084550ee9bc6f3da1081f73a271cf804b4cf9144
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
$ docker pull buildpack-deps@sha256:7391eeef017abf3dc7764528610e6334e284ff14f822b878ac2705e875ebd0f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70062429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab48ea956175da7a435b1258b74f1046ec646e218ef6b57ede31bdd4effcb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
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
$ docker pull buildpack-deps@sha256:85035f6dac04f641efde596e73116d0df38aa82798a45d89d6842315d499f58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8743c0a9eb82230d6f4ccd2ea96817b3753288a530312e5c8a8374b80904edb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

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

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:201b3d44b674e1ff8bac37b9b2064a502fef6557f821466253959ead71f332ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79264159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ef92d1203e95d5305ab675bfd01bba603da95ee5d9e91a5166014001e48ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d4640407bec198a10920cfe4f1e7c39f51d0f7347c498c1e7b4374ea57fa78b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71991388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d59091a65171d25d8f31d2f54baae3cf9a801ce554104397bc466fce40d284f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
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
$ docker pull buildpack-deps@sha256:ab3eb9b59d2b25be54d815162f150309fb31b5cfa3b8ddfa08b22c2992467fca
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
$ docker pull buildpack-deps@sha256:403e99cb3e6a44c9d67a55b500e7922a480feab2307f86c320f9c3d162e928cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37531440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ddac4e20573ec6610b0d0b10fa38fc6e3fd0e2c966e04ec32479da749b189f`
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

### `buildpack-deps:jammy-scm` - linux; amd64

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
$ docker pull buildpack-deps@sha256:cb49daeebc6c078ad9e670382cdeff531fa04168c58933172f6dcd8b24ded702
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
$ docker pull buildpack-deps@sha256:8cf9eae37563c39a03d8b10a514b7ef02d5761aaf0546afd98a009180a79fedb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316142488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d77c14f11524ffaa6068d3a3f03eb263198db066fd37bf735169568fa17164`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:16:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bcb55460b2c2b07856962a4787935d0468bccb7c9dfa177433fa022f264f26`  
		Last Modified: Thu, 05 Sep 2024 00:24:55 GMT  
		Size: 184.6 MB (184553262 bytes)  
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
$ docker pull buildpack-deps@sha256:77880ab350ae8376ea67e1c07e6ec50225ed4adb050ec1ddf385028fd0eb9d0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351642567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c3b841cea75479af0775e87f568570666e00fa91f3eee2ba16f52a23e94e73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:13:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:14737c83f5b55bbada462ce86f67f71c256ff429e1c5b94a7f457569882993b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326003486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaa4c2efdc68becbf386c20c0a170c098a9f2d56689a5b569ffc816c1c143a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:54:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f8cb8fc9c5f50bae748d45f12febe8141263b15997a428733fa15f9121148d`  
		Last Modified: Wed, 04 Sep 2024 23:15:54 GMT  
		Size: 189.8 MB (189827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:16e9e53051615bb49ed45c50d26b19e6a3d624ad240d34c4787af1f52e2c160a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363138602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c01177f587771042c516c6f8cba97b8071fc9e9cc063bc3e87edc666e3e5bee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:03:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f161dd3959faa2f30fc05f50f11de2ff1ae36632b37e08822b40bdd9e596b6ad`  
		Last Modified: Wed, 04 Sep 2024 23:14:38 GMT  
		Size: 214.3 MB (214285993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22f500481e64f18d6090a9a5a37ce02943f8d5394252ad3cad48e8c4d32c1883
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001882b4a0aabecc2d9f853e96cadabde59f35f44ea56357deb7255d313c42d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18612060b30c9f1db538f5e79e46ea0534fafb1c79e714e74e11a1b56e69c56d`  
		Last Modified: Thu, 05 Sep 2024 00:00:45 GMT  
		Size: 183.3 MB (183289806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:98b2accb4e17d922bb693b088fdb8684f5f16b60052b7afc2e7f536a999803cb
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
$ docker pull buildpack-deps@sha256:d576c9d3d2623a662f9147eafcf3d305cab76ea3b2f2811803b7a6ddcc5e6185
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282350393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5a0bf20163c749546f28feb8c6ea9c5e425f7005702c1c9895d04ae3a6ea23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345b5509344fd379350000c7ff7136f4bb9e0907683154a35e01c343d3aaa268`  
		Last Modified: Tue, 17 Sep 2024 00:52:12 GMT  
		Size: 45.5 MB (45477387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51503dd6ffc660c3a5cdfe4907a3f2bb56c131b33c0049777a99c9547d4d33e3`  
		Last Modified: Tue, 17 Sep 2024 00:52:49 GMT  
		Size: 190.2 MB (190244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7c8158415bfcc472b648151a318932f4cfe044041229bfcc0e1fda10f886e064
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (241997040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dfe2c00f04abf01ce6bafd5fcdf18ba0b4511afa6852b985dbab56398c74d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:36:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2411b9846cffe86b78ccc0ca0886e65974eebdb17ef941fd0ca8d1eac5aec`  
		Last Modified: Tue, 17 Sep 2024 01:42:59 GMT  
		Size: 49.0 MB (49027219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36b2f4a9e68f9e10270485abad7f4c1e7ec8abeaacfc1ba0fcf30408d609375`  
		Last Modified: Tue, 17 Sep 2024 01:43:26 GMT  
		Size: 150.7 MB (150677287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c6ed0dea25e024e9e2507254230750ff1e00e5423ef07bfc042b37be8fcb75b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273272442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36d2b0d0624beb046d241fcd7f52d980a863d7cc0fe39753355797167849326`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:23:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264b868c8f7995878c840df83362abf1620d913a715a5035f70e221e4c6c99e`  
		Last Modified: Tue, 17 Sep 2024 01:29:34 GMT  
		Size: 15.7 MB (15671052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b7e7ec07731d713e422c894a544b37e91f78cd6070be19a84193ceb2721a7a`  
		Last Modified: Tue, 17 Sep 2024 01:29:49 GMT  
		Size: 45.4 MB (45436225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b7aec9dda1e1b6b5ef7e69acc15bc8d0d208cdbf89898ab86a5046cc1f63f7`  
		Last Modified: Tue, 17 Sep 2024 01:30:14 GMT  
		Size: 182.2 MB (182211960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f66db98810f9414a05224f51a825d0fbb520cbf715adcfdb591df4ddda0f3762
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301420056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b56948e3c3a192f7459b0053798fb59c67fcceadccd8d8fe23ee0c53c3e2c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c162e72cd72ec90c41417f91a23cfce5a2b5820e5406899302bfea8ba48237b`  
		Last Modified: Tue, 17 Sep 2024 00:53:33 GMT  
		Size: 50.6 MB (50641952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b3d9da5a3b09573aa1743c12128740b6a301436f0d3ba2435ecdef70d9898`  
		Last Modified: Tue, 17 Sep 2024 00:54:10 GMT  
		Size: 196.6 MB (196641767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:963e4ae4e1c3226c12e980267912197fb63345626660613ef58b811c4f68f4b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332417808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5d16f2a6f41210556fc201c48c67a5f511c7a9bc76cf06d5407ea3b198ea1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:19:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ff4b62acbc4050fdf30112f7c0382ff10d99ecdd5fc869c02c029d9a9c27f`  
		Last Modified: Tue, 17 Sep 2024 02:37:51 GMT  
		Size: 53.9 MB (53938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719620108ad09e130bfae61573bb9a6d67dd3fba2631d277f5c686f678d0247b`  
		Last Modified: Tue, 17 Sep 2024 02:42:18 GMT  
		Size: 230.1 MB (230106094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3ee15b8da1fe9d0464f8361abe248664974bf58e7b2c30af91163c16c5c11ecf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264103990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7fba033f71ab0b7b0282d6e61e7ca416b5fb0948d5b78ae1eb0cfd43c7fbef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:24:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054f4588e2fa050fc15cddee8730098abc2d2c3a235c7296c6d7d50c4a7b4a36`  
		Last Modified: Tue, 17 Sep 2024 01:29:17 GMT  
		Size: 47.1 MB (47062470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f0c1001912d6749947e8b3ceda12389dbbe49519dcf8a58eeed2137e009fa0`  
		Last Modified: Tue, 17 Sep 2024 01:29:43 GMT  
		Size: 169.3 MB (169307256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:91ef35765e02629e169edf1e4b2f66644f6169da5bdace2ecbf1d676bf15ec20
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
$ docker pull buildpack-deps@sha256:5ca2897281b063ee5aee00397d461cd1c5fc63a7385b596758176a2d8c37c369
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46628635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0999cd855bf065bf57ef39f3fc4175a91e117a598a2cd9acfb4622289c560f77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7378fd8b9079c627cbf64e65e2cc05f4434545bbee435a0392ce6e61d3173d11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42292534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106e99ee95aefcfa2630c3d9ba65a826d8685c1c826d3d3dc2c3175b9b81aa9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1bd733d8f43eb3269a637b6cab53d1a4e82db1825115830611877692c9e2c642
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45624257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d22c81d768991f54c472bbd4aaa2eea54f3732e2fe82ca8cbe3d9cb2c0ab2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264b868c8f7995878c840df83362abf1620d913a715a5035f70e221e4c6c99e`  
		Last Modified: Tue, 17 Sep 2024 01:29:34 GMT  
		Size: 15.7 MB (15671052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad6152b94fdc26d3243e31944ad6bf88f2fe0e2bc487a198202cc02a68b1d1e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54136337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8850ca23b16189c702035ca8031796c2fd0330fa6314e0a1a29dc8af2004306`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a3718ec79f151ea424a0e2237cd6e1074348ed31dbc2fd83ada601b1997e0111
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48372793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb46e4e0a703fd6d8d1d23976dfd0072e7242a7b3fb99daf90da3d103a2d7ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:00ba728c2bdaa3c28520c2f2f3e309ace3751a0d290526d178071175db6debec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47734264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2bd27d12d23454fcb655a1b0d44b1033f1ac6ee97c980f48820646bbfd18c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:beaa7995dc76b74b97dcfd4bcf6f8e22c2534918c2466f79de6f7c34b84c1e18
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
$ docker pull buildpack-deps@sha256:38f6a114e794136a109f51b1b544436189cf0728dc677f0a754fc7b53fd03776
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92106022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3612b101e2f2bd264ed2b1b752cf2ac81648cda3d9b853bcddaa730076cc996`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345b5509344fd379350000c7ff7136f4bb9e0907683154a35e01c343d3aaa268`  
		Last Modified: Tue, 17 Sep 2024 00:52:12 GMT  
		Size: 45.5 MB (45477387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2bf76b1e82b3dceb7f4b1819fbe0fbe89dcbdc38587d5276953ef7b9ef439a5c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91319753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e60486b55682b93ba1011636395113b3f97ba6af8705b70b7756688821308fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2411b9846cffe86b78ccc0ca0886e65974eebdb17ef941fd0ca8d1eac5aec`  
		Last Modified: Tue, 17 Sep 2024 01:42:59 GMT  
		Size: 49.0 MB (49027219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3670648c790c06cfa89dc784325745024bd60f761abcdf8335113a1f65c31901
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91060482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc63eb103e1aa9de69bd39040dd7165fbcf8b826545b96e6b97ab7a5074c955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264b868c8f7995878c840df83362abf1620d913a715a5035f70e221e4c6c99e`  
		Last Modified: Tue, 17 Sep 2024 01:29:34 GMT  
		Size: 15.7 MB (15671052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b7e7ec07731d713e422c894a544b37e91f78cd6070be19a84193ceb2721a7a`  
		Last Modified: Tue, 17 Sep 2024 01:29:49 GMT  
		Size: 45.4 MB (45436225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9774db35e6c60cf531e99f6c1cba0b8fac37fffcc3042858d68629f11a48ff6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104778289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be963492fee0a35b2b10aa77ca5245bab5b109a1df21c1ed0c51f06b15aadfb6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c162e72cd72ec90c41417f91a23cfce5a2b5820e5406899302bfea8ba48237b`  
		Last Modified: Tue, 17 Sep 2024 00:53:33 GMT  
		Size: 50.6 MB (50641952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9ab5f2e960dc494c8f0f6f4b5a9abf7553fabe39237b72a405f1997f010adea0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102311714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46af3b83629fcb16320417a5af5fdd466e39a6869c8b022ad90479fa04eddb7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ff4b62acbc4050fdf30112f7c0382ff10d99ecdd5fc869c02c029d9a9c27f`  
		Last Modified: Tue, 17 Sep 2024 02:37:51 GMT  
		Size: 53.9 MB (53938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:950a32a40ed79336723c2dff02c75ddb043df2300c510f551ba1d608fde8bf8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94796734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d4ca34652c51504002797c1d31bb2cbe0a0707f536f53fad8242135249abe7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054f4588e2fa050fc15cddee8730098abc2d2c3a235c7296c6d7d50c4a7b4a36`  
		Last Modified: Tue, 17 Sep 2024 01:29:17 GMT  
		Size: 47.1 MB (47062470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:3745d0463037e69da15d81fdbeb85b59e067d59b067d7730e418da018a37037b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull buildpack-deps@sha256:0237bb3f18e55070cc4d4e66a86792632c663baf617d5d034d6342ecb3427c51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295525114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34973007d9e0c92743b32b3397dcaf8d9846a705e8daba2113613ae715f8d831`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:17:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:18:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a961b5130e4ecfa7355c211a605995662ab52f22cdedca888a80a28b50499`  
		Last Modified: Thu, 05 Sep 2024 00:25:23 GMT  
		Size: 52.3 MB (52329511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722539d9a39ccb4043e4974ec89b17b8abff2a5cab04be7be1490350d3f7a9a7`  
		Last Modified: Thu, 05 Sep 2024 00:25:54 GMT  
		Size: 175.2 MB (175237132 bytes)  
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
$ docker pull buildpack-deps@sha256:ba2485293d0b4dd77696e3be78c4223eaf4ea315a0ec5a3550c316472e2b7d51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328339549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85b99d068db2cb99bbdb1a45a847c9f74527919ceb431aebf617f2d11ae41c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:15:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:980aed3656d8ea3aeb8695a298c235944d7070f9c6b2dcaf8ee03e0b7a1565be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (331002231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f4f9f54d0a33d3464fc5cc29ceaab63860acfc146d6eca9267890d6b9b971`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:06:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e63690195c44ac7f50e33f6d43a6b8585cd9ff85300742a379786f04859b6f10
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296082589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7beeb0431d44f34876f0ef2249e7d13fb18d8516e0ce267ed6a0b740801037`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:54:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:d4e3f066cbb79d760e094a9a5fe70440072b9c15f523a39472cb5e5de308e20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull buildpack-deps@sha256:8ebfacf3feed4218f9e12eb5cee975a5057d03049a1b15398e9fb5a28fc1d300
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67958471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a482f2c7d653185b09ffd82af2b1df92db3b06ba2b6b043cd2a6ac064bc809`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
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
$ docker pull buildpack-deps@sha256:d16cccfcd14e808bcf3c48466f552d4fcab63c772f594f8a5c61db5aab84901c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2935c69dd2b84af5ebe6f9f2e14ff454980becd6ad019c271c4c1bbe20b766`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b0c44eec3cf0efabb2a856de91bc08e41348c65692be30a61a648130acb1a606
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75716340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531a5affad292f28c15e65049ce4833d4028619916ba23511818f7f815703a5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c4f581b3e295ad448ff126d8e1c343741cd89f99a5da30ec6876f5ccbb34616
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68959590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b95c547ebd20c6b67b00d60bb7f0519e8220ae8bebb7034450158166ba3a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:916f1e29fadbfdcf4aed52ff1cd3758582bdbfd623ceb69874267da932e86cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull buildpack-deps@sha256:4c06a74210a7db91364077a9fe7365bdfc7268d6fa80a6733eb28a3f3229b96e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120287982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20abbc49ec77360296bff031311d5f6240059920b40f7120d160d16ba9dac17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:17:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a961b5130e4ecfa7355c211a605995662ab52f22cdedca888a80a28b50499`  
		Last Modified: Thu, 05 Sep 2024 00:25:23 GMT  
		Size: 52.3 MB (52329511 bytes)  
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
$ docker pull buildpack-deps@sha256:13d18539ed3902e8a9231be49b3c307ff4e504fd3201e713ed0961852c8e26c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128374542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae664c7e3d74ee3cb5cffe33cf826fab872c7247fb3c282651de0b6440d0c861`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2ca5c5b72629d7a216236a75a039c247c5f99a00898a709135841789ed956ad6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134588881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729273c02ba56f0575a063fc72d9f178390fbb3fc105eb7cca37395aae6627b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bb349a664e79d4d97b88c7f9c8add42a6bfe343e0f210b07592ff7470cd46fb7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123034674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4664f6689b64ee9639f5528c7234e5537622fb2dfb1b3587f2c75a7e781ca43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:a33244dbed25bac2b8d77db39b132651218e42c2e083c4697be1b857383f3160
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
$ docker pull buildpack-deps@sha256:d2f79a85662943a991c08570fae8d4254810f5c2eeb7095f0f29d5a2768995bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296419022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3ddbc388031d479fd74ae1fb6b94a993aef08140fa98d7510ebd8ac0d5eeab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:50:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebac33bb0b35e8874ec506bbc4ce286511296d30234e78372cf6cdb13cbb27`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 46.8 MB (46817542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ee46566cba794047eba87b2fd06bd5a82ab02d8851b283f9019c9fa520e4d`  
		Last Modified: Tue, 17 Sep 2024 00:53:49 GMT  
		Size: 199.3 MB (199256957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ba9afc0023cc915b7e3a8840b9d7ba2f8a97162240468a2dc9036a857d81202d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259494650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d130b4e8178104673f0b37b02aa5b8028ca898b96f9a8aa338a5f9291ee834`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:41:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc0b48238e77689d32490011b9eec7f8b42e661b5baadc8728d31db963ce0cb`  
		Last Modified: Tue, 17 Sep 2024 01:43:53 GMT  
		Size: 49.8 MB (49772451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d6a1034d6fff77d10d7026c062bf712997b493a0b03dc8e5202c87d041320e`  
		Last Modified: Tue, 17 Sep 2024 01:44:22 GMT  
		Size: 161.5 MB (161519377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a08ca8bc6ffcafaba7ab32e2016936f74b47e9c6ee780928db80ce8049710311
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289969552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d9c789cf9c6117f1376ed80ae327feeeefefb61cbb0f6d0387de8c31fe361f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:28:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6b6483c3ac4e3d3df1b1381200ba57b3548bddcc959674a665f97651815fd`  
		Last Modified: Tue, 17 Sep 2024 01:30:40 GMT  
		Size: 46.8 MB (46766606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ba8218c840b5d90dfec54e6a3ee71ca42cd01bb9354a1ddaabb66a28b091ac`  
		Last Modified: Tue, 17 Sep 2024 01:31:10 GMT  
		Size: 193.3 MB (193274154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47e3cb364c767ca79dcfdb7fa2b75236f9b7025117bb5f8bada7be12437ade14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313377841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f877860200083bf23b3a311cba3d2d13d59ed44cf54773f2408c1676d001348b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:51:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032b3cccdd32b4010c1af161c1a432b31b8a95216f55327e02c652bd9616d31`  
		Last Modified: Tue, 17 Sep 2024 00:54:43 GMT  
		Size: 52.2 MB (52154832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7270aa96f49220e8ef5b229b1e9419186895d510137b9798c40e07a17796a`  
		Last Modified: Tue, 17 Sep 2024 00:55:19 GMT  
		Size: 204.3 MB (204333367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b8de50a98489d37d99d315cf2bb8771efdb7cf7fea091eef922c49b4161fa536
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 MB (389023176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8032fabfec89a24ffed66b5a643c9ac7eff935f42ee7bfd8aed16d3f6a77156`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:30:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db76789a2225592ba3f2c14ad9b00436b5d8aa72d91ad76d779dbdb33026fb`  
		Last Modified: Tue, 17 Sep 2024 02:43:56 GMT  
		Size: 55.0 MB (54968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41f993555922f589e5a2ccb58922282904a47cf97af5b42a198c162bfb51304`  
		Last Modified: Tue, 17 Sep 2024 02:49:11 GMT  
		Size: 279.7 MB (279696107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:da575540d80014352eb7a82d8c0890b5981c80e05ad2bb3de565aba9fda57e74
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274112914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea4f841bd56b23e6f39d02c35c7b72bed1f4329638b429789994a1f5ea9b5d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:27:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3709c28ea82a54374ee542db4b1e24030f79925aa8d7be6969a213a51299ee8c`  
		Last Modified: Tue, 17 Sep 2024 01:30:07 GMT  
		Size: 48.2 MB (48228132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a474bb4f20a52b9d20b5366eba94d7644adfc04dd8c3970953a16989ee9b6`  
		Last Modified: Tue, 17 Sep 2024 01:30:33 GMT  
		Size: 174.4 MB (174412278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:e6fe56081e67bacaab0dec44568054854e1f37f10e17c59bf27708e1643f4fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b49b76bb576b4b3fc4f23701ee0a02bbbcb8eae159af9437c5f38f8178785c6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50344523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d4f2a21fc37da45dbb4b161dce07c77ba261fc392b03124a232a0bf44f592f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e605c05d25df4b49d8af9efbf30347b162a511257129d36cfe24b8fe2d507f76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48202822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eadc3eeb0c6a0a6dbc8ba82bbf70611ffdfe5389b2121559df02ef1ce36fb65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e8422ed2ff67797ea95be593ab27072a9a86c6e691541b0a14387ef94d7bd0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49928792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7850bef05e6df56be681b474d0d64f52065492124b39597ba075e45a13998b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c31ef5cefc510370fd2e0d41f558d4a381ecade8e7168378ee6bc5d0309e33e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56889642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0792239655ab9185bcd0a45c457efa02d805aa08515f9b3acaaf76d9fbd01bf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4ae79cdb114f2861368f700eacdc4ad08777dae4bd3b8bd7881c81cb278039a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54358272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26aff06acb6b810e6e4af407d531b74793b840950c46f35059d219013ce2b59d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d60028eb750564e483916b83511cb71d3e7b2e370e71d4ca0822f1267d543266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51472504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638b81654880903527f80e0488e767bc50564d525c4615b1cf2d72d715e4e0d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:e7a8f3c1918856b8dbbe6d6aca20652a01512da2c6aed6b46cc95f20872cfcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1dbfd363c7265b73108465a8d3d29f0f9f581cb47beaad4ea0b3401cc66bad85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97162065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11d235b4586dfae5f82c5113a4bcc2c2f300aec0770c713922eb195365e78a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebac33bb0b35e8874ec506bbc4ce286511296d30234e78372cf6cdb13cbb27`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 46.8 MB (46817542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:12a47b46a874c599524492f8c571093df7d2524b0181552b851ecab6e85524d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97975273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417cccdaf24873a75e31ece8146224d802f454a148b4956fb9e14499f69a4052`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc0b48238e77689d32490011b9eec7f8b42e661b5baadc8728d31db963ce0cb`  
		Last Modified: Tue, 17 Sep 2024 01:43:53 GMT  
		Size: 49.8 MB (49772451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:373b593b8fcc2bc70185776e5973a9dd7b5c0bfeb3249d6ea4471469f317f930
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96695398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57475d81c6eeec3edc4a5d1a241ba02add703605758ade1eb02d30ca7ac7593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6b6483c3ac4e3d3df1b1381200ba57b3548bddcc959674a665f97651815fd`  
		Last Modified: Tue, 17 Sep 2024 01:30:40 GMT  
		Size: 46.8 MB (46766606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d6c7636a492027cadedc80b2be66033e88bcb71afbfb869d1399a6e8bed8e49a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109044474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9076d4d7af26071c76e0e56979ffaf8e0a166374403bcb86b9496ffdfb4237e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032b3cccdd32b4010c1af161c1a432b31b8a95216f55327e02c652bd9616d31`  
		Last Modified: Tue, 17 Sep 2024 00:54:43 GMT  
		Size: 52.2 MB (52154832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e27480fb5658d17fcad2c1b7a265bc681a9957eb3fb549267852b8893976201
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109327069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11b0a5e81034dc297b460e20a85d5365a9774cc36218611effdb2c1134b6e47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db76789a2225592ba3f2c14ad9b00436b5d8aa72d91ad76d779dbdb33026fb`  
		Last Modified: Tue, 17 Sep 2024 02:43:56 GMT  
		Size: 55.0 MB (54968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:932d5e55c820ee37ded13972b2005a7d5a8b347daccda453bb92a0e6d55376fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99700636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d535f4dfc10d95fa40a20365b6ac144cf64260f38800c57559d0cd38ac0d61ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3709c28ea82a54374ee542db4b1e24030f79925aa8d7be6969a213a51299ee8c`  
		Last Modified: Tue, 17 Sep 2024 01:30:07 GMT  
		Size: 48.2 MB (48228132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:b1a3fc06fef89bdb52574d1046a5a8e3fdc39fd710800bb42bc952eb38891fbc
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
$ docker pull buildpack-deps@sha256:f3a42de0dc2ce296f3b3b76ef08f7bdb77524a0a597fd1c044d54dd7341fedc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131589226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070a8135c422aaf7d325113dfcbc72baf6d75dff631f659fb2e1daed799e35ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
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
$ docker pull buildpack-deps@sha256:c2c1fed2fa16483d3c4c8c64cb0f011a7a6512676f9cb5fd21997e3767d0b983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141460953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e524eb07a1b6a66b919ec2c0f72b5ca9bcb6a0f68596051367ed1e10e3975c38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:88b5267bd9605330d451926120f1d6033450530ae93c784644161be024237557
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136176441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cfba6784ced9ecdf572656db14c53f8c6220edc2f9c6c15879796fdac5f1ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d36cb70e85bac41799ca9e2563b5d53a331f678c8103720bdffde2a95d1f6c02
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148852609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106eeee8b0ab29b3c4ed5ceeab253d274dffba6670ad6957882efadde371e1c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c5d375454de128aad302d578dc028cc0945b2a60f637c5eb10c3048e8aff1ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135142057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3655812cd43a04c6f0ef2bbc001576d9617038e288402e1f15b6b730b780e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:bce7026ee0d4977cb13db09d859cf3c91989e16ee592d706aa03149027263992
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
$ docker pull buildpack-deps@sha256:90d185e94b3b2422df15f2e48c0b23148b1e19a892d2a255582922f9b9da3aab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333078604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f5a8b4103d91cf8a90202fae2cdee515fe2d83d51f833f2bdedde32a517217`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:21:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ad08e7d81f82d9e2c4214b3dfd3cce995412f651a08e233d2f09274292773`  
		Last Modified: Thu, 05 Sep 2024 00:26:24 GMT  
		Size: 63.7 MB (63691738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5fab79030c3084031070777f64892494b2cfbdfcd9d756b6a1a41e4a9fd6f1`  
		Last Modified: Thu, 05 Sep 2024 00:26:59 GMT  
		Size: 199.8 MB (199782011 bytes)  
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
$ docker pull buildpack-deps@sha256:4673f0b332d7be287dc13776cfac704af7b54427d8191b4c79fdaac67b32916f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368982385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54773087e8cdcf8c20b2927ca0a1324e9a64c9c0942afa24fcb5ed6d6dd4187c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:17:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676697198fdfee6917623f8c11e9e2725eb0d2fed789bf0e71473beb1651938`  
		Last Modified: Wed, 04 Sep 2024 23:22:51 GMT  
		Size: 68.0 MB (67999768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a071913506a26883892b5bcd5b7e56e30953b90b4bd5c9873aa87a5a33c7123b`  
		Last Modified: Wed, 04 Sep 2024 23:23:37 GMT  
		Size: 225.4 MB (225420586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b7838b4742be13db1d1a747b0acf5a27f7300e2a7c2a4dc5b3709cb5a8f4196c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342005334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f975a1417b3a376323be716cf65328753ef7d8d12b092220d4009e4de25c133a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:04:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac59bc75368032a1aacc11229b927d620146529073e342e9762c4d3c1ff58a`  
		Last Modified: Wed, 04 Sep 2024 23:17:12 GMT  
		Size: 65.0 MB (64982310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec11c68501cca6c2a0da847df5b55346b4f95eafda376070044cc117256d6d4d`  
		Last Modified: Wed, 04 Sep 2024 23:19:25 GMT  
		Size: 204.1 MB (204055737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5e30158940f6b7ed0a121ceba4f482966a825bd751badb19501048704f50164a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (375002708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec97870a6751c6cdd32726095b334ffe32519c68d454d1121b1eabaef714b9b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:09:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af665d962e383e3f1c7578bf8044f6cd38edea60132aae6dd8346eb0999613`  
		Last Modified: Wed, 04 Sep 2024 23:16:11 GMT  
		Size: 71.6 MB (71560086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a471ab9eb3c8df7c43d4364f980d88818e686ad1e8291753a6b86a16af2d77`  
		Last Modified: Wed, 04 Sep 2024 23:16:49 GMT  
		Size: 223.2 MB (223197670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:17af248bfbe1e8ab33b0e561eb6c0ef3686f0cedd557e35c4853def42575cd35
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442888142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c77ba538f9adf10fd862946d1177b5d2576c85e90415beb3ccfb0210ae5248c`
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
# Wed, 04 Sep 2024 23:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
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
	-	`sha256:b1b8269d3170ea5e0ed9b1314bea3a8b5949e212597ca4322a5cda142d67f33c`  
		Last Modified: Wed, 04 Sep 2024 23:14:00 GMT  
		Size: 306.0 MB (305971552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7b5bf9e982fa414441d9f4f9bc06696fb736a2898adade59a400466eec4a5776
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339634143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc28a71caf77ff0ab634c85987af98a59537a6b888e308d0c8da41cd42dc90d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:55:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:56:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fcd27216accec74418e978fea2c6be2752504c8ece95ef0dde330d8a5c092`  
		Last Modified: Thu, 05 Sep 2024 00:01:55 GMT  
		Size: 67.2 MB (67237737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5bb45295cabf007391a31614c906096557565683b0b07fdc3669d2d0ac113f`  
		Last Modified: Thu, 05 Sep 2024 00:02:23 GMT  
		Size: 198.0 MB (198023251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:850df8bb4645b2c35d3ab90f736c6415740341d7b1e25033572ce155f65ecc17
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
$ docker pull buildpack-deps@sha256:5c540b1b211c1efaafb1b4b86625cbd3bd7ae78eee9e3d68baedb2c3d6e2cc92
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69604855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1719edcde9f4bf97ae44287bebcef3f99df21e3c51e3d0d3f8f52b25692d7fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
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
$ docker pull buildpack-deps@sha256:553289d7d0ee3d06a9ca4771be21b82945013086f84b3d7a00d555c96d35e2aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75562031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fceead42a36bd5b0bc8be1827ce8000f4a436742bcb4b732564008d97cfb5c51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0c117689692b057acc8213bf376b412eff1499b594d99c9fdeeb8b793b8dd873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72967287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e41b859b97c6e171049841788de1a97a82477edd39d6477efccc6dd4ad4862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3e558c0209496b0526329fc8de9a8a2da7fefc99f9845dfb7a89bccb1d169e03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80244952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598fe339fe78f27fb2edfcc0109e809d2b7097801eefffdeab4eca9b49503f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
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
$ docker pull buildpack-deps@sha256:be0244159e3edd884c06faaff6483525d4c78c30b4c3eabfbde5ba3ee43dd4f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74373155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59b4514ac5e5cc01c98d02d36641460165f05546ebae0e8319d9c9bea567ecb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:471bc4b421e9679c2d03de9b202d5ba13d8dc5bac58151b95cf1d9fe878736b5
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
$ docker pull buildpack-deps@sha256:6f214b53497b9eb190b57aedfa8795b3a2aabc115bdfb664c43d7ecde50ea22a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133296593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefba7a5e499120643c9f46e4fbf7d581c6cf2524d19e01a2df5b060c69e75e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ad08e7d81f82d9e2c4214b3dfd3cce995412f651a08e233d2f09274292773`  
		Last Modified: Thu, 05 Sep 2024 00:26:24 GMT  
		Size: 63.7 MB (63691738 bytes)  
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
$ docker pull buildpack-deps@sha256:aa2ecf738666a323f7e7d8c40adf61d1138d84212e4b23d6c39bbb7ea60a62bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143561799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e36838e7d0962b487fa77b20613101f2b9c894ccb77220e1de7af2b9eef4c0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676697198fdfee6917623f8c11e9e2725eb0d2fed789bf0e71473beb1651938`  
		Last Modified: Wed, 04 Sep 2024 23:22:51 GMT  
		Size: 68.0 MB (67999768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8af6d4267f7b2ae3a48c5178fc412b19cdb2a9bffd157640981b2c023643dd41
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137949597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3348df9b9deb7caa5c063fbbba211170c944cfb05d10a13b94ad8b67cbfab8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac59bc75368032a1aacc11229b927d620146529073e342e9762c4d3c1ff58a`  
		Last Modified: Wed, 04 Sep 2024 23:17:12 GMT  
		Size: 65.0 MB (64982310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e8aed150e2bfc5c50e50f61c2df8c049f4679922d12e85696155ceb7bbd643f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151805038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b8defb7b402fa6d091d061e89f4fb5739b404d875b4b71417e564957598438`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af665d962e383e3f1c7578bf8044f6cd38edea60132aae6dd8346eb0999613`  
		Last Modified: Wed, 04 Sep 2024 23:16:11 GMT  
		Size: 71.6 MB (71560086 bytes)  
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
$ docker pull buildpack-deps@sha256:1a7538359bf9f1b11be91b4bc365f4a674e73db7cf8b9a58e2a5678e3e7db3b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141610892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8dab2bdfd8e752900399d53743d189ceed42554ec901984badaf89e26a2bb3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:55:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fcd27216accec74418e978fea2c6be2752504c8ece95ef0dde330d8a5c092`  
		Last Modified: Thu, 05 Sep 2024 00:01:55 GMT  
		Size: 67.2 MB (67237737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:cb49daeebc6c078ad9e670382cdeff531fa04168c58933172f6dcd8b24ded702
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
$ docker pull buildpack-deps@sha256:8cf9eae37563c39a03d8b10a514b7ef02d5761aaf0546afd98a009180a79fedb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316142488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d77c14f11524ffaa6068d3a3f03eb263198db066fd37bf735169568fa17164`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:16:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bcb55460b2c2b07856962a4787935d0468bccb7c9dfa177433fa022f264f26`  
		Last Modified: Thu, 05 Sep 2024 00:24:55 GMT  
		Size: 184.6 MB (184553262 bytes)  
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
$ docker pull buildpack-deps@sha256:77880ab350ae8376ea67e1c07e6ec50225ed4adb050ec1ddf385028fd0eb9d0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351642567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c3b841cea75479af0775e87f568570666e00fa91f3eee2ba16f52a23e94e73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:13:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:14737c83f5b55bbada462ce86f67f71c256ff429e1c5b94a7f457569882993b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326003486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaa4c2efdc68becbf386c20c0a170c098a9f2d56689a5b569ffc816c1c143a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:54:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f8cb8fc9c5f50bae748d45f12febe8141263b15997a428733fa15f9121148d`  
		Last Modified: Wed, 04 Sep 2024 23:15:54 GMT  
		Size: 189.8 MB (189827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:16e9e53051615bb49ed45c50d26b19e6a3d624ad240d34c4787af1f52e2c160a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363138602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c01177f587771042c516c6f8cba97b8071fc9e9cc063bc3e87edc666e3e5bee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:03:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f161dd3959faa2f30fc05f50f11de2ff1ae36632b37e08822b40bdd9e596b6ad`  
		Last Modified: Wed, 04 Sep 2024 23:14:38 GMT  
		Size: 214.3 MB (214285993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22f500481e64f18d6090a9a5a37ce02943f8d5394252ad3cad48e8c4d32c1883
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001882b4a0aabecc2d9f853e96cadabde59f35f44ea56357deb7255d313c42d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18612060b30c9f1db538f5e79e46ea0534fafb1c79e714e74e11a1b56e69c56d`  
		Last Modified: Thu, 05 Sep 2024 00:00:45 GMT  
		Size: 183.3 MB (183289806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:3ce25ed8fe89738778796426084550ee9bc6f3da1081f73a271cf804b4cf9144
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
$ docker pull buildpack-deps@sha256:7391eeef017abf3dc7764528610e6334e284ff14f822b878ac2705e875ebd0f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70062429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab48ea956175da7a435b1258b74f1046ec646e218ef6b57ede31bdd4effcb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
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
$ docker pull buildpack-deps@sha256:85035f6dac04f641efde596e73116d0df38aa82798a45d89d6842315d499f58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8743c0a9eb82230d6f4ccd2ea96817b3753288a530312e5c8a8374b80904edb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
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
$ docker pull buildpack-deps@sha256:201b3d44b674e1ff8bac37b9b2064a502fef6557f821466253959ead71f332ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79264159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ef92d1203e95d5305ab675bfd01bba603da95ee5d9e91a5166014001e48ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d4640407bec198a10920cfe4f1e7c39f51d0f7347c498c1e7b4374ea57fa78b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71991388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d59091a65171d25d8f31d2f54baae3cf9a801ce554104397bc466fce40d284f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:b1a3fc06fef89bdb52574d1046a5a8e3fdc39fd710800bb42bc952eb38891fbc
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
$ docker pull buildpack-deps@sha256:f3a42de0dc2ce296f3b3b76ef08f7bdb77524a0a597fd1c044d54dd7341fedc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131589226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070a8135c422aaf7d325113dfcbc72baf6d75dff631f659fb2e1daed799e35ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
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
$ docker pull buildpack-deps@sha256:c2c1fed2fa16483d3c4c8c64cb0f011a7a6512676f9cb5fd21997e3767d0b983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141460953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e524eb07a1b6a66b919ec2c0f72b5ca9bcb6a0f68596051367ed1e10e3975c38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:88b5267bd9605330d451926120f1d6033450530ae93c784644161be024237557
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136176441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cfba6784ced9ecdf572656db14c53f8c6220edc2f9c6c15879796fdac5f1ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d36cb70e85bac41799ca9e2563b5d53a331f678c8103720bdffde2a95d1f6c02
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148852609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106eeee8b0ab29b3c4ed5ceeab253d274dffba6670ad6957882efadde371e1c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c5d375454de128aad302d578dc028cc0945b2a60f637c5eb10c3048e8aff1ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135142057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3655812cd43a04c6f0ef2bbc001576d9617038e288402e1f15b6b730b780e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:238091f7cb4da28f894378fd0514789579406b0faf5eeddc6125e48666baff8f
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
$ docker pull buildpack-deps@sha256:fdf6329ed7f5fc2d3dbe74551ea567f64e7dacbd334c0f211c7fd1e277f77568
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.9 MB (333924648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44324ec0f76769ebafb7cef9a5d659b920bf2a10b0283bc7e07d2ac566b57dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:23:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb49fd6c6abe4b97e2770778db3d0d8790983a911470063ea6b6447f70348bd`  
		Last Modified: Thu, 05 Sep 2024 00:27:27 GMT  
		Size: 63.7 MB (63693639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d0eb68a3ebcb7236aa556189ab47d468b1815b12e7e2f899be551726d4a00`  
		Last Modified: Thu, 05 Sep 2024 00:28:02 GMT  
		Size: 200.6 MB (200635962 bytes)  
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
$ docker pull buildpack-deps@sha256:8e8648210bc49492d668a7c4e942817fbd56f35a7c363e4ee33a3d72b1dc9376
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369943604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2ee2b2fb83d89b6ac68e8bf06d99cba0ab79c2b86b590e38e0f786f9ab994d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:19:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31201b79e8a36b69873f980c46439edb25ae4ac889b1ca464e88c6e9f0556b`  
		Last Modified: Wed, 04 Sep 2024 23:24:14 GMT  
		Size: 68.0 MB (68001606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a319ec9e956588ee40c4f304708b4df65cbd69e4e258d323fab4fd27daf252f9`  
		Last Modified: Wed, 04 Sep 2024 23:25:00 GMT  
		Size: 226.4 MB (226405323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:704b9254b09594d2270a955d0675e6c919c1d8dad1ec492483122e034d75a307
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343787137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7225b32c0c190167eedf5534f1dff2f94160057d2ea72af2ad5fe948cf9130`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:12:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4237e9699f2a42702bbc40ac84636b5bd5b697365781314fa4597f038af203a`  
		Last Modified: Wed, 04 Sep 2024 23:20:37 GMT  
		Size: 65.0 MB (64981816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708770bcaa0a7130dbf5fc08d4f61c4a9e74bd0b9cc8fad9ed65da73a11c090`  
		Last Modified: Wed, 04 Sep 2024 23:22:50 GMT  
		Size: 205.7 MB (205746221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4508ac46893254134703efd4d766acf691caf5c1c8e0f58cb2b96040fdcaf162
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.1 MB (376104803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ebb7b196ddb296a841acdb74c8651640f26049c7dae38ed466efe86d66225`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:12:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5ae18a02755729ef516bd9a7a6cd67d1c73f6b23e00562755d51d9940cb55`  
		Last Modified: Wed, 04 Sep 2024 23:17:19 GMT  
		Size: 71.6 MB (71558349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5930c2023cb34816d843618e8136f3505598fe344ee1e670ad00ed8cb7189a`  
		Last Modified: Wed, 04 Sep 2024 23:17:59 GMT  
		Size: 224.3 MB (224319161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:df0812d7254fa42dfc49d17f36aab2e90060c6d9d2373714649c1f65006e9cca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340560985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aa9fd018bb3186928cbf4f730e3e88db9c82cc6091dd1584aefab744c96e34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2f404abee9eb74c2b285e0671c0d9b756da381a2ffd30ac37149dd5f30055`  
		Last Modified: Thu, 05 Sep 2024 00:02:45 GMT  
		Size: 67.2 MB (67236355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b6d6a6deb87ef00986dcb6d773381c8bddcb18b5debcb57dab3e1ca8ba368`  
		Last Modified: Thu, 05 Sep 2024 00:03:13 GMT  
		Size: 199.0 MB (198974378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:2cec63b75abdda05f02cf7164cf6a05723a73b3f465128c992be7786a4d26638
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
$ docker pull buildpack-deps@sha256:27fd4cfcb18cd2d5384a22a33966913ee334dc7f49ae1c7971b013aa4d6fc8c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69595047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9aa623311f3d33935ec2c3686ead7d1eb6d7e91a9acf5f9d29f96717edff23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
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
$ docker pull buildpack-deps@sha256:962a2b0a55405632c1d31a9cdb722a85939ff23a88efcb3a64ea09282ffc137b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75536675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8d9c8231cda2fd80ea5a1192ea71afce46278e1172205d87fe873d2b38b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a428e09f67360bcc8fb1a124a8fb67610b370ae9e5635bd8e2e950cad7dfb376
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73059100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb1cb53973ae99c5f3918787f88a2be6b9c77abc4f83cb919ab2afc0f5b3a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:feb6cf26df3ed5cda70540b834dde7d99fecfdb5ad2f2d05ae00be1599ad8efe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80227293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d130f96e42cfb572fbb725ebc678daae4713e3b142142a8005a9aabc9beb189f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5dadfc5dab20e01252c673073c5eac4ce3241af71cb7241006f50516e8e5cd4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71492476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82b0ab93f8da1cbebe40d02eb72e1b218f218b3fe86d8cd5595a4e1b5f27141`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:03 GMT
ADD file:3536049154c2250abe969642d7b35b085e3d25447b8953cc1e072b690a306aa1 in / 
# Wed, 04 Sep 2024 22:28:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:38a3e7af214e5e0705f0ceebc8bef13cf31414ef0eb3f3ad8a05574549c77869`  
		Last Modified: Wed, 04 Sep 2024 22:33:47 GMT  
		Size: 51.5 MB (51475526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1754edde6597959b526e1765798c2e5f144cdf29b0cc5a933959b572039f27`  
		Last Modified: Wed, 04 Sep 2024 23:14:26 GMT  
		Size: 20.0 MB (20016950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3520d5b2d703a9ba9f15254f21ff6f525a3a0a16285036d7f46f4c330118417f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74350252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771060c6aeb4dff7b191c35a90d8acbe858592929541822e77932f256839f159`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:a301076e1df1c96b4427461e3a39ec91e20661a28d6c19a49c2ff15f02c0d092
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
$ docker pull buildpack-deps@sha256:c26ddc4c6105e764a5248d22cf6f900eee502ae53901b70f39a99ab8f6d196c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133288686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6db14f1cbab18ee86e685f6c181f769a5c7d2621cc5e7efee7c52932370483`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb49fd6c6abe4b97e2770778db3d0d8790983a911470063ea6b6447f70348bd`  
		Last Modified: Thu, 05 Sep 2024 00:27:27 GMT  
		Size: 63.7 MB (63693639 bytes)  
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
$ docker pull buildpack-deps@sha256:9ed6debda33be9bc6eb5a0965313488921b22d2dedf39405ca0e9326c2c820b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143538281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb69280a0d7741571456231f040f27b6ef2372d1d0330d98ba37622e6a5f37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31201b79e8a36b69873f980c46439edb25ae4ac889b1ca464e88c6e9f0556b`  
		Last Modified: Wed, 04 Sep 2024 23:24:14 GMT  
		Size: 68.0 MB (68001606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c28320a755b93d9e5ae7846728c1dff0f814dc225623d9e31e5a16d40c41a5ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138040916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b2c64297ad42b575c73f405afca220932f1bceb91a66cee45af8eb996fb49a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4237e9699f2a42702bbc40ac84636b5bd5b697365781314fa4597f038af203a`  
		Last Modified: Wed, 04 Sep 2024 23:20:37 GMT  
		Size: 65.0 MB (64981816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8d5c2ad72c939f4fc6456467a38ea5ad8f187a302f45ff1af6d9082afd903956
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151785642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c0d8ceb24ffe092c9396223b22c165d8cb22f1e4f56430240cc6dbbde92b4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5ae18a02755729ef516bd9a7a6cd67d1c73f6b23e00562755d51d9940cb55`  
		Last Modified: Wed, 04 Sep 2024 23:17:19 GMT  
		Size: 71.6 MB (71558349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b7eb09fe07e704734a745a05822f0f8e2732c5e45e0d3b80d48b67f59538d525
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141586607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235eb5b29f2107058a53cb218a44e0840d2007c68649dff771df685ddff74f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2f404abee9eb74c2b285e0671c0d9b756da381a2ffd30ac37149dd5f30055`  
		Last Modified: Thu, 05 Sep 2024 00:02:45 GMT  
		Size: 67.2 MB (67236355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:238091f7cb4da28f894378fd0514789579406b0faf5eeddc6125e48666baff8f
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
$ docker pull buildpack-deps@sha256:fdf6329ed7f5fc2d3dbe74551ea567f64e7dacbd334c0f211c7fd1e277f77568
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.9 MB (333924648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44324ec0f76769ebafb7cef9a5d659b920bf2a10b0283bc7e07d2ac566b57dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:23:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb49fd6c6abe4b97e2770778db3d0d8790983a911470063ea6b6447f70348bd`  
		Last Modified: Thu, 05 Sep 2024 00:27:27 GMT  
		Size: 63.7 MB (63693639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d0eb68a3ebcb7236aa556189ab47d468b1815b12e7e2f899be551726d4a00`  
		Last Modified: Thu, 05 Sep 2024 00:28:02 GMT  
		Size: 200.6 MB (200635962 bytes)  
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
$ docker pull buildpack-deps@sha256:8e8648210bc49492d668a7c4e942817fbd56f35a7c363e4ee33a3d72b1dc9376
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369943604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2ee2b2fb83d89b6ac68e8bf06d99cba0ab79c2b86b590e38e0f786f9ab994d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:19:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31201b79e8a36b69873f980c46439edb25ae4ac889b1ca464e88c6e9f0556b`  
		Last Modified: Wed, 04 Sep 2024 23:24:14 GMT  
		Size: 68.0 MB (68001606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a319ec9e956588ee40c4f304708b4df65cbd69e4e258d323fab4fd27daf252f9`  
		Last Modified: Wed, 04 Sep 2024 23:25:00 GMT  
		Size: 226.4 MB (226405323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:704b9254b09594d2270a955d0675e6c919c1d8dad1ec492483122e034d75a307
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343787137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7225b32c0c190167eedf5534f1dff2f94160057d2ea72af2ad5fe948cf9130`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:12:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4237e9699f2a42702bbc40ac84636b5bd5b697365781314fa4597f038af203a`  
		Last Modified: Wed, 04 Sep 2024 23:20:37 GMT  
		Size: 65.0 MB (64981816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708770bcaa0a7130dbf5fc08d4f61c4a9e74bd0b9cc8fad9ed65da73a11c090`  
		Last Modified: Wed, 04 Sep 2024 23:22:50 GMT  
		Size: 205.7 MB (205746221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4508ac46893254134703efd4d766acf691caf5c1c8e0f58cb2b96040fdcaf162
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.1 MB (376104803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ebb7b196ddb296a841acdb74c8651640f26049c7dae38ed466efe86d66225`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:12:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5ae18a02755729ef516bd9a7a6cd67d1c73f6b23e00562755d51d9940cb55`  
		Last Modified: Wed, 04 Sep 2024 23:17:19 GMT  
		Size: 71.6 MB (71558349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5930c2023cb34816d843618e8136f3505598fe344ee1e670ad00ed8cb7189a`  
		Last Modified: Wed, 04 Sep 2024 23:17:59 GMT  
		Size: 224.3 MB (224319161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:df0812d7254fa42dfc49d17f36aab2e90060c6d9d2373714649c1f65006e9cca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340560985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aa9fd018bb3186928cbf4f730e3e88db9c82cc6091dd1584aefab744c96e34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2f404abee9eb74c2b285e0671c0d9b756da381a2ffd30ac37149dd5f30055`  
		Last Modified: Thu, 05 Sep 2024 00:02:45 GMT  
		Size: 67.2 MB (67236355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b6d6a6deb87ef00986dcb6d773381c8bddcb18b5debcb57dab3e1ca8ba368`  
		Last Modified: Thu, 05 Sep 2024 00:03:13 GMT  
		Size: 199.0 MB (198974378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:2cec63b75abdda05f02cf7164cf6a05723a73b3f465128c992be7786a4d26638
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
$ docker pull buildpack-deps@sha256:27fd4cfcb18cd2d5384a22a33966913ee334dc7f49ae1c7971b013aa4d6fc8c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69595047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9aa623311f3d33935ec2c3686ead7d1eb6d7e91a9acf5f9d29f96717edff23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
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
$ docker pull buildpack-deps@sha256:962a2b0a55405632c1d31a9cdb722a85939ff23a88efcb3a64ea09282ffc137b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75536675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8d9c8231cda2fd80ea5a1192ea71afce46278e1172205d87fe873d2b38b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a428e09f67360bcc8fb1a124a8fb67610b370ae9e5635bd8e2e950cad7dfb376
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73059100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb1cb53973ae99c5f3918787f88a2be6b9c77abc4f83cb919ab2afc0f5b3a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:feb6cf26df3ed5cda70540b834dde7d99fecfdb5ad2f2d05ae00be1599ad8efe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80227293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d130f96e42cfb572fbb725ebc678daae4713e3b142142a8005a9aabc9beb189f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5dadfc5dab20e01252c673073c5eac4ce3241af71cb7241006f50516e8e5cd4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71492476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82b0ab93f8da1cbebe40d02eb72e1b218f218b3fe86d8cd5595a4e1b5f27141`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:03 GMT
ADD file:3536049154c2250abe969642d7b35b085e3d25447b8953cc1e072b690a306aa1 in / 
# Wed, 04 Sep 2024 22:28:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:38a3e7af214e5e0705f0ceebc8bef13cf31414ef0eb3f3ad8a05574549c77869`  
		Last Modified: Wed, 04 Sep 2024 22:33:47 GMT  
		Size: 51.5 MB (51475526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1754edde6597959b526e1765798c2e5f144cdf29b0cc5a933959b572039f27`  
		Last Modified: Wed, 04 Sep 2024 23:14:26 GMT  
		Size: 20.0 MB (20016950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3520d5b2d703a9ba9f15254f21ff6f525a3a0a16285036d7f46f4c330118417f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74350252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771060c6aeb4dff7b191c35a90d8acbe858592929541822e77932f256839f159`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:a301076e1df1c96b4427461e3a39ec91e20661a28d6c19a49c2ff15f02c0d092
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
$ docker pull buildpack-deps@sha256:c26ddc4c6105e764a5248d22cf6f900eee502ae53901b70f39a99ab8f6d196c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133288686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6db14f1cbab18ee86e685f6c181f769a5c7d2621cc5e7efee7c52932370483`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb49fd6c6abe4b97e2770778db3d0d8790983a911470063ea6b6447f70348bd`  
		Last Modified: Thu, 05 Sep 2024 00:27:27 GMT  
		Size: 63.7 MB (63693639 bytes)  
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
$ docker pull buildpack-deps@sha256:9ed6debda33be9bc6eb5a0965313488921b22d2dedf39405ca0e9326c2c820b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143538281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb69280a0d7741571456231f040f27b6ef2372d1d0330d98ba37622e6a5f37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31201b79e8a36b69873f980c46439edb25ae4ac889b1ca464e88c6e9f0556b`  
		Last Modified: Wed, 04 Sep 2024 23:24:14 GMT  
		Size: 68.0 MB (68001606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c28320a755b93d9e5ae7846728c1dff0f814dc225623d9e31e5a16d40c41a5ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138040916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b2c64297ad42b575c73f405afca220932f1bceb91a66cee45af8eb996fb49a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4237e9699f2a42702bbc40ac84636b5bd5b697365781314fa4597f038af203a`  
		Last Modified: Wed, 04 Sep 2024 23:20:37 GMT  
		Size: 65.0 MB (64981816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8d5c2ad72c939f4fc6456467a38ea5ad8f187a302f45ff1af6d9082afd903956
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151785642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c0d8ceb24ffe092c9396223b22c165d8cb22f1e4f56430240cc6dbbde92b4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5ae18a02755729ef516bd9a7a6cd67d1c73f6b23e00562755d51d9940cb55`  
		Last Modified: Wed, 04 Sep 2024 23:17:19 GMT  
		Size: 71.6 MB (71558349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b7eb09fe07e704734a745a05822f0f8e2732c5e45e0d3b80d48b67f59538d525
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141586607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235eb5b29f2107058a53cb218a44e0840d2007c68649dff771df685ddff74f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2f404abee9eb74c2b285e0671c0d9b756da381a2ffd30ac37149dd5f30055`  
		Last Modified: Thu, 05 Sep 2024 00:02:45 GMT  
		Size: 67.2 MB (67236355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:bce7026ee0d4977cb13db09d859cf3c91989e16ee592d706aa03149027263992
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
$ docker pull buildpack-deps@sha256:90d185e94b3b2422df15f2e48c0b23148b1e19a892d2a255582922f9b9da3aab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333078604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f5a8b4103d91cf8a90202fae2cdee515fe2d83d51f833f2bdedde32a517217`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:21:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ad08e7d81f82d9e2c4214b3dfd3cce995412f651a08e233d2f09274292773`  
		Last Modified: Thu, 05 Sep 2024 00:26:24 GMT  
		Size: 63.7 MB (63691738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5fab79030c3084031070777f64892494b2cfbdfcd9d756b6a1a41e4a9fd6f1`  
		Last Modified: Thu, 05 Sep 2024 00:26:59 GMT  
		Size: 199.8 MB (199782011 bytes)  
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
$ docker pull buildpack-deps@sha256:4673f0b332d7be287dc13776cfac704af7b54427d8191b4c79fdaac67b32916f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368982385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54773087e8cdcf8c20b2927ca0a1324e9a64c9c0942afa24fcb5ed6d6dd4187c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:17:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676697198fdfee6917623f8c11e9e2725eb0d2fed789bf0e71473beb1651938`  
		Last Modified: Wed, 04 Sep 2024 23:22:51 GMT  
		Size: 68.0 MB (67999768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a071913506a26883892b5bcd5b7e56e30953b90b4bd5c9873aa87a5a33c7123b`  
		Last Modified: Wed, 04 Sep 2024 23:23:37 GMT  
		Size: 225.4 MB (225420586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b7838b4742be13db1d1a747b0acf5a27f7300e2a7c2a4dc5b3709cb5a8f4196c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342005334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f975a1417b3a376323be716cf65328753ef7d8d12b092220d4009e4de25c133a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:04:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac59bc75368032a1aacc11229b927d620146529073e342e9762c4d3c1ff58a`  
		Last Modified: Wed, 04 Sep 2024 23:17:12 GMT  
		Size: 65.0 MB (64982310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec11c68501cca6c2a0da847df5b55346b4f95eafda376070044cc117256d6d4d`  
		Last Modified: Wed, 04 Sep 2024 23:19:25 GMT  
		Size: 204.1 MB (204055737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5e30158940f6b7ed0a121ceba4f482966a825bd751badb19501048704f50164a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (375002708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec97870a6751c6cdd32726095b334ffe32519c68d454d1121b1eabaef714b9b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:09:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af665d962e383e3f1c7578bf8044f6cd38edea60132aae6dd8346eb0999613`  
		Last Modified: Wed, 04 Sep 2024 23:16:11 GMT  
		Size: 71.6 MB (71560086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a471ab9eb3c8df7c43d4364f980d88818e686ad1e8291753a6b86a16af2d77`  
		Last Modified: Wed, 04 Sep 2024 23:16:49 GMT  
		Size: 223.2 MB (223197670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:17af248bfbe1e8ab33b0e561eb6c0ef3686f0cedd557e35c4853def42575cd35
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442888142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c77ba538f9adf10fd862946d1177b5d2576c85e90415beb3ccfb0210ae5248c`
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
# Wed, 04 Sep 2024 23:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
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
	-	`sha256:b1b8269d3170ea5e0ed9b1314bea3a8b5949e212597ca4322a5cda142d67f33c`  
		Last Modified: Wed, 04 Sep 2024 23:14:00 GMT  
		Size: 306.0 MB (305971552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7b5bf9e982fa414441d9f4f9bc06696fb736a2898adade59a400466eec4a5776
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339634143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc28a71caf77ff0ab634c85987af98a59537a6b888e308d0c8da41cd42dc90d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:55:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:56:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fcd27216accec74418e978fea2c6be2752504c8ece95ef0dde330d8a5c092`  
		Last Modified: Thu, 05 Sep 2024 00:01:55 GMT  
		Size: 67.2 MB (67237737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5bb45295cabf007391a31614c906096557565683b0b07fdc3669d2d0ac113f`  
		Last Modified: Thu, 05 Sep 2024 00:02:23 GMT  
		Size: 198.0 MB (198023251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:850df8bb4645b2c35d3ab90f736c6415740341d7b1e25033572ce155f65ecc17
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
$ docker pull buildpack-deps@sha256:5c540b1b211c1efaafb1b4b86625cbd3bd7ae78eee9e3d68baedb2c3d6e2cc92
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69604855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1719edcde9f4bf97ae44287bebcef3f99df21e3c51e3d0d3f8f52b25692d7fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
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
$ docker pull buildpack-deps@sha256:553289d7d0ee3d06a9ca4771be21b82945013086f84b3d7a00d555c96d35e2aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75562031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fceead42a36bd5b0bc8be1827ce8000f4a436742bcb4b732564008d97cfb5c51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0c117689692b057acc8213bf376b412eff1499b594d99c9fdeeb8b793b8dd873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72967287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e41b859b97c6e171049841788de1a97a82477edd39d6477efccc6dd4ad4862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3e558c0209496b0526329fc8de9a8a2da7fefc99f9845dfb7a89bccb1d169e03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80244952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598fe339fe78f27fb2edfcc0109e809d2b7097801eefffdeab4eca9b49503f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
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
$ docker pull buildpack-deps@sha256:be0244159e3edd884c06faaff6483525d4c78c30b4c3eabfbde5ba3ee43dd4f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74373155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59b4514ac5e5cc01c98d02d36641460165f05546ebae0e8319d9c9bea567ecb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:471bc4b421e9679c2d03de9b202d5ba13d8dc5bac58151b95cf1d9fe878736b5
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
$ docker pull buildpack-deps@sha256:6f214b53497b9eb190b57aedfa8795b3a2aabc115bdfb664c43d7ecde50ea22a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133296593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefba7a5e499120643c9f46e4fbf7d581c6cf2524d19e01a2df5b060c69e75e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ad08e7d81f82d9e2c4214b3dfd3cce995412f651a08e233d2f09274292773`  
		Last Modified: Thu, 05 Sep 2024 00:26:24 GMT  
		Size: 63.7 MB (63691738 bytes)  
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
$ docker pull buildpack-deps@sha256:aa2ecf738666a323f7e7d8c40adf61d1138d84212e4b23d6c39bbb7ea60a62bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143561799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e36838e7d0962b487fa77b20613101f2b9c894ccb77220e1de7af2b9eef4c0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676697198fdfee6917623f8c11e9e2725eb0d2fed789bf0e71473beb1651938`  
		Last Modified: Wed, 04 Sep 2024 23:22:51 GMT  
		Size: 68.0 MB (67999768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8af6d4267f7b2ae3a48c5178fc412b19cdb2a9bffd157640981b2c023643dd41
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137949597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3348df9b9deb7caa5c063fbbba211170c944cfb05d10a13b94ad8b67cbfab8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac59bc75368032a1aacc11229b927d620146529073e342e9762c4d3c1ff58a`  
		Last Modified: Wed, 04 Sep 2024 23:17:12 GMT  
		Size: 65.0 MB (64982310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e8aed150e2bfc5c50e50f61c2df8c049f4679922d12e85696155ceb7bbd643f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151805038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b8defb7b402fa6d091d061e89f4fb5739b404d875b4b71417e564957598438`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af665d962e383e3f1c7578bf8044f6cd38edea60132aae6dd8346eb0999613`  
		Last Modified: Wed, 04 Sep 2024 23:16:11 GMT  
		Size: 71.6 MB (71560086 bytes)  
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
$ docker pull buildpack-deps@sha256:1a7538359bf9f1b11be91b4bc365f4a674e73db7cf8b9a58e2a5678e3e7db3b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141610892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8dab2bdfd8e752900399d53743d189ceed42554ec901984badaf89e26a2bb3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:55:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fcd27216accec74418e978fea2c6be2752504c8ece95ef0dde330d8a5c092`  
		Last Modified: Thu, 05 Sep 2024 00:01:55 GMT  
		Size: 67.2 MB (67237737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
