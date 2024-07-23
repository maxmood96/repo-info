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
$ docker pull buildpack-deps@sha256:4917acbdddf57839e4c0b24d27d35ecbefcc092f41b21239f0dbeac4f127a846
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
$ docker pull buildpack-deps@sha256:ba010e8fb935edf3da510e4aea79b5d7bc2d5dd111469d976b0dddbe7608ea42
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245780758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9f9c7022ab7dc85725e96dc9826990fb316d39179a85978b344aeeedd38626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:33:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0b693a55ba8f2f62faf455314042339a92e3d947e131e8a5a9f4763a1be17`  
		Last Modified: Wed, 05 Jun 2024 04:47:16 GMT  
		Size: 11.1 MB (11131677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06da50534abdbd308d398fccbe7e605e7f760e1b302bc5e8c93058a0cc623057`  
		Last Modified: Wed, 05 Jun 2024 04:47:32 GMT  
		Size: 60.9 MB (60904546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c4ebd31b8500a7712d1ae95d94414f30f7d631d78273bca63023061288005f`  
		Last Modified: Wed, 05 Jun 2024 04:47:59 GMT  
		Size: 145.2 MB (145160312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a23f2782fc97e8fe46e3f205e0e321b503d8cdcc742c531649d045296c8bbd24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212061023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116400feeaca1f1a55f3db77c993044d3f25a50ab4e0ee4854d812d58220321a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:36:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054f0865ad2a3115262baff79f0f568e9aca8177cf21e36926e786435734f85`  
		Last Modified: Wed, 05 Jun 2024 03:51:48 GMT  
		Size: 9.6 MB (9605337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e7c4e1d26ef933f7ebbf4e7360073197b166ada1ffef28e0a0fc7eed78f1c`  
		Last Modified: Wed, 05 Jun 2024 03:52:06 GMT  
		Size: 55.9 MB (55878345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2c9e45258c5090b9e1484a8b0970c5bff6261cb1e7cd3218713c001827885`  
		Last Modified: Wed, 05 Jun 2024 03:52:31 GMT  
		Size: 122.0 MB (121973520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:305862bddac325eca5677b4fcac1ece055411d7befbbe2e507d43e86c3435860
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236070178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45de648bc3af4cb828dd7e8e0b36679adbb36c02b77e4362ce1526103b3daabb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:16:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4413e6a295aaaf041c65afd5671da95530820e6794dc6794636779b453a113e0`  
		Last Modified: Wed, 05 Jun 2024 04:34:11 GMT  
		Size: 11.0 MB (10982267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f58de85ef18320037487fd40921c0911a92f3ec25aae271afde8c56a8bb4e`  
		Last Modified: Wed, 05 Jun 2024 04:34:26 GMT  
		Size: 61.0 MB (61048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c73a257ae5bd83fd91d91c82db58648a6e0fcbcd585d8c196e275ecaa2bd20d`  
		Last Modified: Wed, 05 Jun 2024 04:34:48 GMT  
		Size: 136.8 MB (136834570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a318e4bb6bd67f9bc99e8d13d86edec736680c6b3a56a4cef8ba24599e86284e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269548339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b768226a4fdb4a30fb5cb279e11f6ebbd9f6925dcd028d103ca3558ce6c46c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:26:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a754598d82cd0c4fa1bfb084eefb9b3546c06014e24ca2fe14744cd7a8cfc6c`  
		Last Modified: Wed, 05 Jun 2024 03:47:02 GMT  
		Size: 12.9 MB (12940693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25fcea00df150e7a968dcaec967242a0ede82c633184af93a23b2aa72ef279`  
		Last Modified: Wed, 05 Jun 2024 03:47:26 GMT  
		Size: 69.7 MB (69653712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba1fdfbd84911122cb9e50d5a5c7c470af1cd2b1a763b0032cb81022b8d5545`  
		Last Modified: Wed, 05 Jun 2024 03:47:58 GMT  
		Size: 153.6 MB (153637814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1eefab6d67f98518179c8875573265b781a9d6325d3d060c6ae6666d619580db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226586223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b77468d7463e0bee053cac5bc2dd61782f52a88dbebb677fbe86ead433af96f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc882b1d2007230b7ab89a9d35944234befc417c5e38abec94ad4318f2b6421`  
		Last Modified: Wed, 05 Jun 2024 03:34:51 GMT  
		Size: 10.7 MB (10689958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78260c3c16760a1f95b5fb979620b45c7b2c5950d3c13b9cf8081e756194188d`  
		Last Modified: Wed, 05 Jun 2024 03:35:05 GMT  
		Size: 60.3 MB (60326843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e875c0f87834713797b2b228fd805bcfd69354b86e0309792cb236c9681887bf`  
		Last Modified: Wed, 05 Jun 2024 03:35:29 GMT  
		Size: 128.6 MB (128556004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:d2804bd67516754f7de978473764961c38399b6e1b48957312575cf7a7e4189e
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
$ docker pull buildpack-deps@sha256:6927690522f55e0fd3f47eb6cdefb512566ce3a5751b56a686320305c5bb8c52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1e577e5af8c42784c2dc438e51fa644b8b201e9ce12bfd90f944a4b69ec99e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0b693a55ba8f2f62faf455314042339a92e3d947e131e8a5a9f4763a1be17`  
		Last Modified: Wed, 05 Jun 2024 04:47:16 GMT  
		Size: 11.1 MB (11131677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:544358616bfab643d93a6adea54f434006a1f880b9ecf9af77ad6dd734a85539
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a21e0887b03608386457aa7a4559be214c9768dae621788490faee42d0e7139`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054f0865ad2a3115262baff79f0f568e9aca8177cf21e36926e786435734f85`  
		Last Modified: Wed, 05 Jun 2024 03:51:48 GMT  
		Size: 9.6 MB (9605337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a490e591096a5ffdd0f340b850a6b17398f0c301ffb1da3c2d362d3449de617
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44eda57b7725c60dfae1152e43b88e5c0d15300f75d21dff6fe54cd9048f0d34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4413e6a295aaaf041c65afd5671da95530820e6794dc6794636779b453a113e0`  
		Last Modified: Wed, 05 Jun 2024 04:34:11 GMT  
		Size: 11.0 MB (10982267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7997b415e34aa9822233a3b764d3d0e738cb674da245f3f68a70b13384920812
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46256813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25c58cea52f14836a13e1fc4f8aa38485d327ee8a137a1fc054166a8e1c2f84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a754598d82cd0c4fa1bfb084eefb9b3546c06014e24ca2fe14744cd7a8cfc6c`  
		Last Modified: Wed, 05 Jun 2024 03:47:02 GMT  
		Size: 12.9 MB (12940693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c9ca6b8549544f386947559ac95988cfd53bd56c4fbc9bf0c78703aca1b23a7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37703376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4252506b2904a0edad3f1a8836dc34ad01b2c2f61c806390b402b30925b8cd76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc882b1d2007230b7ab89a9d35944234befc417c5e38abec94ad4318f2b6421`  
		Last Modified: Wed, 05 Jun 2024 03:34:51 GMT  
		Size: 10.7 MB (10689958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:0e1b4b264fd8894d4dd737514d939d13316ec953da2b4e0c8d1270f17ed6575c
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
$ docker pull buildpack-deps@sha256:42fa8b21b4cf1931817ef1f947b9b036db2be147476904e9cdc8a8607a193ab5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100620446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7440898ca26905d7fbf4c58765072d2a7e7e26b211cf27cf067bbde28eecf8f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0b693a55ba8f2f62faf455314042339a92e3d947e131e8a5a9f4763a1be17`  
		Last Modified: Wed, 05 Jun 2024 04:47:16 GMT  
		Size: 11.1 MB (11131677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06da50534abdbd308d398fccbe7e605e7f760e1b302bc5e8c93058a0cc623057`  
		Last Modified: Wed, 05 Jun 2024 04:47:32 GMT  
		Size: 60.9 MB (60904546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:844adfbc56b1fd950f0ca8ed779aff9f7bb902b5d87da154aa145dc66799fc80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90087503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54efd6a8865a571dfdbcbb46c5bcfb6b1c889bde6d4e70054e803929f7d389`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054f0865ad2a3115262baff79f0f568e9aca8177cf21e36926e786435734f85`  
		Last Modified: Wed, 05 Jun 2024 03:51:48 GMT  
		Size: 9.6 MB (9605337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e7c4e1d26ef933f7ebbf4e7360073197b166ada1ffef28e0a0fc7eed78f1c`  
		Last Modified: Wed, 05 Jun 2024 03:52:06 GMT  
		Size: 55.9 MB (55878345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d3a5f4a3f845783df4f54f85b874ff01179ffe3d95070a493d3fd714d708538d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99235608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290f83f01f5cb4fae9145262b114d04bef79bab5b0f3823c71c1e8f6a36b73ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4413e6a295aaaf041c65afd5671da95530820e6794dc6794636779b453a113e0`  
		Last Modified: Wed, 05 Jun 2024 04:34:11 GMT  
		Size: 11.0 MB (10982267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f58de85ef18320037487fd40921c0911a92f3ec25aae271afde8c56a8bb4e`  
		Last Modified: Wed, 05 Jun 2024 04:34:26 GMT  
		Size: 61.0 MB (61048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cc4c735cd16433b98003cbda97b3c6477eceade9d30508271126b2cde85a498d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115910525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886f669f80c106b2b436c8eb04e0af813278dcf355cb13888e7bfd5c9adea39b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a754598d82cd0c4fa1bfb084eefb9b3546c06014e24ca2fe14744cd7a8cfc6c`  
		Last Modified: Wed, 05 Jun 2024 03:47:02 GMT  
		Size: 12.9 MB (12940693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25fcea00df150e7a968dcaec967242a0ede82c633184af93a23b2aa72ef279`  
		Last Modified: Wed, 05 Jun 2024 03:47:26 GMT  
		Size: 69.7 MB (69653712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2715f87961d0874f18198a6d70d0db6d875cfdb2465e0feb38def26ddd8c503e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98030219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b51504aa2dd127e70170ba14f268aa5c30456e27e07cfd7d8140bc833e7c06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc882b1d2007230b7ab89a9d35944234befc417c5e38abec94ad4318f2b6421`  
		Last Modified: Wed, 05 Jun 2024 03:34:51 GMT  
		Size: 10.7 MB (10689958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78260c3c16760a1f95b5fb979620b45c7b2c5950d3c13b9cf8081e756194188d`  
		Last Modified: Wed, 05 Jun 2024 03:35:05 GMT  
		Size: 60.3 MB (60326843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:b64e26f7623add790c8a6ce03f037eb1460781b5d32306d7ce6a91d217a2f602
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
$ docker pull buildpack-deps@sha256:c9f18dbc064cb00add6f56d99c0ccee39e58613773fbc172699bd4ee329c76be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250100638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4b7a675592556f99e88b4251ead06d069e3a498b4d310ceede2e0044cfc78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:59:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966d1a9d7dc827a9dda799795c07c44b594a52122c0b1c90242bab120d580c8`  
		Last Modified: Tue, 02 Jul 2024 02:04:36 GMT  
		Size: 39.5 MB (39454836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92a2766b622bfa17b0f88039006043d2679278f6b9b0af753fe338799989c2d`  
		Last Modified: Tue, 02 Jul 2024 02:05:05 GMT  
		Size: 173.1 MB (173114486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7436788773aee27b47b1a19a321dfd08518f0ee99d3d7b74c3ed05677c42b5ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217355681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0411dd00519e96e92a315428e1c9df69bba263d0d66d84234e47c0001e1226a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19939d362c9742ec7a32f61568520eb8438dc48cbc1335ffd7fa62bf170ceb4`  
		Last Modified: Tue, 02 Jul 2024 01:43:51 GMT  
		Size: 42.2 MB (42243066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdb9d48df11dcb10a55429ed8faecc54ee6b181eaa7468edf44aa87d620423`  
		Last Modified: Tue, 02 Jul 2024 01:44:23 GMT  
		Size: 140.6 MB (140586490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30aedfb24e94c3d840d5f5da9644e37b59a6067882721f954fb7df6abaa74114
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241407221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dde0b121101a91283781bae0ba338f3f71c7c26e2932449f91889dde1444222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:00:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aac2765dc6695d0f69e7852783ff14ecb83d04db68edc06347651928706052`  
		Last Modified: Tue, 02 Jul 2024 04:05:26 GMT  
		Size: 39.4 MB (39378111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686de3b37c2fe2d4b0e553fb3424ba1a1d18540b69904318345c4bfb40cea4e`  
		Last Modified: Tue, 02 Jul 2024 04:05:50 GMT  
		Size: 166.6 MB (166594707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0c9760fe788d9a2ed38a47db502dec216c552f7bff1f0caa5fb21e56fca30089
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271199025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207e8270610c8fa214e29f960e5e11bcdf9ada1795f14076732aecdd7c2dacf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:58:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:03:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82dc8e44a33d0f6fbe0c131eeb8268e1997857f2a63a77b883c6c1e387f308f`  
		Last Modified: Tue, 02 Jul 2024 02:09:30 GMT  
		Size: 43.8 MB (43765840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55636e60f9b3d7c2476012046397c3971c113c7813a4e788ee8e7ffc35a0589`  
		Last Modified: Tue, 02 Jul 2024 02:10:05 GMT  
		Size: 183.7 MB (183654409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:908b950080e80f068a5cd141b29e1cbc0a9b2ccbb3de3a9a3c22c0fa61d39885
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223830002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588eb12b48e4275a58886b6c9420f240d34d3f67190050a6fe73487fab8e03d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:43:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693aac14b0c492b501054836b25b7b1ce8545575960bb0ddd3c31b6bab5bf990`  
		Last Modified: Tue, 02 Jul 2024 03:48:05 GMT  
		Size: 39.4 MB (39420301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff72f078d5786a1145e8ba3fde463cee759a8cb800d930db19c82c562d69034`  
		Last Modified: Tue, 02 Jul 2024 03:48:28 GMT  
		Size: 148.8 MB (148768969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:d9695055e7e1a2582e6edc6a7a05cf7eba229ae0c4dbca24e2ebd58435993ecc
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
$ docker pull buildpack-deps@sha256:0544f948f0e350e0ffa71d159a741fa825bed92a575c1053b56ac45e9113177d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37531316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829a7f0ca64e1b4d275e10ab9b8a41357f0687de6b98b2bdfec2739eea5440a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:399c68581bdccc333843c661f9fe00a428848dc215eebdf801629d1c83f44eb6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34526125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c8e69939a6a1bb863ab0ffccb82e74e155e1a806793cdd17a8d7e285ddde6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13034def1ecea1c8eacfecc9509483aafed50615c56fbfd06b37bfec2984b99a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35434403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc4f871a468e94581d5299c4323c1c5a91cd3302b124e984159269b7812dd18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9ea311b77103ba1d8620c87a44dd42680745126c7d3c72c1edbc535834bdf3ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43778776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50574c983273271b7aea34ce7e841ba3f4b6635c7fe1a38502f1bc4fd9071c63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5fdc9ee3bd4ef0529decc62d532e385768cd9ab7ba9597c418237a72298c19f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35640732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9935af9770bdb0a8bf700e8236379bfc9508df5fe28b253cc26d4ab9224dcc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:19bc4f95f87bb2f0975c5f1090b6a565022a1f890e19af055e3e4f0d701af074
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
$ docker pull buildpack-deps@sha256:5d9cb6dcd1cd3180bf36be7ce1fd0201ff08d3a2e81d30ffe7315220545f6d70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76986152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4a1ee970e379a731f912d64cc05bb22e84dae7cf91b51acc2d8790d824a2a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966d1a9d7dc827a9dda799795c07c44b594a52122c0b1c90242bab120d580c8`  
		Last Modified: Tue, 02 Jul 2024 02:04:36 GMT  
		Size: 39.5 MB (39454836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f82d4287805b367c95ad99bf810f131a7294023636c1db0f7f7e254a1db9fcba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76769191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132a36536fec47518fa8472beebbe070410f5a78ffbf2eac862b0670f3567f9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19939d362c9742ec7a32f61568520eb8438dc48cbc1335ffd7fa62bf170ceb4`  
		Last Modified: Tue, 02 Jul 2024 01:43:51 GMT  
		Size: 42.2 MB (42243066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:55fb4b90a5186d3029858ed5fb1e52fe778753ff241fc82ae91e64d794a2652c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74812514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628d80babb0f665e8b36e0039db96d6c42479562b28379fa8b430ab025a687c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aac2765dc6695d0f69e7852783ff14ecb83d04db68edc06347651928706052`  
		Last Modified: Tue, 02 Jul 2024 04:05:26 GMT  
		Size: 39.4 MB (39378111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8161f7c68935700123953ccf08bcec8ca4cddc7e431090a883b879c44eda157d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87544616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fbdf7b7eb43e810daf796858cfbdbb7267bbb2d358c2ea24f9556a300c3c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:58:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82dc8e44a33d0f6fbe0c131eeb8268e1997857f2a63a77b883c6c1e387f308f`  
		Last Modified: Tue, 02 Jul 2024 02:09:30 GMT  
		Size: 43.8 MB (43765840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4a9437676ab21da7b3ad03457706ea309e2494fe018e775af025e81eb288d464
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75061033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473e03988f89693816397ff7caa90aa86fe7f6fb6879e6e98362da2abe59e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693aac14b0c492b501054836b25b7b1ce8545575960bb0ddd3c31b6bab5bf990`  
		Last Modified: Tue, 02 Jul 2024 03:48:05 GMT  
		Size: 39.4 MB (39420301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:001fbeb72df6623ac6f5c8f4fed31907b3d5ea2d6f8598216dd1872954942f6e
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
$ docker pull buildpack-deps@sha256:3558c964bf569f730093af41bf7496ec8d4cbb6e69653e6fda835ebed85309b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279729175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82247edddad280d6499bfa94389367908da72e47f5cbd48cc6b83cc0d20ada62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:13:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72ee9d28d3323b69c1e98217df15ce99add4d7029330c19edf34afb08d0f6ec`  
		Last Modified: Mon, 17 Jun 2024 23:14:33 GMT  
		Size: 45.5 MB (45471909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4b0288e2a65f9614fc7da6a77af34c15de35b61856448bcd3ca1a93e04db1f`  
		Last Modified: Mon, 17 Jun 2024 23:15:05 GMT  
		Size: 190.1 MB (190080547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:285c1b047419cf6a8071afc484727c1205c15a326e8704ecaba9ad4f044b2640
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239985378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be4225e767be58ed197589ddc16270b3accfec747bdbe1efb5da62e7d7e3d68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:17:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:21:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3d83d18813ec3c59260e725e09e29242f2cc5cf4e44e224657d25db8a16c3`  
		Last Modified: Mon, 17 Jun 2024 23:23:08 GMT  
		Size: 49.0 MB (49013037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761541af846f1634fcac3c55a1f928683a08646e68dd952f7001446a3dafabb`  
		Last Modified: Mon, 17 Jun 2024 23:23:38 GMT  
		Size: 150.5 MB (150516670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1315d2b678fc049a83e52615f97cae207a5b4093c86c215f47592d40c127e851
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270824823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b448c66459f3c077e3bdb7a327170ca53a59e4d8c1b39ddf8ae18f4df231b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:22:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609a6ad39dd54642e8c65403c8463121f544eaa46734a9398e92504cfc9b58b`  
		Last Modified: Mon, 17 Jun 2024 23:24:00 GMT  
		Size: 45.4 MB (45430148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fecb27a7a128ed30affce580f6ec163cd82f77778d337689b1c0f4a642d2ac`  
		Last Modified: Mon, 17 Jun 2024 23:24:25 GMT  
		Size: 182.0 MB (182039729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:45adc8dab7a8c195f39152c2764e82265084d5984a856be8097b57d3413cfa0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299073652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad2c98f93ba002f7a25b19376160c8f429f84483c3eb36be011a46bde6e8fcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:35:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 22:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 22:44:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680834b8998d6424161f149fd8d3eede4f74a70b6dd563538dac24b1723f8527`  
		Last Modified: Mon, 17 Jun 2024 22:45:24 GMT  
		Size: 16.0 MB (15993390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eab164dab1fc04dce97660055bf62a47adbaf0ab1b597a2e793b8d8891da69`  
		Last Modified: Mon, 17 Jun 2024 22:45:43 GMT  
		Size: 50.7 MB (50705839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9efa8dacea2d7266698eb3da2be47f374709dcb801d628fea5bfb4bf1a7fa4d`  
		Last Modified: Mon, 17 Jun 2024 22:46:20 GMT  
		Size: 196.7 MB (196747465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f7cd256cdede38dfa3cb68f5b252b4678a17c83c5e7be456c165eebdc42535b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262133608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db97c661c8584dba7d8f4ce8bbe955776a8e803eef9587707aa92a8f102688a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:06:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1284840252b1ffa18ebffcad2e64de45bf1abd606a36285969141c9abcb94772`  
		Last Modified: Mon, 17 Jun 2024 23:07:43 GMT  
		Size: 47.1 MB (47118403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423b9cfca43b4fd55d1b80d76e6a74581a4e8f297832d84858042e350d25253b`  
		Last Modified: Mon, 17 Jun 2024 23:08:09 GMT  
		Size: 169.3 MB (169340063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:fbdafd2edc3ad1a27612fb5a8e10e71f81940b2b9a3db77ec06a7a54eb2cf672
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
$ docker pull buildpack-deps@sha256:2585023174de70c7a739ecf13c9902890dfdb6cbdadb7bdc62f5e6120738b283
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44176719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6f3fa5f0d93261dc94b286df7d7a7a920500038b1696e30c5d8309dd8e6a4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:933c5a7e7fcda9e71347ef577b0402acb24f54c0c1b5cf202c7ca039539dd7c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40455671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee25a2ae1518005147c757837d74a0e194f30a6ecf038b121c5c457550c91caf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c6e7799bf53219915d10713f87d73e7cc8209401c4224383d5f4cf902c73d888
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43354946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f689d5a21cebfcc1d3289b9029026a240058725b66ce6182773b820ee3a91c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7f91267f9ade9d50a46c441f25adb5245e6d934483f64f103c1a8ac86e4cdc9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51620348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee715c5e481fd95866b33d2df89ceeb242d24d7fc463f34a7fdffef191c60e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:35:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680834b8998d6424161f149fd8d3eede4f74a70b6dd563538dac24b1723f8527`  
		Last Modified: Mon, 17 Jun 2024 22:45:24 GMT  
		Size: 16.0 MB (15993390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c086031ca8e85b68b57730f82ea82afebed26666a4b860f27b5e1353787bc270
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45675142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40755402ca0e041f2c44a78dbfb170ad2c393e7d4414edb9adde22cb7aa4ccc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:2889a448b03110715f5d411dbc6b418cbf6aa98be43c12fdb20d42d2c6653855
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
$ docker pull buildpack-deps@sha256:7cca663125706539abaff96a7d22357007092215aee78e08316021ff7e5ae9e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89648628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145143d9069dbb8bdfdc88150b49b7e6a63b0813dab5fd0da1f1aded0f85620`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72ee9d28d3323b69c1e98217df15ce99add4d7029330c19edf34afb08d0f6ec`  
		Last Modified: Mon, 17 Jun 2024 23:14:33 GMT  
		Size: 45.5 MB (45471909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5123e18b23283e983435188b0efad6a2bf55810a9c8e88df1ba1315a7444f2dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89468708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd91127d1bd2cc71e111ddd276b455226127a0fbcef23a11d5cb2f87709501d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:17:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3d83d18813ec3c59260e725e09e29242f2cc5cf4e44e224657d25db8a16c3`  
		Last Modified: Mon, 17 Jun 2024 23:23:08 GMT  
		Size: 49.0 MB (49013037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d477af5db35ff44f214f92b84de818dd3f03a0f70c7d55e35b9dd545853ff67f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88785094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e775b4006c238856702c6adaf6bf2c6669302a6aa934b083054d6e0dc514be4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609a6ad39dd54642e8c65403c8463121f544eaa46734a9398e92504cfc9b58b`  
		Last Modified: Mon, 17 Jun 2024 23:24:00 GMT  
		Size: 45.4 MB (45430148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c8896bf226b69733c0724cf927c235bed492e2dd2d7ed69a0eb70bb97673dca8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102326187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201ed28a9de01929f56df9c5db22af79dfb80dde6a6c37026373b3659b760064`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:35:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 22:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680834b8998d6424161f149fd8d3eede4f74a70b6dd563538dac24b1723f8527`  
		Last Modified: Mon, 17 Jun 2024 22:45:24 GMT  
		Size: 16.0 MB (15993390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eab164dab1fc04dce97660055bf62a47adbaf0ab1b597a2e793b8d8891da69`  
		Last Modified: Mon, 17 Jun 2024 22:45:43 GMT  
		Size: 50.7 MB (50705839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5e817c6055ba102aedf7daa16c007aa70e27821ff653e39f3541ad249ec340d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92793545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4887a2fe2a1ed08dfbb5a70d4130f2d0aa6d26478ccf9e13890eff22d6363f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1284840252b1ffa18ebffcad2e64de45bf1abd606a36285969141c9abcb94772`  
		Last Modified: Mon, 17 Jun 2024 23:07:43 GMT  
		Size: 47.1 MB (47118403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:a654d52e4608eeec0b8d6dca760d413fe31317b6fb8183f7c68c149b7cf96e16
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
$ docker pull buildpack-deps@sha256:96aa4125d8f866a6785439835e61cb499edd11adc09aa9a62ed339a802947543
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348989680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed840514560ecb23da04a87e26e68226347cd0918f03e72a626ea1de94fd456`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:07:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dc1019d7935fe82827434da11bf96cf14e24979f8155e73b794286f10b7f05`  
		Last Modified: Tue, 23 Jul 2024 06:14:07 GMT  
		Size: 211.2 MB (211241610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:75f7bcc90a107ae0a8c7d579a00e36db8d3f92fe9ad0004a7aab4ee3dc835388
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55ad79738158b9b559b3a6288f599b973b8d833c9853056b0abfbb42a663986`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f383f84306b6f41c3ed73bdfceb22befd854a21432eeb20e66606aa7f0de1a3`  
		Last Modified: Tue, 23 Jul 2024 03:53:14 GMT  
		Size: 184.5 MB (184529578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b700c1d49e1f79f868c5189c14f66db5cdb8704cb0537f367d7b9a1a9062563e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301508491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec96321e5eac42f04632d42f615ae2a2b80b43033a1e83898bf7f42ef0868d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:75647bbd8cd18fcef825cbf38b3481b77336c708c0b01dfde68160a54d253329
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339785031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbf3968966835222500849ac2ff10413acfb4b7619efea0037b113106497938`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d03d80f0fbcb18457424c859d43d6dfffc35d1c45e5f23b15020e176392f5828
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351616214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461ad229eee29e7dc604ca63e86ee7e94aa4f774d534ce3feede24a6067a99d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4a7c31652ee354c7323f3315523d185b07416d8cb4bc316907ce5389dbee90`  
		Last Modified: Tue, 23 Jul 2024 04:49:51 GMT  
		Size: 210.2 MB (210156525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5594e02abeeadcf7c3da5c425498803af089369c7c29f9364df5e038e9f0a83f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325970317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c681e16b27e6af6e089f0cc788f13d8603dbc1667f2f2fd3017f34a437c262f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:31:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9bf98f8625482717f751cc9795fbc191bb19c8a1b474435b13be58561da0b`  
		Last Modified: Tue, 23 Jul 2024 02:01:39 GMT  
		Size: 189.8 MB (189804860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1bc97343130aa4ba3f5649e57b64b8993e7826e9e406e70115c4b43d74f75736
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4919d10ea191445ba34fdf226173f4528ea1d10a1282b0a48731e4f63692a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:377884cf88179e14c6ff704b53232cf6b55f3eef045612a04ac496fbf1eebf4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318370734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797108ba88070ce02961f0112d95ab47909ee25ec71bb86877aa6a49b66214e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:bf7e3a7f11e5803e1ee3d143d1f4324fb768d6287dfe0a167992024eaa71963e
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
$ docker pull buildpack-deps@sha256:4216ba7e789db813eef27113ffc0e7798f461f316bcfa059615e2920b54d7b86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73604871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499bc7f80746cb842f582a9553c7c763a503d471e561ce5c05e1f2a23097e6a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d2f44c22fd4532965fb02333473e85c6d3ab86609da43e49d723754abe3d1427
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722b23eda8fb4d3431b7031cfae4c188bd177309d8390d5b4e53e97e3495e498`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:425da63e21a8968bab7eab3050f542ae6a46e81ba6972b5aa4198380192c407d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67102785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0795e70b98c0048818600534dd4db827d5f7683f4a675ce9e2b8f51cf5a89d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a8155f724f1e6e368526d3793b1e62b186bc19d14d3bc9017ac2b29aa075cb8e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc5c4b620ecc5a3f564f49bbc825a6843e429303da6ec5de922ca9a2fe13fe6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64b00994df20baff3673b688e5ba2e439f5700e377214e45416fca94433fd7a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b86e5b7a2525a74ba3a1b1d71faffff73e72c5eed68cfdbecca4a70652bba3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:59005510b61f0f0ef977e4f2962bab45b50e47a53845aa5cc1d7786d44a5ada4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84595c9eabc4b54f273d65e511c9cf48b6e5d6e8409b6ae5813074faa4797603`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44a13b4fd2ecaf87d3361e50327286868a7ff3b7a41b6e877c1b5e4b22990de1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3cedc1cf1f38c69c9e9ccb44c8ddcdb8c4513da74fdf516f7837f69ad38b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6b42e6b8dbdd9cfe8f865b7b7e3f24f0c902f08fad4f5ee71ad91cfc1eaee04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13456429367f068f0a2cd22da31db81103299aa4b4714e95244a0eb0a3defd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:6976225849ed01372fe39066d7fb17c36ccffe53b6278886a5af525265e2afc1
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
$ docker pull buildpack-deps@sha256:37bc82e1ffaada99675f7c27376608cfff5fb56ae24fcc19756296dfe72405f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462d4a80b845e56a63fc8715d615dcdfdf198132ea93f5ad29a7ef236dfe7ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ead148a14be0e2afbbd64a5d75545bdbc67d5e495d64a0b0dea93bda62a8ce65
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131570072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcbd3cbc69a70376ad459ba896d3c18d643b49949a8d1af3d137168be02d2ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d2d65254d091265f939d4ef9a5c69f4f96bed13cb391222b43663acabeea0e4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126325600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27630f25b34b76a6ed40de03ebf679bfe86c39dea5e799983ac8f182a9c2002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef0610482c2e5909b3035c731b58fe4e0e92503aa55184971b4c76225a1a6d71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137174230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8237381f2e62f9c64dce46304e239cc2525c498fa324df76649544daabd946`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1e53076e757e1a41fe591c7f1e4e7a73884ae1bd0ccb718c22fef1bf4e4dace8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e116de79bd7590d0d53a2256e2f90e344e581ccdff8df85ed6c35ed1b99138c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8a04c418d221f88c661ce9fe8d82e529a1defa8a456c524b5f43de0297711bef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d65e857df7d381ad6a1edab761c02e89f343484180e7d10d5fdca547f9dc7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59fad96d845621440d0ea25364fecb6fd032c65ce53b07df77cb6b3d3c51b1ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf5d917a1d1b050133d4e48093febe11d2ea19d61e4a1cab54dcb39dba62c40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af65546aef0be20475bd81e286ca22b7ec1c1f436b29f08a6d94103f81830110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06da605e1e080ed7ee6281acc3ff42965cadd025807adb75473222af2c8c21bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:f170f181ea7c562b477ada0b581509406db3a81d8e541be521197287f0f6b6a2
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
$ docker pull buildpack-deps@sha256:5719e0100f0de0a49b65c1d0a7168ce45eb80f5b2bbabacfd847fcc78c42b8cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322476575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f42335de5c8808ef874f20a66cda1517328eea560574fe7287729d507f7ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:09:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c6efb0908b76d25c6355b6afc739337771c5a9f3a556c262cb1d0c767b6604`  
		Last Modified: Tue, 23 Jul 2024 06:15:02 GMT  
		Size: 197.0 MB (197039174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:182380f39ae0e270be65c806d1ddd928dfeeadbbcbd9e64d41b90f1a8a1df17e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295540784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dbd5741723e0879bf1485eeea459f127119a450752404039464f4863de47f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:41:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:43:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b062df9eea8fb3b005e76c03f7ef72ba9331888f68b2b9dd6b1f7afaddd042cc`  
		Last Modified: Tue, 23 Jul 2024 03:53:50 GMT  
		Size: 52.3 MB (52329700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5972ef34abc8f8302675fa051e04d2b0db7995a024a1f4298f5a462fcabd0d`  
		Last Modified: Tue, 23 Jul 2024 03:54:35 GMT  
		Size: 175.2 MB (175246775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6bf27a78e3cc626d21dba8d100dbb9a36e2baee8376366e7de7192d12a7da59c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282981788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b588c5bbdf1d403f11c3e62c2563ef328fa139967a225442d867cb171518dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7dd73ef69a71e0df94b32b858c9f24073577ba71f5b1051153a44ccde294a5e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314102222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca99d083a4ed5bd7e7677b36202282952a95d2e9802e1586fec6be0276244d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:53:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75f0ece8974d005f2532701f9fffb099d09a9bd1a53465b796982e4c2f594c`  
		Last Modified: Tue, 02 Jul 2024 04:03:16 GMT  
		Size: 189.9 MB (189935947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:93260457ef10b0b3880d788d8e7a4a2a1f7a5b88822d15a2d046489e85d420b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328213978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0a13798ca5638cef17990e78215ba03b311bf89ce25f0d2dac91a2c5e393d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:43:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30928a030df8a953adc83c67e2ab17a4c5048cc04287762bc9e03e269fe7c3dc`  
		Last Modified: Tue, 23 Jul 2024 04:51:04 GMT  
		Size: 199.9 MB (199944219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90707d07e88c5456e10f0504199636c1e8de85352b20db5391157aa8a573bbb2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301517721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c2735c637f37fa7ccb5acf1d0ec690e6916d35eaed079a0fe45605d74a5aca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:39:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99842c367e8366da5cce8062955a8adc51f02bf39119fe6c706b6971d2a9d218`  
		Last Modified: Tue, 23 Jul 2024 02:02:48 GMT  
		Size: 53.3 MB (53311607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18848575707cdf418cce9d480db3e082d823f30e54ae921840643faa7d52a14e`  
		Last Modified: Tue, 23 Jul 2024 02:04:47 GMT  
		Size: 179.2 MB (179160971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28b7060984a9a006e31c0b82fdf3b4b02404fb351512878238b54e753ff9c7b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330989547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ecbd4e6769fe22daa9e42e241ebba651c7dbd72ad9d14ca138f4e7df9a1f2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e81e7819bebf367f17dbc683fc34c6aadc4158e9b6b05cba1a4c966f077d02f2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296099464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed3096195a0e5b0ecd4d9873a4d0b50f8c7665fb711f4c3738969baaf1b57c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:79ef5da615c4aabe9c8b65081d6f59846ce47101b294949cb49fbe9268b0dd06
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
$ docker pull buildpack-deps@sha256:a504bb2cc4019727fae50df881b8bf5ecb5514e79daa53179da6056f57a6401d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba75d7cad2670b5207d207623743c4b2b2c437726cdeca5f6f3fe17ef78ed2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eb8435553af2ce9919814f08faf602ce03fbe0ec9b5724266dc68e907ea42b49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb193bd8f4c63c65ee9227c16f9d7a483161a469ccf530a8c88c258a9254be2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:34982cc2831f44918cef0bd5cd34ae8b96f2706e617bae9caf68a6acd96e74e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65122020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9c594b42a25d0f6ed9f5f895af4f5ea2e52bf56e17daac70f14c13f112079a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4bc65dbdf99b85e1d096a0b5fe82b7e18e999520ad8326df8dc8ef225adab48b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69471218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe19f2cd286b38892de1f8a24683cd9aec0ca038b7058f752e0298ab3262774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:167054572b59412b36ebfe3b4eb40d3c86c4452ada800413c5ec812f0f6973a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d426404e66e09e52514300bbad7094e621048ecdd787582e9911ee078f8f1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fe1a8cd7f8e57bf72c67bbc2f30188367a8973caee362c8418646c43103540a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69045143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff7e128d711d5080cdfb492363b6bb11153bc1b4befef6c3e2e3318f597daaa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:446c4d72ab4ad87a7dbcf025a258a2f642ee39e0712060c917936192bf940eaf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ea32ed165cd42a1567b0f3b4b216122c7b0511c2a69b04c57d10a6f49d2081`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a174b73fb0d4d8958dbabd27c12a350813aecb073857b648794b226c82046e68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68965812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3210584f000afb879f87d583b2703d804c1add30b83c9610f1095ed1f7ce6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:23ec434d35fd158825845b9d0b0e3108f21c7aa1bef4444082274392677b755e
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
$ docker pull buildpack-deps@sha256:69d36ad13ecffb8dd51412c7579dbecc4f17f661dd9fd8857c14875fa43c95c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125437401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfdd900dd285a53a5afb08c6190630059edec24d4d75b3bc125b723de69ebcd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d22f58ffb9427c05e97e6462a1b3385feb8d7f61143e82ca06fc8afc50d88096
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120294009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd7a259fbd58722024f4504fe24e9f1bf866bb69095de420706fa88ab53c2ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:41:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b062df9eea8fb3b005e76c03f7ef72ba9331888f68b2b9dd6b1f7afaddd042cc`  
		Last Modified: Tue, 23 Jul 2024 03:53:50 GMT  
		Size: 52.3 MB (52329700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfaf01a3c00dc625c6f22ee3e0a942a8e0f9577d3166ade3c3086f20dfbbf645
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115479818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0323fb2c99dcde25333251776876e1dea9c3585e9e3fa81040ac9d49edfd7b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:78a1705430080aa1449064e2437d48b39c14b54085a4dbd017e06b336e846b7e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124166275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71dbaf9643ff77b80b3b18db7dea38a1341cacfaaeedbf094d402d8947695c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fc507dd2c0ae791a27569c497f2750526f3fbdababe837b3ef1e1104444858fa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128269759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebfd400e18099c87719624296a965748d8640a394cb9395e431379460bbf19d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7c158891bc067ee9459ab34e03960b31f256a5841c91ab1c25d474663c1fdb73
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122356750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451b4e177fa1a4e8c432f462a9a1def547ea1da5090ed6ca90715d446cc6b405`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99842c367e8366da5cce8062955a8adc51f02bf39119fe6c706b6971d2a9d218`  
		Last Modified: Tue, 23 Jul 2024 02:02:48 GMT  
		Size: 53.3 MB (53311607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6d5be2179353f4ee7aa2378890b84a27085d33d98ead9e6f493567846e90da08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e071c1475ac021ffe4b1dfc80f52e92321ab7395ebcf2491166490edf412f38a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b4fb3f45bf0497cb7da93e1e5f88cab03e0ac0c6f552b9ed7f3a23d433ba6115
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123041107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a010209e7a82320af74aa73e24fd4954556e0248f6588f002eed4a7dac0df82e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:bf7e3a7f11e5803e1ee3d143d1f4324fb768d6287dfe0a167992024eaa71963e
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
$ docker pull buildpack-deps@sha256:4216ba7e789db813eef27113ffc0e7798f461f316bcfa059615e2920b54d7b86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73604871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499bc7f80746cb842f582a9553c7c763a503d471e561ce5c05e1f2a23097e6a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d2f44c22fd4532965fb02333473e85c6d3ab86609da43e49d723754abe3d1427
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722b23eda8fb4d3431b7031cfae4c188bd177309d8390d5b4e53e97e3495e498`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:425da63e21a8968bab7eab3050f542ae6a46e81ba6972b5aa4198380192c407d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67102785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0795e70b98c0048818600534dd4db827d5f7683f4a675ce9e2b8f51cf5a89d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a8155f724f1e6e368526d3793b1e62b186bc19d14d3bc9017ac2b29aa075cb8e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc5c4b620ecc5a3f564f49bbc825a6843e429303da6ec5de922ca9a2fe13fe6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64b00994df20baff3673b688e5ba2e439f5700e377214e45416fca94433fd7a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b86e5b7a2525a74ba3a1b1d71faffff73e72c5eed68cfdbecca4a70652bba3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:59005510b61f0f0ef977e4f2962bab45b50e47a53845aa5cc1d7786d44a5ada4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84595c9eabc4b54f273d65e511c9cf48b6e5d6e8409b6ae5813074faa4797603`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44a13b4fd2ecaf87d3361e50327286868a7ff3b7a41b6e877c1b5e4b22990de1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3cedc1cf1f38c69c9e9ccb44c8ddcdb8c4513da74fdf516f7837f69ad38b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6b42e6b8dbdd9cfe8f865b7b7e3f24f0c902f08fad4f5ee71ad91cfc1eaee04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13456429367f068f0a2cd22da31db81103299aa4b4714e95244a0eb0a3defd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:4917acbdddf57839e4c0b24d27d35ecbefcc092f41b21239f0dbeac4f127a846
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
$ docker pull buildpack-deps@sha256:ba010e8fb935edf3da510e4aea79b5d7bc2d5dd111469d976b0dddbe7608ea42
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245780758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9f9c7022ab7dc85725e96dc9826990fb316d39179a85978b344aeeedd38626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:33:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0b693a55ba8f2f62faf455314042339a92e3d947e131e8a5a9f4763a1be17`  
		Last Modified: Wed, 05 Jun 2024 04:47:16 GMT  
		Size: 11.1 MB (11131677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06da50534abdbd308d398fccbe7e605e7f760e1b302bc5e8c93058a0cc623057`  
		Last Modified: Wed, 05 Jun 2024 04:47:32 GMT  
		Size: 60.9 MB (60904546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c4ebd31b8500a7712d1ae95d94414f30f7d631d78273bca63023061288005f`  
		Last Modified: Wed, 05 Jun 2024 04:47:59 GMT  
		Size: 145.2 MB (145160312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a23f2782fc97e8fe46e3f205e0e321b503d8cdcc742c531649d045296c8bbd24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212061023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116400feeaca1f1a55f3db77c993044d3f25a50ab4e0ee4854d812d58220321a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:36:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054f0865ad2a3115262baff79f0f568e9aca8177cf21e36926e786435734f85`  
		Last Modified: Wed, 05 Jun 2024 03:51:48 GMT  
		Size: 9.6 MB (9605337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e7c4e1d26ef933f7ebbf4e7360073197b166ada1ffef28e0a0fc7eed78f1c`  
		Last Modified: Wed, 05 Jun 2024 03:52:06 GMT  
		Size: 55.9 MB (55878345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2c9e45258c5090b9e1484a8b0970c5bff6261cb1e7cd3218713c001827885`  
		Last Modified: Wed, 05 Jun 2024 03:52:31 GMT  
		Size: 122.0 MB (121973520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:305862bddac325eca5677b4fcac1ece055411d7befbbe2e507d43e86c3435860
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236070178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45de648bc3af4cb828dd7e8e0b36679adbb36c02b77e4362ce1526103b3daabb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:16:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4413e6a295aaaf041c65afd5671da95530820e6794dc6794636779b453a113e0`  
		Last Modified: Wed, 05 Jun 2024 04:34:11 GMT  
		Size: 11.0 MB (10982267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f58de85ef18320037487fd40921c0911a92f3ec25aae271afde8c56a8bb4e`  
		Last Modified: Wed, 05 Jun 2024 04:34:26 GMT  
		Size: 61.0 MB (61048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c73a257ae5bd83fd91d91c82db58648a6e0fcbcd585d8c196e275ecaa2bd20d`  
		Last Modified: Wed, 05 Jun 2024 04:34:48 GMT  
		Size: 136.8 MB (136834570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a318e4bb6bd67f9bc99e8d13d86edec736680c6b3a56a4cef8ba24599e86284e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269548339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b768226a4fdb4a30fb5cb279e11f6ebbd9f6925dcd028d103ca3558ce6c46c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:26:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a754598d82cd0c4fa1bfb084eefb9b3546c06014e24ca2fe14744cd7a8cfc6c`  
		Last Modified: Wed, 05 Jun 2024 03:47:02 GMT  
		Size: 12.9 MB (12940693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25fcea00df150e7a968dcaec967242a0ede82c633184af93a23b2aa72ef279`  
		Last Modified: Wed, 05 Jun 2024 03:47:26 GMT  
		Size: 69.7 MB (69653712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba1fdfbd84911122cb9e50d5a5c7c470af1cd2b1a763b0032cb81022b8d5545`  
		Last Modified: Wed, 05 Jun 2024 03:47:58 GMT  
		Size: 153.6 MB (153637814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1eefab6d67f98518179c8875573265b781a9d6325d3d060c6ae6666d619580db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226586223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b77468d7463e0bee053cac5bc2dd61782f52a88dbebb677fbe86ead433af96f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc882b1d2007230b7ab89a9d35944234befc417c5e38abec94ad4318f2b6421`  
		Last Modified: Wed, 05 Jun 2024 03:34:51 GMT  
		Size: 10.7 MB (10689958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78260c3c16760a1f95b5fb979620b45c7b2c5950d3c13b9cf8081e756194188d`  
		Last Modified: Wed, 05 Jun 2024 03:35:05 GMT  
		Size: 60.3 MB (60326843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e875c0f87834713797b2b228fd805bcfd69354b86e0309792cb236c9681887bf`  
		Last Modified: Wed, 05 Jun 2024 03:35:29 GMT  
		Size: 128.6 MB (128556004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:d2804bd67516754f7de978473764961c38399b6e1b48957312575cf7a7e4189e
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
$ docker pull buildpack-deps@sha256:6927690522f55e0fd3f47eb6cdefb512566ce3a5751b56a686320305c5bb8c52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1e577e5af8c42784c2dc438e51fa644b8b201e9ce12bfd90f944a4b69ec99e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0b693a55ba8f2f62faf455314042339a92e3d947e131e8a5a9f4763a1be17`  
		Last Modified: Wed, 05 Jun 2024 04:47:16 GMT  
		Size: 11.1 MB (11131677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:544358616bfab643d93a6adea54f434006a1f880b9ecf9af77ad6dd734a85539
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a21e0887b03608386457aa7a4559be214c9768dae621788490faee42d0e7139`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054f0865ad2a3115262baff79f0f568e9aca8177cf21e36926e786435734f85`  
		Last Modified: Wed, 05 Jun 2024 03:51:48 GMT  
		Size: 9.6 MB (9605337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a490e591096a5ffdd0f340b850a6b17398f0c301ffb1da3c2d362d3449de617
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44eda57b7725c60dfae1152e43b88e5c0d15300f75d21dff6fe54cd9048f0d34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4413e6a295aaaf041c65afd5671da95530820e6794dc6794636779b453a113e0`  
		Last Modified: Wed, 05 Jun 2024 04:34:11 GMT  
		Size: 11.0 MB (10982267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7997b415e34aa9822233a3b764d3d0e738cb674da245f3f68a70b13384920812
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46256813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25c58cea52f14836a13e1fc4f8aa38485d327ee8a137a1fc054166a8e1c2f84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a754598d82cd0c4fa1bfb084eefb9b3546c06014e24ca2fe14744cd7a8cfc6c`  
		Last Modified: Wed, 05 Jun 2024 03:47:02 GMT  
		Size: 12.9 MB (12940693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c9ca6b8549544f386947559ac95988cfd53bd56c4fbc9bf0c78703aca1b23a7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37703376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4252506b2904a0edad3f1a8836dc34ad01b2c2f61c806390b402b30925b8cd76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc882b1d2007230b7ab89a9d35944234befc417c5e38abec94ad4318f2b6421`  
		Last Modified: Wed, 05 Jun 2024 03:34:51 GMT  
		Size: 10.7 MB (10689958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:0e1b4b264fd8894d4dd737514d939d13316ec953da2b4e0c8d1270f17ed6575c
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
$ docker pull buildpack-deps@sha256:42fa8b21b4cf1931817ef1f947b9b036db2be147476904e9cdc8a8607a193ab5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100620446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7440898ca26905d7fbf4c58765072d2a7e7e26b211cf27cf067bbde28eecf8f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0b693a55ba8f2f62faf455314042339a92e3d947e131e8a5a9f4763a1be17`  
		Last Modified: Wed, 05 Jun 2024 04:47:16 GMT  
		Size: 11.1 MB (11131677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06da50534abdbd308d398fccbe7e605e7f760e1b302bc5e8c93058a0cc623057`  
		Last Modified: Wed, 05 Jun 2024 04:47:32 GMT  
		Size: 60.9 MB (60904546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:844adfbc56b1fd950f0ca8ed779aff9f7bb902b5d87da154aa145dc66799fc80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90087503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54efd6a8865a571dfdbcbb46c5bcfb6b1c889bde6d4e70054e803929f7d389`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054f0865ad2a3115262baff79f0f568e9aca8177cf21e36926e786435734f85`  
		Last Modified: Wed, 05 Jun 2024 03:51:48 GMT  
		Size: 9.6 MB (9605337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e7c4e1d26ef933f7ebbf4e7360073197b166ada1ffef28e0a0fc7eed78f1c`  
		Last Modified: Wed, 05 Jun 2024 03:52:06 GMT  
		Size: 55.9 MB (55878345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d3a5f4a3f845783df4f54f85b874ff01179ffe3d95070a493d3fd714d708538d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99235608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290f83f01f5cb4fae9145262b114d04bef79bab5b0f3823c71c1e8f6a36b73ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4413e6a295aaaf041c65afd5671da95530820e6794dc6794636779b453a113e0`  
		Last Modified: Wed, 05 Jun 2024 04:34:11 GMT  
		Size: 11.0 MB (10982267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f58de85ef18320037487fd40921c0911a92f3ec25aae271afde8c56a8bb4e`  
		Last Modified: Wed, 05 Jun 2024 04:34:26 GMT  
		Size: 61.0 MB (61048097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cc4c735cd16433b98003cbda97b3c6477eceade9d30508271126b2cde85a498d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115910525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886f669f80c106b2b436c8eb04e0af813278dcf355cb13888e7bfd5c9adea39b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a754598d82cd0c4fa1bfb084eefb9b3546c06014e24ca2fe14744cd7a8cfc6c`  
		Last Modified: Wed, 05 Jun 2024 03:47:02 GMT  
		Size: 12.9 MB (12940693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25fcea00df150e7a968dcaec967242a0ede82c633184af93a23b2aa72ef279`  
		Last Modified: Wed, 05 Jun 2024 03:47:26 GMT  
		Size: 69.7 MB (69653712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2715f87961d0874f18198a6d70d0db6d875cfdb2465e0feb38def26ddd8c503e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98030219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b51504aa2dd127e70170ba14f268aa5c30456e27e07cfd7d8140bc833e7c06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc882b1d2007230b7ab89a9d35944234befc417c5e38abec94ad4318f2b6421`  
		Last Modified: Wed, 05 Jun 2024 03:34:51 GMT  
		Size: 10.7 MB (10689958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78260c3c16760a1f95b5fb979620b45c7b2c5950d3c13b9cf8081e756194188d`  
		Last Modified: Wed, 05 Jun 2024 03:35:05 GMT  
		Size: 60.3 MB (60326843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:b64e26f7623add790c8a6ce03f037eb1460781b5d32306d7ce6a91d217a2f602
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
$ docker pull buildpack-deps@sha256:c9f18dbc064cb00add6f56d99c0ccee39e58613773fbc172699bd4ee329c76be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250100638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4b7a675592556f99e88b4251ead06d069e3a498b4d310ceede2e0044cfc78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:59:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966d1a9d7dc827a9dda799795c07c44b594a52122c0b1c90242bab120d580c8`  
		Last Modified: Tue, 02 Jul 2024 02:04:36 GMT  
		Size: 39.5 MB (39454836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92a2766b622bfa17b0f88039006043d2679278f6b9b0af753fe338799989c2d`  
		Last Modified: Tue, 02 Jul 2024 02:05:05 GMT  
		Size: 173.1 MB (173114486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7436788773aee27b47b1a19a321dfd08518f0ee99d3d7b74c3ed05677c42b5ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217355681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0411dd00519e96e92a315428e1c9df69bba263d0d66d84234e47c0001e1226a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19939d362c9742ec7a32f61568520eb8438dc48cbc1335ffd7fa62bf170ceb4`  
		Last Modified: Tue, 02 Jul 2024 01:43:51 GMT  
		Size: 42.2 MB (42243066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdb9d48df11dcb10a55429ed8faecc54ee6b181eaa7468edf44aa87d620423`  
		Last Modified: Tue, 02 Jul 2024 01:44:23 GMT  
		Size: 140.6 MB (140586490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30aedfb24e94c3d840d5f5da9644e37b59a6067882721f954fb7df6abaa74114
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241407221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dde0b121101a91283781bae0ba338f3f71c7c26e2932449f91889dde1444222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:00:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aac2765dc6695d0f69e7852783ff14ecb83d04db68edc06347651928706052`  
		Last Modified: Tue, 02 Jul 2024 04:05:26 GMT  
		Size: 39.4 MB (39378111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686de3b37c2fe2d4b0e553fb3424ba1a1d18540b69904318345c4bfb40cea4e`  
		Last Modified: Tue, 02 Jul 2024 04:05:50 GMT  
		Size: 166.6 MB (166594707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0c9760fe788d9a2ed38a47db502dec216c552f7bff1f0caa5fb21e56fca30089
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271199025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207e8270610c8fa214e29f960e5e11bcdf9ada1795f14076732aecdd7c2dacf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:58:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:03:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82dc8e44a33d0f6fbe0c131eeb8268e1997857f2a63a77b883c6c1e387f308f`  
		Last Modified: Tue, 02 Jul 2024 02:09:30 GMT  
		Size: 43.8 MB (43765840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55636e60f9b3d7c2476012046397c3971c113c7813a4e788ee8e7ffc35a0589`  
		Last Modified: Tue, 02 Jul 2024 02:10:05 GMT  
		Size: 183.7 MB (183654409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:908b950080e80f068a5cd141b29e1cbc0a9b2ccbb3de3a9a3c22c0fa61d39885
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223830002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588eb12b48e4275a58886b6c9420f240d34d3f67190050a6fe73487fab8e03d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:43:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693aac14b0c492b501054836b25b7b1ce8545575960bb0ddd3c31b6bab5bf990`  
		Last Modified: Tue, 02 Jul 2024 03:48:05 GMT  
		Size: 39.4 MB (39420301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff72f078d5786a1145e8ba3fde463cee759a8cb800d930db19c82c562d69034`  
		Last Modified: Tue, 02 Jul 2024 03:48:28 GMT  
		Size: 148.8 MB (148768969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:d9695055e7e1a2582e6edc6a7a05cf7eba229ae0c4dbca24e2ebd58435993ecc
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
$ docker pull buildpack-deps@sha256:0544f948f0e350e0ffa71d159a741fa825bed92a575c1053b56ac45e9113177d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37531316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829a7f0ca64e1b4d275e10ab9b8a41357f0687de6b98b2bdfec2739eea5440a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:399c68581bdccc333843c661f9fe00a428848dc215eebdf801629d1c83f44eb6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34526125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c8e69939a6a1bb863ab0ffccb82e74e155e1a806793cdd17a8d7e285ddde6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13034def1ecea1c8eacfecc9509483aafed50615c56fbfd06b37bfec2984b99a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35434403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc4f871a468e94581d5299c4323c1c5a91cd3302b124e984159269b7812dd18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9ea311b77103ba1d8620c87a44dd42680745126c7d3c72c1edbc535834bdf3ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43778776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50574c983273271b7aea34ce7e841ba3f4b6635c7fe1a38502f1bc4fd9071c63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5fdc9ee3bd4ef0529decc62d532e385768cd9ab7ba9597c418237a72298c19f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35640732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9935af9770bdb0a8bf700e8236379bfc9508df5fe28b253cc26d4ab9224dcc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:19bc4f95f87bb2f0975c5f1090b6a565022a1f890e19af055e3e4f0d701af074
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
$ docker pull buildpack-deps@sha256:5d9cb6dcd1cd3180bf36be7ce1fd0201ff08d3a2e81d30ffe7315220545f6d70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76986152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4a1ee970e379a731f912d64cc05bb22e84dae7cf91b51acc2d8790d824a2a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966d1a9d7dc827a9dda799795c07c44b594a52122c0b1c90242bab120d580c8`  
		Last Modified: Tue, 02 Jul 2024 02:04:36 GMT  
		Size: 39.5 MB (39454836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f82d4287805b367c95ad99bf810f131a7294023636c1db0f7f7e254a1db9fcba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76769191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132a36536fec47518fa8472beebbe070410f5a78ffbf2eac862b0670f3567f9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19939d362c9742ec7a32f61568520eb8438dc48cbc1335ffd7fa62bf170ceb4`  
		Last Modified: Tue, 02 Jul 2024 01:43:51 GMT  
		Size: 42.2 MB (42243066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:55fb4b90a5186d3029858ed5fb1e52fe778753ff241fc82ae91e64d794a2652c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74812514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628d80babb0f665e8b36e0039db96d6c42479562b28379fa8b430ab025a687c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aac2765dc6695d0f69e7852783ff14ecb83d04db68edc06347651928706052`  
		Last Modified: Tue, 02 Jul 2024 04:05:26 GMT  
		Size: 39.4 MB (39378111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8161f7c68935700123953ccf08bcec8ca4cddc7e431090a883b879c44eda157d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87544616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fbdf7b7eb43e810daf796858cfbdbb7267bbb2d358c2ea24f9556a300c3c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:58:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82dc8e44a33d0f6fbe0c131eeb8268e1997857f2a63a77b883c6c1e387f308f`  
		Last Modified: Tue, 02 Jul 2024 02:09:30 GMT  
		Size: 43.8 MB (43765840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4a9437676ab21da7b3ad03457706ea309e2494fe018e775af025e81eb288d464
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75061033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473e03988f89693816397ff7caa90aa86fe7f6fb6879e6e98362da2abe59e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693aac14b0c492b501054836b25b7b1ce8545575960bb0ddd3c31b6bab5bf990`  
		Last Modified: Tue, 02 Jul 2024 03:48:05 GMT  
		Size: 39.4 MB (39420301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:a654d52e4608eeec0b8d6dca760d413fe31317b6fb8183f7c68c149b7cf96e16
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
$ docker pull buildpack-deps@sha256:96aa4125d8f866a6785439835e61cb499edd11adc09aa9a62ed339a802947543
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348989680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed840514560ecb23da04a87e26e68226347cd0918f03e72a626ea1de94fd456`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:07:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dc1019d7935fe82827434da11bf96cf14e24979f8155e73b794286f10b7f05`  
		Last Modified: Tue, 23 Jul 2024 06:14:07 GMT  
		Size: 211.2 MB (211241610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:75f7bcc90a107ae0a8c7d579a00e36db8d3f92fe9ad0004a7aab4ee3dc835388
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55ad79738158b9b559b3a6288f599b973b8d833c9853056b0abfbb42a663986`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f383f84306b6f41c3ed73bdfceb22befd854a21432eeb20e66606aa7f0de1a3`  
		Last Modified: Tue, 23 Jul 2024 03:53:14 GMT  
		Size: 184.5 MB (184529578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b700c1d49e1f79f868c5189c14f66db5cdb8704cb0537f367d7b9a1a9062563e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301508491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec96321e5eac42f04632d42f615ae2a2b80b43033a1e83898bf7f42ef0868d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:75647bbd8cd18fcef825cbf38b3481b77336c708c0b01dfde68160a54d253329
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339785031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbf3968966835222500849ac2ff10413acfb4b7619efea0037b113106497938`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d03d80f0fbcb18457424c859d43d6dfffc35d1c45e5f23b15020e176392f5828
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351616214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461ad229eee29e7dc604ca63e86ee7e94aa4f774d534ce3feede24a6067a99d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4a7c31652ee354c7323f3315523d185b07416d8cb4bc316907ce5389dbee90`  
		Last Modified: Tue, 23 Jul 2024 04:49:51 GMT  
		Size: 210.2 MB (210156525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5594e02abeeadcf7c3da5c425498803af089369c7c29f9364df5e038e9f0a83f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325970317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c681e16b27e6af6e089f0cc788f13d8603dbc1667f2f2fd3017f34a437c262f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:31:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9bf98f8625482717f751cc9795fbc191bb19c8a1b474435b13be58561da0b`  
		Last Modified: Tue, 23 Jul 2024 02:01:39 GMT  
		Size: 189.8 MB (189804860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1bc97343130aa4ba3f5649e57b64b8993e7826e9e406e70115c4b43d74f75736
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4919d10ea191445ba34fdf226173f4528ea1d10a1282b0a48731e4f63692a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:377884cf88179e14c6ff704b53232cf6b55f3eef045612a04ac496fbf1eebf4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318370734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797108ba88070ce02961f0112d95ab47909ee25ec71bb86877aa6a49b66214e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:001fbeb72df6623ac6f5c8f4fed31907b3d5ea2d6f8598216dd1872954942f6e
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
$ docker pull buildpack-deps@sha256:3558c964bf569f730093af41bf7496ec8d4cbb6e69653e6fda835ebed85309b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279729175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82247edddad280d6499bfa94389367908da72e47f5cbd48cc6b83cc0d20ada62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:13:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72ee9d28d3323b69c1e98217df15ce99add4d7029330c19edf34afb08d0f6ec`  
		Last Modified: Mon, 17 Jun 2024 23:14:33 GMT  
		Size: 45.5 MB (45471909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4b0288e2a65f9614fc7da6a77af34c15de35b61856448bcd3ca1a93e04db1f`  
		Last Modified: Mon, 17 Jun 2024 23:15:05 GMT  
		Size: 190.1 MB (190080547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:285c1b047419cf6a8071afc484727c1205c15a326e8704ecaba9ad4f044b2640
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239985378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be4225e767be58ed197589ddc16270b3accfec747bdbe1efb5da62e7d7e3d68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:17:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:21:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3d83d18813ec3c59260e725e09e29242f2cc5cf4e44e224657d25db8a16c3`  
		Last Modified: Mon, 17 Jun 2024 23:23:08 GMT  
		Size: 49.0 MB (49013037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761541af846f1634fcac3c55a1f928683a08646e68dd952f7001446a3dafabb`  
		Last Modified: Mon, 17 Jun 2024 23:23:38 GMT  
		Size: 150.5 MB (150516670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1315d2b678fc049a83e52615f97cae207a5b4093c86c215f47592d40c127e851
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270824823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b448c66459f3c077e3bdb7a327170ca53a59e4d8c1b39ddf8ae18f4df231b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:22:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609a6ad39dd54642e8c65403c8463121f544eaa46734a9398e92504cfc9b58b`  
		Last Modified: Mon, 17 Jun 2024 23:24:00 GMT  
		Size: 45.4 MB (45430148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fecb27a7a128ed30affce580f6ec163cd82f77778d337689b1c0f4a642d2ac`  
		Last Modified: Mon, 17 Jun 2024 23:24:25 GMT  
		Size: 182.0 MB (182039729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:45adc8dab7a8c195f39152c2764e82265084d5984a856be8097b57d3413cfa0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299073652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad2c98f93ba002f7a25b19376160c8f429f84483c3eb36be011a46bde6e8fcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:35:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 22:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 22:44:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680834b8998d6424161f149fd8d3eede4f74a70b6dd563538dac24b1723f8527`  
		Last Modified: Mon, 17 Jun 2024 22:45:24 GMT  
		Size: 16.0 MB (15993390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eab164dab1fc04dce97660055bf62a47adbaf0ab1b597a2e793b8d8891da69`  
		Last Modified: Mon, 17 Jun 2024 22:45:43 GMT  
		Size: 50.7 MB (50705839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9efa8dacea2d7266698eb3da2be47f374709dcb801d628fea5bfb4bf1a7fa4d`  
		Last Modified: Mon, 17 Jun 2024 22:46:20 GMT  
		Size: 196.7 MB (196747465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f7cd256cdede38dfa3cb68f5b252b4678a17c83c5e7be456c165eebdc42535b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262133608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db97c661c8584dba7d8f4ce8bbe955776a8e803eef9587707aa92a8f102688a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:06:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1284840252b1ffa18ebffcad2e64de45bf1abd606a36285969141c9abcb94772`  
		Last Modified: Mon, 17 Jun 2024 23:07:43 GMT  
		Size: 47.1 MB (47118403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423b9cfca43b4fd55d1b80d76e6a74581a4e8f297832d84858042e350d25253b`  
		Last Modified: Mon, 17 Jun 2024 23:08:09 GMT  
		Size: 169.3 MB (169340063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:fbdafd2edc3ad1a27612fb5a8e10e71f81940b2b9a3db77ec06a7a54eb2cf672
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
$ docker pull buildpack-deps@sha256:2585023174de70c7a739ecf13c9902890dfdb6cbdadb7bdc62f5e6120738b283
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44176719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6f3fa5f0d93261dc94b286df7d7a7a920500038b1696e30c5d8309dd8e6a4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:933c5a7e7fcda9e71347ef577b0402acb24f54c0c1b5cf202c7ca039539dd7c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40455671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee25a2ae1518005147c757837d74a0e194f30a6ecf038b121c5c457550c91caf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c6e7799bf53219915d10713f87d73e7cc8209401c4224383d5f4cf902c73d888
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43354946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f689d5a21cebfcc1d3289b9029026a240058725b66ce6182773b820ee3a91c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7f91267f9ade9d50a46c441f25adb5245e6d934483f64f103c1a8ac86e4cdc9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51620348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee715c5e481fd95866b33d2df89ceeb242d24d7fc463f34a7fdffef191c60e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:35:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680834b8998d6424161f149fd8d3eede4f74a70b6dd563538dac24b1723f8527`  
		Last Modified: Mon, 17 Jun 2024 22:45:24 GMT  
		Size: 16.0 MB (15993390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c086031ca8e85b68b57730f82ea82afebed26666a4b860f27b5e1353787bc270
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45675142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40755402ca0e041f2c44a78dbfb170ad2c393e7d4414edb9adde22cb7aa4ccc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:2889a448b03110715f5d411dbc6b418cbf6aa98be43c12fdb20d42d2c6653855
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
$ docker pull buildpack-deps@sha256:7cca663125706539abaff96a7d22357007092215aee78e08316021ff7e5ae9e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89648628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145143d9069dbb8bdfdc88150b49b7e6a63b0813dab5fd0da1f1aded0f85620`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72ee9d28d3323b69c1e98217df15ce99add4d7029330c19edf34afb08d0f6ec`  
		Last Modified: Mon, 17 Jun 2024 23:14:33 GMT  
		Size: 45.5 MB (45471909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5123e18b23283e983435188b0efad6a2bf55810a9c8e88df1ba1315a7444f2dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89468708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd91127d1bd2cc71e111ddd276b455226127a0fbcef23a11d5cb2f87709501d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:17:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3d83d18813ec3c59260e725e09e29242f2cc5cf4e44e224657d25db8a16c3`  
		Last Modified: Mon, 17 Jun 2024 23:23:08 GMT  
		Size: 49.0 MB (49013037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d477af5db35ff44f214f92b84de818dd3f03a0f70c7d55e35b9dd545853ff67f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88785094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e775b4006c238856702c6adaf6bf2c6669302a6aa934b083054d6e0dc514be4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609a6ad39dd54642e8c65403c8463121f544eaa46734a9398e92504cfc9b58b`  
		Last Modified: Mon, 17 Jun 2024 23:24:00 GMT  
		Size: 45.4 MB (45430148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c8896bf226b69733c0724cf927c235bed492e2dd2d7ed69a0eb70bb97673dca8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102326187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201ed28a9de01929f56df9c5db22af79dfb80dde6a6c37026373b3659b760064`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:35:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 22:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680834b8998d6424161f149fd8d3eede4f74a70b6dd563538dac24b1723f8527`  
		Last Modified: Mon, 17 Jun 2024 22:45:24 GMT  
		Size: 16.0 MB (15993390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eab164dab1fc04dce97660055bf62a47adbaf0ab1b597a2e793b8d8891da69`  
		Last Modified: Mon, 17 Jun 2024 22:45:43 GMT  
		Size: 50.7 MB (50705839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5e817c6055ba102aedf7daa16c007aa70e27821ff653e39f3541ad249ec340d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92793545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4887a2fe2a1ed08dfbb5a70d4130f2d0aa6d26478ccf9e13890eff22d6363f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1284840252b1ffa18ebffcad2e64de45bf1abd606a36285969141c9abcb94772`  
		Last Modified: Mon, 17 Jun 2024 23:07:43 GMT  
		Size: 47.1 MB (47118403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:f170f181ea7c562b477ada0b581509406db3a81d8e541be521197287f0f6b6a2
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
$ docker pull buildpack-deps@sha256:5719e0100f0de0a49b65c1d0a7168ce45eb80f5b2bbabacfd847fcc78c42b8cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322476575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f42335de5c8808ef874f20a66cda1517328eea560574fe7287729d507f7ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:09:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c6efb0908b76d25c6355b6afc739337771c5a9f3a556c262cb1d0c767b6604`  
		Last Modified: Tue, 23 Jul 2024 06:15:02 GMT  
		Size: 197.0 MB (197039174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:182380f39ae0e270be65c806d1ddd928dfeeadbbcbd9e64d41b90f1a8a1df17e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295540784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dbd5741723e0879bf1485eeea459f127119a450752404039464f4863de47f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:41:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:43:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b062df9eea8fb3b005e76c03f7ef72ba9331888f68b2b9dd6b1f7afaddd042cc`  
		Last Modified: Tue, 23 Jul 2024 03:53:50 GMT  
		Size: 52.3 MB (52329700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5972ef34abc8f8302675fa051e04d2b0db7995a024a1f4298f5a462fcabd0d`  
		Last Modified: Tue, 23 Jul 2024 03:54:35 GMT  
		Size: 175.2 MB (175246775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6bf27a78e3cc626d21dba8d100dbb9a36e2baee8376366e7de7192d12a7da59c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282981788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b588c5bbdf1d403f11c3e62c2563ef328fa139967a225442d867cb171518dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7dd73ef69a71e0df94b32b858c9f24073577ba71f5b1051153a44ccde294a5e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314102222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca99d083a4ed5bd7e7677b36202282952a95d2e9802e1586fec6be0276244d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:53:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75f0ece8974d005f2532701f9fffb099d09a9bd1a53465b796982e4c2f594c`  
		Last Modified: Tue, 02 Jul 2024 04:03:16 GMT  
		Size: 189.9 MB (189935947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:93260457ef10b0b3880d788d8e7a4a2a1f7a5b88822d15a2d046489e85d420b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328213978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0a13798ca5638cef17990e78215ba03b311bf89ce25f0d2dac91a2c5e393d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:43:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30928a030df8a953adc83c67e2ab17a4c5048cc04287762bc9e03e269fe7c3dc`  
		Last Modified: Tue, 23 Jul 2024 04:51:04 GMT  
		Size: 199.9 MB (199944219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90707d07e88c5456e10f0504199636c1e8de85352b20db5391157aa8a573bbb2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301517721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c2735c637f37fa7ccb5acf1d0ec690e6916d35eaed079a0fe45605d74a5aca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:39:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99842c367e8366da5cce8062955a8adc51f02bf39119fe6c706b6971d2a9d218`  
		Last Modified: Tue, 23 Jul 2024 02:02:48 GMT  
		Size: 53.3 MB (53311607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18848575707cdf418cce9d480db3e082d823f30e54ae921840643faa7d52a14e`  
		Last Modified: Tue, 23 Jul 2024 02:04:47 GMT  
		Size: 179.2 MB (179160971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28b7060984a9a006e31c0b82fdf3b4b02404fb351512878238b54e753ff9c7b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330989547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ecbd4e6769fe22daa9e42e241ebba651c7dbd72ad9d14ca138f4e7df9a1f2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e81e7819bebf367f17dbc683fc34c6aadc4158e9b6b05cba1a4c966f077d02f2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296099464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed3096195a0e5b0ecd4d9873a4d0b50f8c7665fb711f4c3738969baaf1b57c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:79ef5da615c4aabe9c8b65081d6f59846ce47101b294949cb49fbe9268b0dd06
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
$ docker pull buildpack-deps@sha256:a504bb2cc4019727fae50df881b8bf5ecb5514e79daa53179da6056f57a6401d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba75d7cad2670b5207d207623743c4b2b2c437726cdeca5f6f3fe17ef78ed2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eb8435553af2ce9919814f08faf602ce03fbe0ec9b5724266dc68e907ea42b49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb193bd8f4c63c65ee9227c16f9d7a483161a469ccf530a8c88c258a9254be2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:34982cc2831f44918cef0bd5cd34ae8b96f2706e617bae9caf68a6acd96e74e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65122020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9c594b42a25d0f6ed9f5f895af4f5ea2e52bf56e17daac70f14c13f112079a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4bc65dbdf99b85e1d096a0b5fe82b7e18e999520ad8326df8dc8ef225adab48b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69471218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe19f2cd286b38892de1f8a24683cd9aec0ca038b7058f752e0298ab3262774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:167054572b59412b36ebfe3b4eb40d3c86c4452ada800413c5ec812f0f6973a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d426404e66e09e52514300bbad7094e621048ecdd787582e9911ee078f8f1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fe1a8cd7f8e57bf72c67bbc2f30188367a8973caee362c8418646c43103540a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69045143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff7e128d711d5080cdfb492363b6bb11153bc1b4befef6c3e2e3318f597daaa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:446c4d72ab4ad87a7dbcf025a258a2f642ee39e0712060c917936192bf940eaf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ea32ed165cd42a1567b0f3b4b216122c7b0511c2a69b04c57d10a6f49d2081`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a174b73fb0d4d8958dbabd27c12a350813aecb073857b648794b226c82046e68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68965812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3210584f000afb879f87d583b2703d804c1add30b83c9610f1095ed1f7ce6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:23ec434d35fd158825845b9d0b0e3108f21c7aa1bef4444082274392677b755e
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
$ docker pull buildpack-deps@sha256:69d36ad13ecffb8dd51412c7579dbecc4f17f661dd9fd8857c14875fa43c95c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125437401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfdd900dd285a53a5afb08c6190630059edec24d4d75b3bc125b723de69ebcd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d22f58ffb9427c05e97e6462a1b3385feb8d7f61143e82ca06fc8afc50d88096
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120294009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd7a259fbd58722024f4504fe24e9f1bf866bb69095de420706fa88ab53c2ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:41:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b062df9eea8fb3b005e76c03f7ef72ba9331888f68b2b9dd6b1f7afaddd042cc`  
		Last Modified: Tue, 23 Jul 2024 03:53:50 GMT  
		Size: 52.3 MB (52329700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfaf01a3c00dc625c6f22ee3e0a942a8e0f9577d3166ade3c3086f20dfbbf645
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115479818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0323fb2c99dcde25333251776876e1dea9c3585e9e3fa81040ac9d49edfd7b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:78a1705430080aa1449064e2437d48b39c14b54085a4dbd017e06b336e846b7e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124166275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71dbaf9643ff77b80b3b18db7dea38a1341cacfaaeedbf094d402d8947695c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fc507dd2c0ae791a27569c497f2750526f3fbdababe837b3ef1e1104444858fa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128269759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebfd400e18099c87719624296a965748d8640a394cb9395e431379460bbf19d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7c158891bc067ee9459ab34e03960b31f256a5841c91ab1c25d474663c1fdb73
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122356750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451b4e177fa1a4e8c432f462a9a1def547ea1da5090ed6ca90715d446cc6b405`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99842c367e8366da5cce8062955a8adc51f02bf39119fe6c706b6971d2a9d218`  
		Last Modified: Tue, 23 Jul 2024 02:02:48 GMT  
		Size: 53.3 MB (53311607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6d5be2179353f4ee7aa2378890b84a27085d33d98ead9e6f493567846e90da08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e071c1475ac021ffe4b1dfc80f52e92321ab7395ebcf2491166490edf412f38a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b4fb3f45bf0497cb7da93e1e5f88cab03e0ac0c6f552b9ed7f3a23d433ba6115
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123041107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a010209e7a82320af74aa73e24fd4954556e0248f6588f002eed4a7dac0df82e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:6976225849ed01372fe39066d7fb17c36ccffe53b6278886a5af525265e2afc1
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
$ docker pull buildpack-deps@sha256:37bc82e1ffaada99675f7c27376608cfff5fb56ae24fcc19756296dfe72405f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462d4a80b845e56a63fc8715d615dcdfdf198132ea93f5ad29a7ef236dfe7ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ead148a14be0e2afbbd64a5d75545bdbc67d5e495d64a0b0dea93bda62a8ce65
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131570072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcbd3cbc69a70376ad459ba896d3c18d643b49949a8d1af3d137168be02d2ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d2d65254d091265f939d4ef9a5c69f4f96bed13cb391222b43663acabeea0e4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126325600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27630f25b34b76a6ed40de03ebf679bfe86c39dea5e799983ac8f182a9c2002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef0610482c2e5909b3035c731b58fe4e0e92503aa55184971b4c76225a1a6d71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137174230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8237381f2e62f9c64dce46304e239cc2525c498fa324df76649544daabd946`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1e53076e757e1a41fe591c7f1e4e7a73884ae1bd0ccb718c22fef1bf4e4dace8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e116de79bd7590d0d53a2256e2f90e344e581ccdff8df85ed6c35ed1b99138c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8a04c418d221f88c661ce9fe8d82e529a1defa8a456c524b5f43de0297711bef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d65e857df7d381ad6a1edab761c02e89f343484180e7d10d5fdca547f9dc7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59fad96d845621440d0ea25364fecb6fd032c65ce53b07df77cb6b3d3c51b1ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf5d917a1d1b050133d4e48093febe11d2ea19d61e4a1cab54dcb39dba62c40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af65546aef0be20475bd81e286ca22b7ec1c1f436b29f08a6d94103f81830110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06da605e1e080ed7ee6281acc3ff42965cadd025807adb75473222af2c8c21bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:602c67cd2a3a2cea8f4f233ad277d063dfc2018680db313ad6d03b9934830263
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
$ docker pull buildpack-deps@sha256:6d176259c6b7a34bc0adf35f30ab267d5391c3149895198e79897c2508991866
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.9 MB (356891688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adea96ff5bbbe3d2cf37062cdb0220b675cd88975454fab80ca974dbc85ab5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a88954649deb248d6fd991fbff086ba12beaa2049bdb4f71a1a86908a6d06`  
		Last Modified: Tue, 23 Jul 2024 06:15:29 GMT  
		Size: 66.0 MB (66023447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea56e91006e20d1258408621b6da0c46533963c358da290f5423b1d1a55dc821`  
		Last Modified: Tue, 23 Jul 2024 06:16:03 GMT  
		Size: 218.8 MB (218789325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1681bcb26b04d6e7008b5553e6277ceb5413f1509b573713cbc2f3e3a9a635fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326235431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716998cfc77e470a5652ecc36e4a16f8e9530f004f2948e545e809f5e3367c9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:48:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9873310e83bd2c9cddf329c78833d832e9bbd909cf26e632b676e3b31b940`  
		Last Modified: Tue, 23 Jul 2024 03:55:11 GMT  
		Size: 63.6 MB (63564737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982638bae6423bbae98e0c502921f436b34355d3d4bf030c2252127b0c30dfbc`  
		Last Modified: Tue, 23 Jul 2024 03:55:59 GMT  
		Size: 194.6 MB (194599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b6cffdded486696d01044be124faf6afefa35c28402259fab0949e106904e28
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308055812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eead025bb596ebe6cd8def784662514169861219bea83d20c391d0d27e6a9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:43:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530b2c70788d78360d3f365fdef0a3a385f75d30ac92e588df91acda5d06910`  
		Last Modified: Tue, 23 Jul 2024 03:50:00 GMT  
		Size: 61.0 MB (61013856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f4bb1861e73c2193c46843eb11525964345067e7c1f80c54e7480ca0853eea`  
		Last Modified: Tue, 23 Jul 2024 03:50:46 GMT  
		Size: 182.1 MB (182121659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b45c87615bec35fb193846411480bb3fbf2e3405f8a70788966be99d98a5b49f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.7 MB (344717348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42c69deab6111c8cafb2fd66bb05974b6aeed0b41e5f2eaa21b16c92cd9da7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:55:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b13905653e52085cac0034a182fbc6e1096638d960653d96dee8be2a517342f`  
		Last Modified: Tue, 02 Jul 2024 04:03:42 GMT  
		Size: 66.9 MB (66940858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe043a6ab3915a1c9cd4aca34966c52c7162e40fae409638a34baa845fa99`  
		Last Modified: Tue, 02 Jul 2024 04:04:09 GMT  
		Size: 206.1 MB (206123380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:84886c9650d92c3b6aa8e0bf2cbf8df5e237e815d0e5e991d239e2dee62c22f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 MB (360049319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3f66fbd365e52553315d162563189082e7b6321df23366fe5364e288cf7ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429258c06093466c9fba74ce4846613a377ce78cf008d521b760c5170697024`  
		Last Modified: Tue, 23 Jul 2024 04:51:38 GMT  
		Size: 67.8 MB (67826201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83348b487e8b0fae77078e8fe8aacc19153613ee80154985d7004b2189853994`  
		Last Modified: Tue, 23 Jul 2024 04:52:23 GMT  
		Size: 218.2 MB (218167549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9028c225fe9b65a98fd81e5ad4b28ac2aa5b828cfb1f98ec22d39a175a306200
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332195395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d78f180eb1b796ab7aabca6af1df31c1b12f369e9e02d0bbf4a30c83c099656`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:49:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf5f50c37db38e90a50520c093b6fa2939d9fef5a62895ea90c91d02dbdeac`  
		Last Modified: Tue, 23 Jul 2024 02:06:02 GMT  
		Size: 64.8 MB (64814442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990154075f1f9e5c156fcb25dcc580ad4535cfc9df883915675c583a91f37a59`  
		Last Modified: Tue, 23 Jul 2024 02:08:16 GMT  
		Size: 196.0 MB (195964609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c18683a7b2e4a08a201c00bc455b420cb3bec97f5445c87e0b7b123a70689b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362845834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6421ee50a6f14c7c122aedb9c7582332b0d3a46aed1c235bb3fc86f978db3305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:37:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b98c88f8a6ca27a89215004b3cdac4fa255a74553ee93c0bb336155b16701`  
		Last Modified: Tue, 23 Jul 2024 02:44:32 GMT  
		Size: 71.4 MB (71413135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632e7382e9bc8051ac63dc520d51f93484e2c1c8f3c624baf6d2a99a37294f6`  
		Last Modified: Tue, 23 Jul 2024 02:45:10 GMT  
		Size: 213.4 MB (213409348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8fe7dfa1ba06d87a806cb93752c9e8224f1ec001816ec683bc3d8983b3b8b23d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 MB (392052260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dc99285208332856ca4f86ba0c2e095e5e6ad46644908ef457a9e2733717b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:17:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8a525751918610936d3d7c2f56948a95908e5fdc97875a13eabf5b5755181`  
		Last Modified: Tue, 02 Jul 2024 09:18:58 GMT  
		Size: 66.2 MB (66196372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d148814d72aaa345d1ebb818dabc2c064dbd11ae389facc1be8b9b7c3f8b5f67`  
		Last Modified: Tue, 02 Jul 2024 09:23:36 GMT  
		Size: 256.2 MB (256224615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:104b8641b7f47fbc3c0cf767a00a4df89cd675e96ec4abf2fc9bfcc2e2b5b392
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334266471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8581bebdd6dbb28f2b1f3ea4479683d449a04d2392a92133ae50fad25c8b4072`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:09:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:10:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b90812b56a031f8fd0e591290e9252f35ca6f8f86d5550448fbfcba2c2560`  
		Last Modified: Tue, 23 Jul 2024 03:16:20 GMT  
		Size: 67.1 MB (67066609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3711122f465e94e5fe0e07180db63aa5750b29edafa7e72d91bbd960a4724a29`  
		Last Modified: Tue, 23 Jul 2024 03:16:49 GMT  
		Size: 194.3 MB (194286348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:1c72afc3f7316b9452024d33fa62de29b136b713f8e51528076b39baf8c116c6
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
$ docker pull buildpack-deps@sha256:c506c9a4be6710ea11f6f9e651b299b2923321eb160bb25bf1d1e072cda99e99
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72078916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f91c17165e09e37563417b4384a281bd5f9a34451345ed1e380530c62e936f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6b5b91dd8563b6c83f9f292f47b4f4dbe9be84f6e6132701121dc0133e988f57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68071420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b80c1c593db8ba05c984a51879cef29a28366f43e1fb6396f1eb08e2ab6422`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfa97ce73cde95032209696321352612680db764c680a1b0951f78188c543fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64920297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9f5d5f12b39b29e168914b6f8c8975fdcee316b9e697f402b0b3c5137032b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:565aa9075ce6be708b8c521144ae8c1767a8ed5942f3f8b1295a4493b60f0a57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71653110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf790b8c8dcd40de930e7bb2cf6fc241552c0a3335cb4b13d3fb229e4becf95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04c2515d0b3ac31ffd91e42f38e369e1bff2641c2728fd0621aedc407df1b678
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74055569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad98ccf705d644b38203f371bfff8ec7f09a2c081edea59d84db557b6519f68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e7fa6ef8eb669a3a49a45a66f8cc69d7f09d1b83c63555825932c55ae4e2220
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71416344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfba9f25abc92be9a113bf2def9775d340036cb7b23d08e40a068554fb1d56c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:597bffbfd546b0553a21404706d32d58cb0aff05e5d1c007c50f45820a980671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78023351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e74849ee887deb1ee055850655ecbc96c46bfe4cdabff05dbcb2e34bf9a2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0ceb7dfebed647afc7aa3a53e3a91dc13bc962c18ea18a6febbae1ca159fb643
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69631273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0d285c318a8b4b87b73abe2d0dad0afb0f59bfcbea02b03781a46a17c7e4e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1fbd779f4eb589e092c27e36df4ce7691bba7800c279e8aa9588ed295da8f17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72913514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30203e2370c0857b26cbd63c6d17b0d5cb59f4f69da9eca5b30f41fc7f5143eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:3b2ef4e261459174b8e6f46108a757382681007fb4e8f86639082b968ab77a45
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
$ docker pull buildpack-deps@sha256:871b92b67481317387e09ac213f279b8fb96059446e3c7d40bfb5bb5148d8013
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138102363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf3e8f9d33353c4f56ccc19c5eb6ef5d3d9ced7c1fd41842802f454f5fa3f92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a88954649deb248d6fd991fbff086ba12beaa2049bdb4f71a1a86908a6d06`  
		Last Modified: Tue, 23 Jul 2024 06:15:29 GMT  
		Size: 66.0 MB (66023447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7177a05d7c22b3a9b2d05a23d3288d53fafa60f977a3de046d93d1e3294a97e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280ebc938aa661d553a0d9eb668d100e4f218a67504cf709cbbe6430f396df51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9873310e83bd2c9cddf329c78833d832e9bbd909cf26e632b676e3b31b940`  
		Last Modified: Tue, 23 Jul 2024 03:55:11 GMT  
		Size: 63.6 MB (63564737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:39c7d006924dc193dc2f5d78faa3f1d17c7e9aa6b3a182f32f75281bb942dfd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125934153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87e3a737cd11656c9a9dd1ce82646005ace4c4e66d8a1d15916c59c8511634e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530b2c70788d78360d3f365fdef0a3a385f75d30ac92e588df91acda5d06910`  
		Last Modified: Tue, 23 Jul 2024 03:50:00 GMT  
		Size: 61.0 MB (61013856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:743a0ce5bd6cfaa274351397485f81aad864345a0c13926d220cdee4eb03b940
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138593968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc61761d538deeed0142d5c59ceecc4f78dcfcfb450e7f4089f6ba36739de0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b13905653e52085cac0034a182fbc6e1096638d960653d96dee8be2a517342f`  
		Last Modified: Tue, 02 Jul 2024 04:03:42 GMT  
		Size: 66.9 MB (66940858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b56da467efc94000547dd9034462b8d9f943b11fc6f30c64478fcbed11d40b37
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141881770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605124dff5e3a0fb6f298d2b079bfbdf70edf727e979fdbced8ab337e4cc7bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429258c06093466c9fba74ce4846613a377ce78cf008d521b760c5170697024`  
		Last Modified: Tue, 23 Jul 2024 04:51:38 GMT  
		Size: 67.8 MB (67826201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15334f31455e132e2262d1167e932c92d2a60b10f7557b753356d655eb6feac4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136230786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf6833d7529096fa1bb3815fec2f0d0ee573811115caa84d9329959be919808`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf5f50c37db38e90a50520c093b6fa2939d9fef5a62895ea90c91d02dbdeac`  
		Last Modified: Tue, 23 Jul 2024 02:06:02 GMT  
		Size: 64.8 MB (64814442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fa91f7fe251a3e3a6e112335750dfcb83db9277a82a5fa58b45ecada4ffbfcae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149436486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ca1609d70f49394d680d1e00297b69c5471c813ff5070bb5360ed09c502aa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b98c88f8a6ca27a89215004b3cdac4fa255a74553ee93c0bb336155b16701`  
		Last Modified: Tue, 23 Jul 2024 02:44:32 GMT  
		Size: 71.4 MB (71413135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f96cb4ed9d65bc2f134e70ec4ec06cbd5c85b4b0504a225cff4315ed8c8227b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135827645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bac5dd12e16d55713e1db5e729f29cde5ac97748d2c50c3398cacfd525a733`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8a525751918610936d3d7c2f56948a95908e5fdc97875a13eabf5b5755181`  
		Last Modified: Tue, 02 Jul 2024 09:18:58 GMT  
		Size: 66.2 MB (66196372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c8daa564a12c68f5fdd9e98aa37893e0024a408aa9ee724e7d2bb44b70fea5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139980123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5535b3ab8cc246f97a1fe491db849a94bd5948200d49ca2d576954535f4ec275`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:09:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b90812b56a031f8fd0e591290e9252f35ca6f8f86d5550448fbfcba2c2560`  
		Last Modified: Tue, 23 Jul 2024 03:16:20 GMT  
		Size: 67.1 MB (67066609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:a654d52e4608eeec0b8d6dca760d413fe31317b6fb8183f7c68c149b7cf96e16
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
$ docker pull buildpack-deps@sha256:96aa4125d8f866a6785439835e61cb499edd11adc09aa9a62ed339a802947543
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348989680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed840514560ecb23da04a87e26e68226347cd0918f03e72a626ea1de94fd456`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:07:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dc1019d7935fe82827434da11bf96cf14e24979f8155e73b794286f10b7f05`  
		Last Modified: Tue, 23 Jul 2024 06:14:07 GMT  
		Size: 211.2 MB (211241610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:75f7bcc90a107ae0a8c7d579a00e36db8d3f92fe9ad0004a7aab4ee3dc835388
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55ad79738158b9b559b3a6288f599b973b8d833c9853056b0abfbb42a663986`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f383f84306b6f41c3ed73bdfceb22befd854a21432eeb20e66606aa7f0de1a3`  
		Last Modified: Tue, 23 Jul 2024 03:53:14 GMT  
		Size: 184.5 MB (184529578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b700c1d49e1f79f868c5189c14f66db5cdb8704cb0537f367d7b9a1a9062563e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301508491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec96321e5eac42f04632d42f615ae2a2b80b43033a1e83898bf7f42ef0868d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:75647bbd8cd18fcef825cbf38b3481b77336c708c0b01dfde68160a54d253329
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339785031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbf3968966835222500849ac2ff10413acfb4b7619efea0037b113106497938`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d03d80f0fbcb18457424c859d43d6dfffc35d1c45e5f23b15020e176392f5828
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351616214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461ad229eee29e7dc604ca63e86ee7e94aa4f774d534ce3feede24a6067a99d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4a7c31652ee354c7323f3315523d185b07416d8cb4bc316907ce5389dbee90`  
		Last Modified: Tue, 23 Jul 2024 04:49:51 GMT  
		Size: 210.2 MB (210156525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5594e02abeeadcf7c3da5c425498803af089369c7c29f9364df5e038e9f0a83f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325970317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c681e16b27e6af6e089f0cc788f13d8603dbc1667f2f2fd3017f34a437c262f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:31:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9bf98f8625482717f751cc9795fbc191bb19c8a1b474435b13be58561da0b`  
		Last Modified: Tue, 23 Jul 2024 02:01:39 GMT  
		Size: 189.8 MB (189804860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1bc97343130aa4ba3f5649e57b64b8993e7826e9e406e70115c4b43d74f75736
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4919d10ea191445ba34fdf226173f4528ea1d10a1282b0a48731e4f63692a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:377884cf88179e14c6ff704b53232cf6b55f3eef045612a04ac496fbf1eebf4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318370734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797108ba88070ce02961f0112d95ab47909ee25ec71bb86877aa6a49b66214e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:bf7e3a7f11e5803e1ee3d143d1f4324fb768d6287dfe0a167992024eaa71963e
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
$ docker pull buildpack-deps@sha256:4216ba7e789db813eef27113ffc0e7798f461f316bcfa059615e2920b54d7b86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73604871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499bc7f80746cb842f582a9553c7c763a503d471e561ce5c05e1f2a23097e6a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d2f44c22fd4532965fb02333473e85c6d3ab86609da43e49d723754abe3d1427
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722b23eda8fb4d3431b7031cfae4c188bd177309d8390d5b4e53e97e3495e498`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:425da63e21a8968bab7eab3050f542ae6a46e81ba6972b5aa4198380192c407d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67102785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0795e70b98c0048818600534dd4db827d5f7683f4a675ce9e2b8f51cf5a89d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a8155f724f1e6e368526d3793b1e62b186bc19d14d3bc9017ac2b29aa075cb8e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc5c4b620ecc5a3f564f49bbc825a6843e429303da6ec5de922ca9a2fe13fe6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64b00994df20baff3673b688e5ba2e439f5700e377214e45416fca94433fd7a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75470882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b86e5b7a2525a74ba3a1b1d71faffff73e72c5eed68cfdbecca4a70652bba3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:59005510b61f0f0ef977e4f2962bab45b50e47a53845aa5cc1d7786d44a5ada4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84595c9eabc4b54f273d65e511c9cf48b6e5d6e8409b6ae5813074faa4797603`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44a13b4fd2ecaf87d3361e50327286868a7ff3b7a41b6e877c1b5e4b22990de1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3cedc1cf1f38c69c9e9ccb44c8ddcdb8c4513da74fdf516f7837f69ad38b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6b42e6b8dbdd9cfe8f865b7b7e3f24f0c902f08fad4f5ee71ad91cfc1eaee04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13456429367f068f0a2cd22da31db81103299aa4b4714e95244a0eb0a3defd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:6976225849ed01372fe39066d7fb17c36ccffe53b6278886a5af525265e2afc1
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
$ docker pull buildpack-deps@sha256:37bc82e1ffaada99675f7c27376608cfff5fb56ae24fcc19756296dfe72405f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462d4a80b845e56a63fc8715d615dcdfdf198132ea93f5ad29a7ef236dfe7ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ead148a14be0e2afbbd64a5d75545bdbc67d5e495d64a0b0dea93bda62a8ce65
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131570072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcbd3cbc69a70376ad459ba896d3c18d643b49949a8d1af3d137168be02d2ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d2d65254d091265f939d4ef9a5c69f4f96bed13cb391222b43663acabeea0e4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126325600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27630f25b34b76a6ed40de03ebf679bfe86c39dea5e799983ac8f182a9c2002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef0610482c2e5909b3035c731b58fe4e0e92503aa55184971b4c76225a1a6d71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137174230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8237381f2e62f9c64dce46304e239cc2525c498fa324df76649544daabd946`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1e53076e757e1a41fe591c7f1e4e7a73884ae1bd0ccb718c22fef1bf4e4dace8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e116de79bd7590d0d53a2256e2f90e344e581ccdff8df85ed6c35ed1b99138c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8a04c418d221f88c661ce9fe8d82e529a1defa8a456c524b5f43de0297711bef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d65e857df7d381ad6a1edab761c02e89f343484180e7d10d5fdca547f9dc7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59fad96d845621440d0ea25364fecb6fd032c65ce53b07df77cb6b3d3c51b1ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf5d917a1d1b050133d4e48093febe11d2ea19d61e4a1cab54dcb39dba62c40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af65546aef0be20475bd81e286ca22b7ec1c1f436b29f08a6d94103f81830110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06da605e1e080ed7ee6281acc3ff42965cadd025807adb75473222af2c8c21bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:96e3fc28b2763eac4b370ce143227fac18fb612c4181fd04a85cb53780cad062
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
$ docker pull buildpack-deps@sha256:b006b5e15bf4032eed50c971c62aec789fea8fc5717f9e5c987a8548190955c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357209185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8d94b8a6178f22e0459e8669a894cc7203f9ace0b33f4bff125e11f09733de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:12:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb2782ec0c8f6a51d6d35106ecb2c6dc20884f4733b1236af9de7260944277`  
		Last Modified: Tue, 23 Jul 2024 06:16:29 GMT  
		Size: 65.4 MB (65410843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07c89ce659cfb84b0c460c4260986b1fb669b25c5d60b77d01039830100b514`  
		Last Modified: Tue, 23 Jul 2024 06:17:02 GMT  
		Size: 219.7 MB (219681492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f16dd90fed099bbdd38c9ba2b4043c2f6dd5fff753f8e83efcb01f53c54aee5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340730804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e1602b1478c15c9a4d7e0895ad2894d4d31414497f18460bc450208deea5af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:51:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3995f67f100684b8a4349bea104130c9a88c087b6156a290542809abaf92fee`  
		Last Modified: Tue, 23 Jul 2024 03:56:39 GMT  
		Size: 65.5 MB (65524112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e5d20634a81bc4b6c92c003ee534fb6e97c79718d23d099b71e138a19b8e9e`  
		Last Modified: Tue, 23 Jul 2024 03:57:24 GMT  
		Size: 202.0 MB (201988970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77e38d7aa99a2e0cb7e262cc703690c283c00862288360178c22022695df5b0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321697298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032c751d25fd26bece446525e54e6934ccedf99662f558a6584db2e9ca8d68ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90386b6142530b1ede165d6dd3a0cd162bcd3ddd68e43f48c8f76f8ada03618`  
		Last Modified: Tue, 23 Jul 2024 03:51:24 GMT  
		Size: 62.9 MB (62860451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2ab6b90f24721261dec59e268b9ba45d61a39ab16580eb2fc884cc1af4ac2`  
		Last Modified: Tue, 23 Jul 2024 03:52:04 GMT  
		Size: 189.0 MB (189038149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6946b524587fdfb8804d74ca8c7297cde64dec1c55682cbfd8654cf38fcf8b26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344812580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c228b9102c2cdaf53fb665c93f639497a8378bcfad99bb19f86a8f245fe6937b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b366a841875c380bfef184d661cc1ce4751b4e07e9e2eaaf6d0c55114a91de`  
		Last Modified: Tue, 02 Jul 2024 04:05:03 GMT  
		Size: 207.0 MB (207001748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b55f5fa2e52d1e5f02faeb6421fc0504f6c89079a0349b4a9b8f3a55e6fb126b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360367038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf488d33e1aaba3de18374b95161a57c7954c7a8e0748fd2375ca2b79275512d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:48:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908527b139d9269245a4259635b1caf76393575aba5a1f4650d84a199883a1b1`  
		Last Modified: Tue, 23 Jul 2024 04:52:56 GMT  
		Size: 67.2 MB (67169878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef45fd5d95eb76e975ce6ad7fc757f1f16d9221d52553ce276767b054cf300fe`  
		Last Modified: Tue, 23 Jul 2024 04:53:41 GMT  
		Size: 219.2 MB (219161545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:086ee42fd7bfcbcf3a180d3a1fb8cd492372909dca9ac35acf6f30908f5d6b98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336180671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9924d6cd88082f4605e70e21cbb36a72f69d506bf2427203ffbb64b4af9841`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:57:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee36f9299929b13c64e8d1dcbbecffbc23ec614ec5279d3468b3cc790fe0439`  
		Last Modified: Tue, 23 Jul 2024 02:09:30 GMT  
		Size: 64.2 MB (64222016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4466f890a1001c0f56f2d169603e31a1e4180b6e1c7a95244e03020c696c07fe`  
		Last Modified: Tue, 23 Jul 2024 02:11:46 GMT  
		Size: 200.6 MB (200551501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0231f23e687071af6193d3f0efe7be3b212b3ea430c78ed6f8239d66a92b110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370097457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1fa43090877b8dfc38d6d93cdb85f0bae92c5bfc0a34b06b25c9908342eb8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:40:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aca4b63ee1a3a6c2c0c85f637c9ff06323c852e1a5363d3eaf9b36ec6bafd`  
		Last Modified: Tue, 23 Jul 2024 02:45:39 GMT  
		Size: 70.7 MB (70683207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0b716eafc6c8d8353c17c7c5d4fab52f3e2e2faa1180bb4d0761b66a184629`  
		Last Modified: Tue, 23 Jul 2024 02:46:18 GMT  
		Size: 221.4 MB (221396731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b82e36ee67e0cb1b63575257de321a356d70d95f7859923b926ed40667d7d01a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334590501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34de17661113981e29208c56c9e5a0c3adc6da76e0f0dde5d6b1ea77592a668`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:12:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13abee5c4577fc2e5e5ccd45eb4abcc067e815317edd4eb7fb89c6b9ff137b4`  
		Last Modified: Tue, 23 Jul 2024 03:17:12 GMT  
		Size: 66.5 MB (66483586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b246619b57093ef2ffbfca7ad46965ab0172ecaa73b81ecb7f975cf22e368de`  
		Last Modified: Tue, 23 Jul 2024 03:17:39 GMT  
		Size: 195.2 MB (195213514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:507533448f9d2e1cd93485a961771ea1f19c87cae1af33ed57b096f1156de25f
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
$ docker pull buildpack-deps@sha256:db7e1584702e2ce2c1843e73785ea850b91f22b67a0057a09fdef7e43de922ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72116850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbbda00da917e7c15e5ae572efa6c80ac276fd353d004993e53fb8b8c27c91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:db1f5252158b47f3f9fa5ed5624b494ab78c51d4463b03f107f133fbb5ea5f49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73217722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b039e1e67b088cf0cd7c850addcf872710e237ab7ea3dfa3aaca588c77ac4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f9dc952f28f4f4fd3c026313044d8143b61e1b9866c641dc75f5fc704e353656
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2989804b2d5db3e6028493ab7b4716ed548cfe707075cba70ebf5708623bf36d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7e59002f0c5a17bacae57287d22ffb537dbdad7313e5584c0587c37995b68dac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71456321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0958582e9224f89984a38c8702208aba470365a870911c829cd325bf7962df7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cccd4bbf4ceaf8dbca6aa841b6acb4b4d23f4ff686fbed7962ee9e81012c58d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74035615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442401ad9c62f629aa9238e9a3a47f7d55640fda00a3ae58c6c0958692b0cb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0f420425a3e3e552c0a70a1c436e26f5e2e750c3914e1b22d7fbde7af0aa2873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71407154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f58ed6eff53d376e39f4903d043d43b4a3d17e197634c8e49ac79add3e8172c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e5f97fe3f1a48f9e4aca45af9b3b7e87ba798a8ba240471261f529a919152f52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78017519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebba4d5b7f38f8bf724f7d03b2866b7ddd69981687a27b688571964bc6e68e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:89d1d494114c9c2f0f75857f06665f950ca2720c93062acc91e730f6fd4a4173
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72893401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f6498b1cd64a3a88462fec2b32b0c627d87abb7acfbaf75d585798ac49973`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:3406980511592ebd1ac32d131458cfe904552a8f7bc901be92ef196e20d973c3
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
$ docker pull buildpack-deps@sha256:079424468f0eb509ef049deee98b5cef0b9ebdcea733b003cd7395bde02700b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137527693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4fd31e466aae2585a1c45186ec7693e0f6c4d2da23cf32fd7488f304f3715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb2782ec0c8f6a51d6d35106ecb2c6dc20884f4733b1236af9de7260944277`  
		Last Modified: Tue, 23 Jul 2024 06:16:29 GMT  
		Size: 65.4 MB (65410843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d0191a2b3eb5bbc58aeab05f297127fa46c0883320291916434150c83e955d23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138741834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23a8db2f6fadafad6db8d02d01b62dc2151f0380773c96f655321756d8446a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3995f67f100684b8a4349bea104130c9a88c087b6156a290542809abaf92fee`  
		Last Modified: Tue, 23 Jul 2024 03:56:39 GMT  
		Size: 65.5 MB (65524112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:63f39701455c7b52b5afc3a4dbe8b79d58a527e2f7b96be64eb0eefb2c93942a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132659149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbccdac0e820af648947deaeceb9fc4085258cd537072d2a68ed494ce72573eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90386b6142530b1ede165d6dd3a0cd162bcd3ddd68e43f48c8f76f8ada03618`  
		Last Modified: Tue, 23 Jul 2024 03:51:24 GMT  
		Size: 62.9 MB (62860451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:879cf292ca55f2dac3f60d1ae87c900d99a880b17f984e3cea0f803942fb91a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137810832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a97ec39812e39e1c687955dc4e4357d504033c6bc4b60b658da73fc4fb46db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d923d1db8297e4b85a34a97bc7d75b03fe29b101ddb7138fecd879a6ebb4a9b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141205493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6af04ff871c1be2747f0f54793aed4b11296e5872e9eecd576d860f486361a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908527b139d9269245a4259635b1caf76393575aba5a1f4650d84a199883a1b1`  
		Last Modified: Tue, 23 Jul 2024 04:52:56 GMT  
		Size: 67.2 MB (67169878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6228088f3891510ab445efe6f056342d9a805dc01b753b8872d499908cf34828
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135629170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75ea010fd80caa8f1bb20778ef586a1688bfe15b745ebc58f17bbcb5ed3702c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee36f9299929b13c64e8d1dcbbecffbc23ec614ec5279d3468b3cc790fe0439`  
		Last Modified: Tue, 23 Jul 2024 02:09:30 GMT  
		Size: 64.2 MB (64222016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b9c22c11ce24f944e5ab6db7b108c9dc0d66620bc8a8b16ac2b1992ae0c11f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148700726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a6cd597306f829d3ed16e8c3b4fd9ca4cd5a55945dec1e4c5840820b52036c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aca4b63ee1a3a6c2c0c85f637c9ff06323c852e1a5363d3eaf9b36ec6bafd`  
		Last Modified: Tue, 23 Jul 2024 02:45:39 GMT  
		Size: 70.7 MB (70683207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6329d78700cf3032add31025f8c1fc5a855f016d94dab2742cf438bc93f333e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139376987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb065e2e54ebbee952f3f504e0aec0e591fb660cb8dd576307932ab4d75b050`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13abee5c4577fc2e5e5ccd45eb4abcc067e815317edd4eb7fb89c6b9ff137b4`  
		Last Modified: Tue, 23 Jul 2024 03:17:12 GMT  
		Size: 66.5 MB (66483586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:96e3fc28b2763eac4b370ce143227fac18fb612c4181fd04a85cb53780cad062
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
$ docker pull buildpack-deps@sha256:b006b5e15bf4032eed50c971c62aec789fea8fc5717f9e5c987a8548190955c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357209185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8d94b8a6178f22e0459e8669a894cc7203f9ace0b33f4bff125e11f09733de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:12:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb2782ec0c8f6a51d6d35106ecb2c6dc20884f4733b1236af9de7260944277`  
		Last Modified: Tue, 23 Jul 2024 06:16:29 GMT  
		Size: 65.4 MB (65410843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07c89ce659cfb84b0c460c4260986b1fb669b25c5d60b77d01039830100b514`  
		Last Modified: Tue, 23 Jul 2024 06:17:02 GMT  
		Size: 219.7 MB (219681492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f16dd90fed099bbdd38c9ba2b4043c2f6dd5fff753f8e83efcb01f53c54aee5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340730804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e1602b1478c15c9a4d7e0895ad2894d4d31414497f18460bc450208deea5af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:51:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3995f67f100684b8a4349bea104130c9a88c087b6156a290542809abaf92fee`  
		Last Modified: Tue, 23 Jul 2024 03:56:39 GMT  
		Size: 65.5 MB (65524112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e5d20634a81bc4b6c92c003ee534fb6e97c79718d23d099b71e138a19b8e9e`  
		Last Modified: Tue, 23 Jul 2024 03:57:24 GMT  
		Size: 202.0 MB (201988970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77e38d7aa99a2e0cb7e262cc703690c283c00862288360178c22022695df5b0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321697298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032c751d25fd26bece446525e54e6934ccedf99662f558a6584db2e9ca8d68ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90386b6142530b1ede165d6dd3a0cd162bcd3ddd68e43f48c8f76f8ada03618`  
		Last Modified: Tue, 23 Jul 2024 03:51:24 GMT  
		Size: 62.9 MB (62860451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2ab6b90f24721261dec59e268b9ba45d61a39ab16580eb2fc884cc1af4ac2`  
		Last Modified: Tue, 23 Jul 2024 03:52:04 GMT  
		Size: 189.0 MB (189038149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6946b524587fdfb8804d74ca8c7297cde64dec1c55682cbfd8654cf38fcf8b26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344812580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c228b9102c2cdaf53fb665c93f639497a8378bcfad99bb19f86a8f245fe6937b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b366a841875c380bfef184d661cc1ce4751b4e07e9e2eaaf6d0c55114a91de`  
		Last Modified: Tue, 02 Jul 2024 04:05:03 GMT  
		Size: 207.0 MB (207001748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b55f5fa2e52d1e5f02faeb6421fc0504f6c89079a0349b4a9b8f3a55e6fb126b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360367038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf488d33e1aaba3de18374b95161a57c7954c7a8e0748fd2375ca2b79275512d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:48:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908527b139d9269245a4259635b1caf76393575aba5a1f4650d84a199883a1b1`  
		Last Modified: Tue, 23 Jul 2024 04:52:56 GMT  
		Size: 67.2 MB (67169878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef45fd5d95eb76e975ce6ad7fc757f1f16d9221d52553ce276767b054cf300fe`  
		Last Modified: Tue, 23 Jul 2024 04:53:41 GMT  
		Size: 219.2 MB (219161545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:086ee42fd7bfcbcf3a180d3a1fb8cd492372909dca9ac35acf6f30908f5d6b98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336180671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9924d6cd88082f4605e70e21cbb36a72f69d506bf2427203ffbb64b4af9841`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:57:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee36f9299929b13c64e8d1dcbbecffbc23ec614ec5279d3468b3cc790fe0439`  
		Last Modified: Tue, 23 Jul 2024 02:09:30 GMT  
		Size: 64.2 MB (64222016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4466f890a1001c0f56f2d169603e31a1e4180b6e1c7a95244e03020c696c07fe`  
		Last Modified: Tue, 23 Jul 2024 02:11:46 GMT  
		Size: 200.6 MB (200551501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0231f23e687071af6193d3f0efe7be3b212b3ea430c78ed6f8239d66a92b110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370097457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1fa43090877b8dfc38d6d93cdb85f0bae92c5bfc0a34b06b25c9908342eb8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:40:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aca4b63ee1a3a6c2c0c85f637c9ff06323c852e1a5363d3eaf9b36ec6bafd`  
		Last Modified: Tue, 23 Jul 2024 02:45:39 GMT  
		Size: 70.7 MB (70683207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0b716eafc6c8d8353c17c7c5d4fab52f3e2e2faa1180bb4d0761b66a184629`  
		Last Modified: Tue, 23 Jul 2024 02:46:18 GMT  
		Size: 221.4 MB (221396731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b82e36ee67e0cb1b63575257de321a356d70d95f7859923b926ed40667d7d01a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334590501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34de17661113981e29208c56c9e5a0c3adc6da76e0f0dde5d6b1ea77592a668`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:12:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13abee5c4577fc2e5e5ccd45eb4abcc067e815317edd4eb7fb89c6b9ff137b4`  
		Last Modified: Tue, 23 Jul 2024 03:17:12 GMT  
		Size: 66.5 MB (66483586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b246619b57093ef2ffbfca7ad46965ab0172ecaa73b81ecb7f975cf22e368de`  
		Last Modified: Tue, 23 Jul 2024 03:17:39 GMT  
		Size: 195.2 MB (195213514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:507533448f9d2e1cd93485a961771ea1f19c87cae1af33ed57b096f1156de25f
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
$ docker pull buildpack-deps@sha256:db7e1584702e2ce2c1843e73785ea850b91f22b67a0057a09fdef7e43de922ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72116850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbbda00da917e7c15e5ae572efa6c80ac276fd353d004993e53fb8b8c27c91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:db1f5252158b47f3f9fa5ed5624b494ab78c51d4463b03f107f133fbb5ea5f49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73217722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b039e1e67b088cf0cd7c850addcf872710e237ab7ea3dfa3aaca588c77ac4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f9dc952f28f4f4fd3c026313044d8143b61e1b9866c641dc75f5fc704e353656
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2989804b2d5db3e6028493ab7b4716ed548cfe707075cba70ebf5708623bf36d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7e59002f0c5a17bacae57287d22ffb537dbdad7313e5584c0587c37995b68dac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71456321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0958582e9224f89984a38c8702208aba470365a870911c829cd325bf7962df7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cccd4bbf4ceaf8dbca6aa841b6acb4b4d23f4ff686fbed7962ee9e81012c58d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74035615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442401ad9c62f629aa9238e9a3a47f7d55640fda00a3ae58c6c0958692b0cb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0f420425a3e3e552c0a70a1c436e26f5e2e750c3914e1b22d7fbde7af0aa2873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71407154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f58ed6eff53d376e39f4903d043d43b4a3d17e197634c8e49ac79add3e8172c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e5f97fe3f1a48f9e4aca45af9b3b7e87ba798a8ba240471261f529a919152f52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78017519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebba4d5b7f38f8bf724f7d03b2866b7ddd69981687a27b688571964bc6e68e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:89d1d494114c9c2f0f75857f06665f950ca2720c93062acc91e730f6fd4a4173
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72893401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f6498b1cd64a3a88462fec2b32b0c627d87abb7acfbaf75d585798ac49973`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:3406980511592ebd1ac32d131458cfe904552a8f7bc901be92ef196e20d973c3
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
$ docker pull buildpack-deps@sha256:079424468f0eb509ef049deee98b5cef0b9ebdcea733b003cd7395bde02700b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137527693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4fd31e466aae2585a1c45186ec7693e0f6c4d2da23cf32fd7488f304f3715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb2782ec0c8f6a51d6d35106ecb2c6dc20884f4733b1236af9de7260944277`  
		Last Modified: Tue, 23 Jul 2024 06:16:29 GMT  
		Size: 65.4 MB (65410843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d0191a2b3eb5bbc58aeab05f297127fa46c0883320291916434150c83e955d23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138741834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23a8db2f6fadafad6db8d02d01b62dc2151f0380773c96f655321756d8446a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3995f67f100684b8a4349bea104130c9a88c087b6156a290542809abaf92fee`  
		Last Modified: Tue, 23 Jul 2024 03:56:39 GMT  
		Size: 65.5 MB (65524112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:63f39701455c7b52b5afc3a4dbe8b79d58a527e2f7b96be64eb0eefb2c93942a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132659149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbccdac0e820af648947deaeceb9fc4085258cd537072d2a68ed494ce72573eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90386b6142530b1ede165d6dd3a0cd162bcd3ddd68e43f48c8f76f8ada03618`  
		Last Modified: Tue, 23 Jul 2024 03:51:24 GMT  
		Size: 62.9 MB (62860451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:879cf292ca55f2dac3f60d1ae87c900d99a880b17f984e3cea0f803942fb91a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137810832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a97ec39812e39e1c687955dc4e4357d504033c6bc4b60b658da73fc4fb46db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d923d1db8297e4b85a34a97bc7d75b03fe29b101ddb7138fecd879a6ebb4a9b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141205493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6af04ff871c1be2747f0f54793aed4b11296e5872e9eecd576d860f486361a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908527b139d9269245a4259635b1caf76393575aba5a1f4650d84a199883a1b1`  
		Last Modified: Tue, 23 Jul 2024 04:52:56 GMT  
		Size: 67.2 MB (67169878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6228088f3891510ab445efe6f056342d9a805dc01b753b8872d499908cf34828
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135629170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75ea010fd80caa8f1bb20778ef586a1688bfe15b745ebc58f17bbcb5ed3702c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee36f9299929b13c64e8d1dcbbecffbc23ec614ec5279d3468b3cc790fe0439`  
		Last Modified: Tue, 23 Jul 2024 02:09:30 GMT  
		Size: 64.2 MB (64222016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b9c22c11ce24f944e5ab6db7b108c9dc0d66620bc8a8b16ac2b1992ae0c11f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148700726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a6cd597306f829d3ed16e8c3b4fd9ca4cd5a55945dec1e4c5840820b52036c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aca4b63ee1a3a6c2c0c85f637c9ff06323c852e1a5363d3eaf9b36ec6bafd`  
		Last Modified: Tue, 23 Jul 2024 02:45:39 GMT  
		Size: 70.7 MB (70683207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6329d78700cf3032add31025f8c1fc5a855f016d94dab2742cf438bc93f333e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139376987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb065e2e54ebbee952f3f504e0aec0e591fb660cb8dd576307932ab4d75b050`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13abee5c4577fc2e5e5ccd45eb4abcc067e815317edd4eb7fb89c6b9ff137b4`  
		Last Modified: Tue, 23 Jul 2024 03:17:12 GMT  
		Size: 66.5 MB (66483586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:602c67cd2a3a2cea8f4f233ad277d063dfc2018680db313ad6d03b9934830263
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
$ docker pull buildpack-deps@sha256:6d176259c6b7a34bc0adf35f30ab267d5391c3149895198e79897c2508991866
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.9 MB (356891688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adea96ff5bbbe3d2cf37062cdb0220b675cd88975454fab80ca974dbc85ab5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a88954649deb248d6fd991fbff086ba12beaa2049bdb4f71a1a86908a6d06`  
		Last Modified: Tue, 23 Jul 2024 06:15:29 GMT  
		Size: 66.0 MB (66023447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea56e91006e20d1258408621b6da0c46533963c358da290f5423b1d1a55dc821`  
		Last Modified: Tue, 23 Jul 2024 06:16:03 GMT  
		Size: 218.8 MB (218789325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1681bcb26b04d6e7008b5553e6277ceb5413f1509b573713cbc2f3e3a9a635fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326235431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716998cfc77e470a5652ecc36e4a16f8e9530f004f2948e545e809f5e3367c9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:48:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9873310e83bd2c9cddf329c78833d832e9bbd909cf26e632b676e3b31b940`  
		Last Modified: Tue, 23 Jul 2024 03:55:11 GMT  
		Size: 63.6 MB (63564737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982638bae6423bbae98e0c502921f436b34355d3d4bf030c2252127b0c30dfbc`  
		Last Modified: Tue, 23 Jul 2024 03:55:59 GMT  
		Size: 194.6 MB (194599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b6cffdded486696d01044be124faf6afefa35c28402259fab0949e106904e28
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308055812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eead025bb596ebe6cd8def784662514169861219bea83d20c391d0d27e6a9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:43:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530b2c70788d78360d3f365fdef0a3a385f75d30ac92e588df91acda5d06910`  
		Last Modified: Tue, 23 Jul 2024 03:50:00 GMT  
		Size: 61.0 MB (61013856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f4bb1861e73c2193c46843eb11525964345067e7c1f80c54e7480ca0853eea`  
		Last Modified: Tue, 23 Jul 2024 03:50:46 GMT  
		Size: 182.1 MB (182121659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b45c87615bec35fb193846411480bb3fbf2e3405f8a70788966be99d98a5b49f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.7 MB (344717348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42c69deab6111c8cafb2fd66bb05974b6aeed0b41e5f2eaa21b16c92cd9da7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:55:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b13905653e52085cac0034a182fbc6e1096638d960653d96dee8be2a517342f`  
		Last Modified: Tue, 02 Jul 2024 04:03:42 GMT  
		Size: 66.9 MB (66940858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe043a6ab3915a1c9cd4aca34966c52c7162e40fae409638a34baa845fa99`  
		Last Modified: Tue, 02 Jul 2024 04:04:09 GMT  
		Size: 206.1 MB (206123380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:84886c9650d92c3b6aa8e0bf2cbf8df5e237e815d0e5e991d239e2dee62c22f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 MB (360049319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3f66fbd365e52553315d162563189082e7b6321df23366fe5364e288cf7ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429258c06093466c9fba74ce4846613a377ce78cf008d521b760c5170697024`  
		Last Modified: Tue, 23 Jul 2024 04:51:38 GMT  
		Size: 67.8 MB (67826201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83348b487e8b0fae77078e8fe8aacc19153613ee80154985d7004b2189853994`  
		Last Modified: Tue, 23 Jul 2024 04:52:23 GMT  
		Size: 218.2 MB (218167549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9028c225fe9b65a98fd81e5ad4b28ac2aa5b828cfb1f98ec22d39a175a306200
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332195395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d78f180eb1b796ab7aabca6af1df31c1b12f369e9e02d0bbf4a30c83c099656`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:49:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf5f50c37db38e90a50520c093b6fa2939d9fef5a62895ea90c91d02dbdeac`  
		Last Modified: Tue, 23 Jul 2024 02:06:02 GMT  
		Size: 64.8 MB (64814442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990154075f1f9e5c156fcb25dcc580ad4535cfc9df883915675c583a91f37a59`  
		Last Modified: Tue, 23 Jul 2024 02:08:16 GMT  
		Size: 196.0 MB (195964609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c18683a7b2e4a08a201c00bc455b420cb3bec97f5445c87e0b7b123a70689b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362845834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6421ee50a6f14c7c122aedb9c7582332b0d3a46aed1c235bb3fc86f978db3305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:37:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b98c88f8a6ca27a89215004b3cdac4fa255a74553ee93c0bb336155b16701`  
		Last Modified: Tue, 23 Jul 2024 02:44:32 GMT  
		Size: 71.4 MB (71413135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632e7382e9bc8051ac63dc520d51f93484e2c1c8f3c624baf6d2a99a37294f6`  
		Last Modified: Tue, 23 Jul 2024 02:45:10 GMT  
		Size: 213.4 MB (213409348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8fe7dfa1ba06d87a806cb93752c9e8224f1ec001816ec683bc3d8983b3b8b23d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 MB (392052260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dc99285208332856ca4f86ba0c2e095e5e6ad46644908ef457a9e2733717b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:17:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8a525751918610936d3d7c2f56948a95908e5fdc97875a13eabf5b5755181`  
		Last Modified: Tue, 02 Jul 2024 09:18:58 GMT  
		Size: 66.2 MB (66196372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d148814d72aaa345d1ebb818dabc2c064dbd11ae389facc1be8b9b7c3f8b5f67`  
		Last Modified: Tue, 02 Jul 2024 09:23:36 GMT  
		Size: 256.2 MB (256224615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:104b8641b7f47fbc3c0cf767a00a4df89cd675e96ec4abf2fc9bfcc2e2b5b392
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334266471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8581bebdd6dbb28f2b1f3ea4479683d449a04d2392a92133ae50fad25c8b4072`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:09:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:10:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b90812b56a031f8fd0e591290e9252f35ca6f8f86d5550448fbfcba2c2560`  
		Last Modified: Tue, 23 Jul 2024 03:16:20 GMT  
		Size: 67.1 MB (67066609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3711122f465e94e5fe0e07180db63aa5750b29edafa7e72d91bbd960a4724a29`  
		Last Modified: Tue, 23 Jul 2024 03:16:49 GMT  
		Size: 194.3 MB (194286348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:1c72afc3f7316b9452024d33fa62de29b136b713f8e51528076b39baf8c116c6
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
$ docker pull buildpack-deps@sha256:c506c9a4be6710ea11f6f9e651b299b2923321eb160bb25bf1d1e072cda99e99
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72078916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f91c17165e09e37563417b4384a281bd5f9a34451345ed1e380530c62e936f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6b5b91dd8563b6c83f9f292f47b4f4dbe9be84f6e6132701121dc0133e988f57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68071420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b80c1c593db8ba05c984a51879cef29a28366f43e1fb6396f1eb08e2ab6422`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfa97ce73cde95032209696321352612680db764c680a1b0951f78188c543fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64920297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9f5d5f12b39b29e168914b6f8c8975fdcee316b9e697f402b0b3c5137032b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:565aa9075ce6be708b8c521144ae8c1767a8ed5942f3f8b1295a4493b60f0a57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71653110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf790b8c8dcd40de930e7bb2cf6fc241552c0a3335cb4b13d3fb229e4becf95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04c2515d0b3ac31ffd91e42f38e369e1bff2641c2728fd0621aedc407df1b678
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74055569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad98ccf705d644b38203f371bfff8ec7f09a2c081edea59d84db557b6519f68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e7fa6ef8eb669a3a49a45a66f8cc69d7f09d1b83c63555825932c55ae4e2220
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71416344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfba9f25abc92be9a113bf2def9775d340036cb7b23d08e40a068554fb1d56c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:597bffbfd546b0553a21404706d32d58cb0aff05e5d1c007c50f45820a980671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78023351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e74849ee887deb1ee055850655ecbc96c46bfe4cdabff05dbcb2e34bf9a2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0ceb7dfebed647afc7aa3a53e3a91dc13bc962c18ea18a6febbae1ca159fb643
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69631273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0d285c318a8b4b87b73abe2d0dad0afb0f59bfcbea02b03781a46a17c7e4e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1fbd779f4eb589e092c27e36df4ce7691bba7800c279e8aa9588ed295da8f17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72913514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30203e2370c0857b26cbd63c6d17b0d5cb59f4f69da9eca5b30f41fc7f5143eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:3b2ef4e261459174b8e6f46108a757382681007fb4e8f86639082b968ab77a45
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
$ docker pull buildpack-deps@sha256:871b92b67481317387e09ac213f279b8fb96059446e3c7d40bfb5bb5148d8013
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138102363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf3e8f9d33353c4f56ccc19c5eb6ef5d3d9ced7c1fd41842802f454f5fa3f92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a88954649deb248d6fd991fbff086ba12beaa2049bdb4f71a1a86908a6d06`  
		Last Modified: Tue, 23 Jul 2024 06:15:29 GMT  
		Size: 66.0 MB (66023447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7177a05d7c22b3a9b2d05a23d3288d53fafa60f977a3de046d93d1e3294a97e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280ebc938aa661d553a0d9eb668d100e4f218a67504cf709cbbe6430f396df51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9873310e83bd2c9cddf329c78833d832e9bbd909cf26e632b676e3b31b940`  
		Last Modified: Tue, 23 Jul 2024 03:55:11 GMT  
		Size: 63.6 MB (63564737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:39c7d006924dc193dc2f5d78faa3f1d17c7e9aa6b3a182f32f75281bb942dfd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125934153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87e3a737cd11656c9a9dd1ce82646005ace4c4e66d8a1d15916c59c8511634e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530b2c70788d78360d3f365fdef0a3a385f75d30ac92e588df91acda5d06910`  
		Last Modified: Tue, 23 Jul 2024 03:50:00 GMT  
		Size: 61.0 MB (61013856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:743a0ce5bd6cfaa274351397485f81aad864345a0c13926d220cdee4eb03b940
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138593968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc61761d538deeed0142d5c59ceecc4f78dcfcfb450e7f4089f6ba36739de0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b13905653e52085cac0034a182fbc6e1096638d960653d96dee8be2a517342f`  
		Last Modified: Tue, 02 Jul 2024 04:03:42 GMT  
		Size: 66.9 MB (66940858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b56da467efc94000547dd9034462b8d9f943b11fc6f30c64478fcbed11d40b37
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141881770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605124dff5e3a0fb6f298d2b079bfbdf70edf727e979fdbced8ab337e4cc7bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429258c06093466c9fba74ce4846613a377ce78cf008d521b760c5170697024`  
		Last Modified: Tue, 23 Jul 2024 04:51:38 GMT  
		Size: 67.8 MB (67826201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15334f31455e132e2262d1167e932c92d2a60b10f7557b753356d655eb6feac4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136230786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf6833d7529096fa1bb3815fec2f0d0ee573811115caa84d9329959be919808`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf5f50c37db38e90a50520c093b6fa2939d9fef5a62895ea90c91d02dbdeac`  
		Last Modified: Tue, 23 Jul 2024 02:06:02 GMT  
		Size: 64.8 MB (64814442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fa91f7fe251a3e3a6e112335750dfcb83db9277a82a5fa58b45ecada4ffbfcae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149436486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ca1609d70f49394d680d1e00297b69c5471c813ff5070bb5360ed09c502aa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b98c88f8a6ca27a89215004b3cdac4fa255a74553ee93c0bb336155b16701`  
		Last Modified: Tue, 23 Jul 2024 02:44:32 GMT  
		Size: 71.4 MB (71413135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f96cb4ed9d65bc2f134e70ec4ec06cbd5c85b4b0504a225cff4315ed8c8227b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135827645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bac5dd12e16d55713e1db5e729f29cde5ac97748d2c50c3398cacfd525a733`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8a525751918610936d3d7c2f56948a95908e5fdc97875a13eabf5b5755181`  
		Last Modified: Tue, 02 Jul 2024 09:18:58 GMT  
		Size: 66.2 MB (66196372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c8daa564a12c68f5fdd9e98aa37893e0024a408aa9ee724e7d2bb44b70fea5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139980123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5535b3ab8cc246f97a1fe491db849a94bd5948200d49ca2d576954535f4ec275`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:09:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b90812b56a031f8fd0e591290e9252f35ca6f8f86d5550448fbfcba2c2560`  
		Last Modified: Tue, 23 Jul 2024 03:16:20 GMT  
		Size: 67.1 MB (67066609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
