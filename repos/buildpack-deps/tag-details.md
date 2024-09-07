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

## `buildpack-deps:24.10`

```console
$ docker pull buildpack-deps@sha256:4b37bafa009eab5c0a3458199633d3f1a98430feec8baed7e18a34a425e1e7d6
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
$ docker pull buildpack-deps@sha256:53a3af67688dca3357dc3c61750adf28f8538254864c06acb3896e346d69fd23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298126965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51675e700651d03dddab91d364cd70e1336f1991beadfb035c88b781a000539`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:26:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055335bda5b48b9b7f5bf248f1a6cda9c73710f1621ec8e7795dfa323f2e016d`  
		Last Modified: Sat, 07 Sep 2024 04:27:39 GMT  
		Size: 46.9 MB (46852775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee09a1f0595ea00a56bf60089efe3547f7c5b9e6ab94e3fec96f1d6ec2225dce`  
		Last Modified: Sat, 07 Sep 2024 04:28:12 GMT  
		Size: 201.9 MB (201893634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f5303ef2025d662e9f49e96d8f9a65496c6464611d6c26f02271de44cca99f03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258946084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbed6e56952a127479fa7e8f064c4286d6698794d76d534c349ec0cddc6e92b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:04:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff511081b01199e4b9bb12d45bce6d56e4cd79db917542973d713b209bc166e`  
		Last Modified: Sat, 07 Sep 2024 02:05:26 GMT  
		Size: 49.8 MB (49799754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cf6986399844487d0a4441f3c73bd0d75f4f01a51d238f23d20b323d9123ff`  
		Last Modified: Sat, 07 Sep 2024 02:05:57 GMT  
		Size: 164.8 MB (164763866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6e1914b35a42dc8a1e3d3c3c7b2e39ff7bd08fd344e441940ade2c25aba9741
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292039463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069aca49b11ddfab5419df6d0a322999fca568e6f3cb68fe4d5f48a9a806d9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:24:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024e10b71baa355a2df6e0d250585dc206f2c9ea54534441463dc57467b4b44`  
		Last Modified: Sat, 07 Sep 2024 04:25:59 GMT  
		Size: 46.8 MB (46802301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951062e5b2fd6d80a940e440cd74d8a39d9ff7b11defbf672b243f6fe4612d08`  
		Last Modified: Sat, 07 Sep 2024 04:26:26 GMT  
		Size: 195.9 MB (195906336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c9649827163d60b6e8a1f61b1252872e212351892e53bc2a01a277e0efabdc49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316117234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a5dddb4b63f18e6b6fec2cf320e166504a6d8fd6c2f4f975a9e8f89b14f0c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 05:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 06:05:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314fe13ab777163606b9145019d08931bba0381111e334bc7a164f67a035ed73`  
		Last Modified: Sat, 07 Sep 2024 06:06:31 GMT  
		Size: 52.2 MB (52185743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4c027cd6ebb8fffc10d99f831ea2742f2251c37b83d72e34dce5596fe5c50`  
		Last Modified: Sat, 07 Sep 2024 06:07:10 GMT  
		Size: 207.4 MB (207437906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0c0d381d66bfd394c176e6f0c85dcfb43adc87c7bd81ff11f00f99b100e686ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (390032694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0411807a6bb5da9d5a34e4c831c706725b4c75fcbe16a607bdb70e9ff6e7c59e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 14:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 14:33:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2241754e98cf7884cc7b38dc30666fa15dfe2c846239595a26f28fa0792b730c`  
		Last Modified: Sat, 07 Sep 2024 14:35:33 GMT  
		Size: 55.0 MB (54986722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3dcb618b590368c44a4e2831a7f18b4be80254abb77d58e8d83bcd5524130b`  
		Last Modified: Sat, 07 Sep 2024 14:41:09 GMT  
		Size: 284.1 MB (284056105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f013b5d281ec472e3bec9d5008e19e377beefacb2c9c6d60ebfd05630d5b6790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276051969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9215737453d0c0471a03c64c6bf94d12f7df48d6501e1531b132e45a0c0176f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:55:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008cf182f449632ffe2a4d63ef9fa22ab66fd95d2c395d89ba25703628dae55b`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 48.3 MB (48256989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91c618697b775b83b66d93e2814a7040b5e3340d5be35ed7c381a24ad9e448`  
		Last Modified: Sat, 07 Sep 2024 01:57:02 GMT  
		Size: 177.3 MB (177250883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-curl`

```console
$ docker pull buildpack-deps@sha256:bbe532c9fdb3d1ff64ab31461576e131a96fad25f7d8ea6bd3a064e38b826686
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
$ docker pull buildpack-deps@sha256:b2d10852a5a8b250588d8b3aa134e847ed89d71742af3b061ad87556089fe01b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49380556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba469658ee98def318f50852da532a47c0f9afd8968662dbbe2463724e577ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9446ee61f995f3dfc1fa728f233d2da1e5b24ff028ba8167889404204dae903f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44382464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a2f3f82859bdc8b1634c4aade93ae6077a54f750a95e27fc7fad3b4c49200f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e16dd7f2df32674bb26fcabbccdd1ccf59e55d9edd2c012c3237719aa906c11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49330826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ad42c1592da0f50a51ac84647eb333e07ccedc14104a52d63a2927c8738660`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ba80ab0b3f996f6fbb71e33d1334c69ab19a4fa8fcfe394326d235d7d3c08cf6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56493585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800ade7a21d3dff2b3db4ab70b9a99841ecf9079ea7767c88254303ce9809402`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8bae7a8936a258e09c7dbc700fba9509253561b417d46f360568eb7ce5cf2dd1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb7c2e96d5d09c84c81980bacf3e84aeb009013a6a49e807a620bd0f9b6ded8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2fcf7b518d8c311ccc0e0622d08cb0e97d47626ef630f5234913688c7bd5bdcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50544097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6014a89ccf41a15552b52943eeaf557fbde2b8420cf3c6aa990c1d72fe143f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-scm`

```console
$ docker pull buildpack-deps@sha256:b9d425635b55508007dfba534c2f299d9210a784d2a06029ad2f6665c77570ea
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
$ docker pull buildpack-deps@sha256:bb1bae1c72b9e6e3c837c88439483deb57fb23e29b13af78dc5cac9d527570c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96233331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2084689826f3194265f0ecfd05f9d226214ded5e01b985238a0bfb341692b67b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055335bda5b48b9b7f5bf248f1a6cda9c73710f1621ec8e7795dfa323f2e016d`  
		Last Modified: Sat, 07 Sep 2024 04:27:39 GMT  
		Size: 46.9 MB (46852775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e8115839661ba0860f523aa5dc52f0996d50bcb66b7dac2426d3751c1e707d8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94182218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f4879bc17f4cedf51f9ea3f3d7f92f600b6ea5c8b1a4fd668ed36f0e115c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff511081b01199e4b9bb12d45bce6d56e4cd79db917542973d713b209bc166e`  
		Last Modified: Sat, 07 Sep 2024 02:05:26 GMT  
		Size: 49.8 MB (49799754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:94264f92b0f40c54d2d0121c7e8282be78c7206938df364c29001ce97906a396
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96133127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d209bc091e3256b3bff604f86e7403d54ecb16f4b2fa2b7ad38897c19c0b6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024e10b71baa355a2df6e0d250585dc206f2c9ea54534441463dc57467b4b44`  
		Last Modified: Sat, 07 Sep 2024 04:25:59 GMT  
		Size: 46.8 MB (46802301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0ab6aee778a6a3ecd0d0931b815693deb97a5e19b885144f7405af59d2e8772d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108679328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e587be00d51681002fe607e3dfa916b65cf4bc7d51c3cc9107b561ac69a345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 05:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314fe13ab777163606b9145019d08931bba0381111e334bc7a164f67a035ed73`  
		Last Modified: Sat, 07 Sep 2024 06:06:31 GMT  
		Size: 52.2 MB (52185743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:35613709acc4ea8bcfcfa6d711b2271dff5b9e120bb8c0b6c6dac2f8c34db151
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105976589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419577b50cc157b961183f2aaabbfe0f6b7a081e371798751ed9b9e2c1e3f3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 14:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2241754e98cf7884cc7b38dc30666fa15dfe2c846239595a26f28fa0792b730c`  
		Last Modified: Sat, 07 Sep 2024 14:35:33 GMT  
		Size: 55.0 MB (54986722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2545f66cce61aa3a51ae66a8bcaafadbb8ee5d314962d0685d527fc728e0789e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98801086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d9ba9e6a60f35a439d147379eedbda2b8b7b38e0e792c52f8935c0ea6277f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008cf182f449632ffe2a4d63ef9fa22ab66fd95d2c395d89ba25703628dae55b`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 48.3 MB (48256989 bytes)  
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
$ docker pull buildpack-deps@sha256:4b37bafa009eab5c0a3458199633d3f1a98430feec8baed7e18a34a425e1e7d6
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
$ docker pull buildpack-deps@sha256:53a3af67688dca3357dc3c61750adf28f8538254864c06acb3896e346d69fd23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298126965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51675e700651d03dddab91d364cd70e1336f1991beadfb035c88b781a000539`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:26:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055335bda5b48b9b7f5bf248f1a6cda9c73710f1621ec8e7795dfa323f2e016d`  
		Last Modified: Sat, 07 Sep 2024 04:27:39 GMT  
		Size: 46.9 MB (46852775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee09a1f0595ea00a56bf60089efe3547f7c5b9e6ab94e3fec96f1d6ec2225dce`  
		Last Modified: Sat, 07 Sep 2024 04:28:12 GMT  
		Size: 201.9 MB (201893634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f5303ef2025d662e9f49e96d8f9a65496c6464611d6c26f02271de44cca99f03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258946084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbed6e56952a127479fa7e8f064c4286d6698794d76d534c349ec0cddc6e92b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:04:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff511081b01199e4b9bb12d45bce6d56e4cd79db917542973d713b209bc166e`  
		Last Modified: Sat, 07 Sep 2024 02:05:26 GMT  
		Size: 49.8 MB (49799754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cf6986399844487d0a4441f3c73bd0d75f4f01a51d238f23d20b323d9123ff`  
		Last Modified: Sat, 07 Sep 2024 02:05:57 GMT  
		Size: 164.8 MB (164763866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6e1914b35a42dc8a1e3d3c3c7b2e39ff7bd08fd344e441940ade2c25aba9741
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292039463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069aca49b11ddfab5419df6d0a322999fca568e6f3cb68fe4d5f48a9a806d9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:24:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024e10b71baa355a2df6e0d250585dc206f2c9ea54534441463dc57467b4b44`  
		Last Modified: Sat, 07 Sep 2024 04:25:59 GMT  
		Size: 46.8 MB (46802301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951062e5b2fd6d80a940e440cd74d8a39d9ff7b11defbf672b243f6fe4612d08`  
		Last Modified: Sat, 07 Sep 2024 04:26:26 GMT  
		Size: 195.9 MB (195906336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c9649827163d60b6e8a1f61b1252872e212351892e53bc2a01a277e0efabdc49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316117234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a5dddb4b63f18e6b6fec2cf320e166504a6d8fd6c2f4f975a9e8f89b14f0c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 05:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 06:05:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314fe13ab777163606b9145019d08931bba0381111e334bc7a164f67a035ed73`  
		Last Modified: Sat, 07 Sep 2024 06:06:31 GMT  
		Size: 52.2 MB (52185743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4c027cd6ebb8fffc10d99f831ea2742f2251c37b83d72e34dce5596fe5c50`  
		Last Modified: Sat, 07 Sep 2024 06:07:10 GMT  
		Size: 207.4 MB (207437906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0c0d381d66bfd394c176e6f0c85dcfb43adc87c7bd81ff11f00f99b100e686ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (390032694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0411807a6bb5da9d5a34e4c831c706725b4c75fcbe16a607bdb70e9ff6e7c59e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 14:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 14:33:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2241754e98cf7884cc7b38dc30666fa15dfe2c846239595a26f28fa0792b730c`  
		Last Modified: Sat, 07 Sep 2024 14:35:33 GMT  
		Size: 55.0 MB (54986722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3dcb618b590368c44a4e2831a7f18b4be80254abb77d58e8d83bcd5524130b`  
		Last Modified: Sat, 07 Sep 2024 14:41:09 GMT  
		Size: 284.1 MB (284056105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f013b5d281ec472e3bec9d5008e19e377beefacb2c9c6d60ebfd05630d5b6790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276051969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9215737453d0c0471a03c64c6bf94d12f7df48d6501e1531b132e45a0c0176f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:55:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008cf182f449632ffe2a4d63ef9fa22ab66fd95d2c395d89ba25703628dae55b`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 48.3 MB (48256989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91c618697b775b83b66d93e2814a7040b5e3340d5be35ed7c381a24ad9e448`  
		Last Modified: Sat, 07 Sep 2024 01:57:02 GMT  
		Size: 177.3 MB (177250883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:bbe532c9fdb3d1ff64ab31461576e131a96fad25f7d8ea6bd3a064e38b826686
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
$ docker pull buildpack-deps@sha256:b2d10852a5a8b250588d8b3aa134e847ed89d71742af3b061ad87556089fe01b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49380556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba469658ee98def318f50852da532a47c0f9afd8968662dbbe2463724e577ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9446ee61f995f3dfc1fa728f233d2da1e5b24ff028ba8167889404204dae903f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44382464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a2f3f82859bdc8b1634c4aade93ae6077a54f750a95e27fc7fad3b4c49200f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e16dd7f2df32674bb26fcabbccdd1ccf59e55d9edd2c012c3237719aa906c11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49330826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ad42c1592da0f50a51ac84647eb333e07ccedc14104a52d63a2927c8738660`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ba80ab0b3f996f6fbb71e33d1334c69ab19a4fa8fcfe394326d235d7d3c08cf6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56493585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800ade7a21d3dff2b3db4ab70b9a99841ecf9079ea7767c88254303ce9809402`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8bae7a8936a258e09c7dbc700fba9509253561b417d46f360568eb7ce5cf2dd1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb7c2e96d5d09c84c81980bacf3e84aeb009013a6a49e807a620bd0f9b6ded8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2fcf7b518d8c311ccc0e0622d08cb0e97d47626ef630f5234913688c7bd5bdcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50544097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6014a89ccf41a15552b52943eeaf557fbde2b8420cf3c6aa990c1d72fe143f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:b9d425635b55508007dfba534c2f299d9210a784d2a06029ad2f6665c77570ea
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
$ docker pull buildpack-deps@sha256:bb1bae1c72b9e6e3c837c88439483deb57fb23e29b13af78dc5cac9d527570c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96233331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2084689826f3194265f0ecfd05f9d226214ded5e01b985238a0bfb341692b67b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055335bda5b48b9b7f5bf248f1a6cda9c73710f1621ec8e7795dfa323f2e016d`  
		Last Modified: Sat, 07 Sep 2024 04:27:39 GMT  
		Size: 46.9 MB (46852775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e8115839661ba0860f523aa5dc52f0996d50bcb66b7dac2426d3751c1e707d8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94182218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f4879bc17f4cedf51f9ea3f3d7f92f600b6ea5c8b1a4fd668ed36f0e115c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff511081b01199e4b9bb12d45bce6d56e4cd79db917542973d713b209bc166e`  
		Last Modified: Sat, 07 Sep 2024 02:05:26 GMT  
		Size: 49.8 MB (49799754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:94264f92b0f40c54d2d0121c7e8282be78c7206938df364c29001ce97906a396
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96133127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d209bc091e3256b3bff604f86e7403d54ecb16f4b2fa2b7ad38897c19c0b6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024e10b71baa355a2df6e0d250585dc206f2c9ea54534441463dc57467b4b44`  
		Last Modified: Sat, 07 Sep 2024 04:25:59 GMT  
		Size: 46.8 MB (46802301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0ab6aee778a6a3ecd0d0931b815693deb97a5e19b885144f7405af59d2e8772d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108679328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e587be00d51681002fe607e3dfa916b65cf4bc7d51c3cc9107b561ac69a345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 05:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314fe13ab777163606b9145019d08931bba0381111e334bc7a164f67a035ed73`  
		Last Modified: Sat, 07 Sep 2024 06:06:31 GMT  
		Size: 52.2 MB (52185743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:35613709acc4ea8bcfcfa6d711b2271dff5b9e120bb8c0b6c6dac2f8c34db151
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105976589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419577b50cc157b961183f2aaabbfe0f6b7a081e371798751ed9b9e2c1e3f3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 14:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2241754e98cf7884cc7b38dc30666fa15dfe2c846239595a26f28fa0792b730c`  
		Last Modified: Sat, 07 Sep 2024 14:35:33 GMT  
		Size: 55.0 MB (54986722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2545f66cce61aa3a51ae66a8bcaafadbb8ee5d314962d0685d527fc728e0789e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98801086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d9ba9e6a60f35a439d147379eedbda2b8b7b38e0e792c52f8935c0ea6277f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008cf182f449632ffe2a4d63ef9fa22ab66fd95d2c395d89ba25703628dae55b`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 48.3 MB (48256989 bytes)  
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
