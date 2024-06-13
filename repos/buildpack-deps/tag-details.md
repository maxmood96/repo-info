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
$ docker pull buildpack-deps@sha256:dbcaa5e6d9a2781212cf407729c39653cd32b2fc9c872d7b08f83c74697c65f1
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
$ docker pull buildpack-deps@sha256:045167f341265e83e50fcbc0739476bf0c2f9056e29d3edf85a810d33a6b99a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250119475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5603ea9d4e5f0860302e6cf426c1b9e0d54144f8c1ecbb1fcfd97e076b30faa4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:36:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed3c1f7e733f659785f3ec09fc5aafb7181463dfde5fd621ff4e755186f295c`  
		Last Modified: Wed, 05 Jun 2024 04:48:21 GMT  
		Size: 39.5 MB (39455122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59c778615bbd8bcc1be2d1888085cc6c6bf77a833779e4735d3976c6a7f7ef`  
		Last Modified: Wed, 05 Jun 2024 04:48:50 GMT  
		Size: 173.1 MB (173102637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7ac0497be5df83242ab5725cd28b64ffbdbe23c98b2d45456d6cbf1f7a176d1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217380055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1bf7033391d1a0b7cc1504eac0fa6cb1c2af14699869963af9880e2b07e228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:40:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca9608aaaded7216940920cf94566cf760f1f392ee5dcb044dffd51f2680344`  
		Last Modified: Wed, 05 Jun 2024 03:52:39 GMT  
		Size: 7.0 MB (7020980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b616962298953cec573067317321f9ed107e558b2aaa8c7f347d76f0129ebd9`  
		Last Modified: Wed, 05 Jun 2024 03:52:57 GMT  
		Size: 42.2 MB (42244717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e1e99ce186e310dbea71f5e194c20e0ae8ac0eff0f6ccd1439adc547184991`  
		Last Modified: Wed, 05 Jun 2024 03:53:24 GMT  
		Size: 140.6 MB (140579470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8740d6bcb54a076b11bb490e55a3af5c59a9c55f978a7eb2fa307640ab32e030
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241436596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6370b15f514326099ac8c4c3a558bb94d21c8e1c836cdbc491040755315b230a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:20:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcea6186f66b83759565293824604721be05055657a93197754d875e87759a3`  
		Last Modified: Wed, 05 Jun 2024 04:35:09 GMT  
		Size: 39.4 MB (39379473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d0ccb2a4ca3cac708a2c81e02a99813751e077a7558cf776e9ec6f0d48574`  
		Last Modified: Wed, 05 Jun 2024 04:35:33 GMT  
		Size: 166.6 MB (166584981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:35099699803f52697799371d71ca3a0bae89e112c13ea26b3116997a8a2e8073
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271240786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392776700688bd2613331e7b45d886a5e930bbc7ca2684ee1a97434a3bed4a2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:32:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c0335cfd20faf41c2684df8db8c0918fc181307423fe4a1ded886aa9f7918`  
		Last Modified: Wed, 05 Jun 2024 03:48:08 GMT  
		Size: 8.2 MB (8244447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a89acddeaf8bc6c6da6eb663640c72d2949562aa1209b43a9d83b6e4edb2f`  
		Last Modified: Wed, 05 Jun 2024 03:48:30 GMT  
		Size: 43.8 MB (43766282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18c46025e7dda290c1af9e27ec11bcf37af08631611eca1861819bbe77e8169`  
		Last Modified: Wed, 05 Jun 2024 03:49:05 GMT  
		Size: 183.6 MB (183641725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c7444befe6d944d10a9fb4ffd8b1b3f59cf8fd8fbcf3a7cdd3496315b08329ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223848864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02c9e254fc06ea48788748be5b571a06c32e5a72c91ed7eebdc6c170e7d3f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:25:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d1f4280511cf001472a1d4614c2482b39c5f1c36f22bdb5bdf1d80b6f34e1`  
		Last Modified: Wed, 05 Jun 2024 03:35:35 GMT  
		Size: 7.0 MB (7037156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d800481ca4a578ffd6afacde055d5c9b10f15aa78ed7e6f1f58003583f17ab0`  
		Last Modified: Wed, 05 Jun 2024 03:35:46 GMT  
		Size: 39.4 MB (39420378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8b47e75b6d22e0e3356eb110bee36d391172e58eec7a70d59e9b6a8aa219f0`  
		Last Modified: Wed, 05 Jun 2024 03:36:11 GMT  
		Size: 148.8 MB (148753931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:7779a591a40bfc86721dcbc2469adc533308056e5c6e7d674b89a04af56878f6
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
$ docker pull buildpack-deps@sha256:07cada24341288e2f2385b80b296dcb2bf94e13ba9370fd356d85cb1b18887db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37561716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f4668081a46b8c4134c13f9ac41f3bdb01170347d3f013436cc01b42bb5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bf8af84c64e569c3169c20c5c12e27b2869cdb73c88379cff4530418ffb26cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34555868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e057aece6c48fc6b656907bbeafb0862c0915a57b38a68c8a8d5cc0fa4ee47f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca9608aaaded7216940920cf94566cf760f1f392ee5dcb044dffd51f2680344`  
		Last Modified: Wed, 05 Jun 2024 03:52:39 GMT  
		Size: 7.0 MB (7020980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cbbd8a1f4560a08ebd715d246bd20d10753c50b8375de73afebda5f0d5d87c3f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35472142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444e5d79c70daed061f0ad6f19046b658de60a386af1502ef9b0d794794de955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:792e24bd13799c76879a0e6c5a61863c354cf7510f7e133bb490660368a1f23d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43832779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aba8a170045e6e319505c0d24c89181e999a4f34d96144f1f9c1cc257b36b3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c0335cfd20faf41c2684df8db8c0918fc181307423fe4a1ded886aa9f7918`  
		Last Modified: Wed, 05 Jun 2024 03:48:08 GMT  
		Size: 8.2 MB (8244447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9237ce3f5fcd17c4ff1d8162c7496b9664174362acaaf12ce58e122ce6b8d33a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35674555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfffd16e235800517314ce93c25987f978d9b772f1505c682c27c0ec36c862d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d1f4280511cf001472a1d4614c2482b39c5f1c36f22bdb5bdf1d80b6f34e1`  
		Last Modified: Wed, 05 Jun 2024 03:35:35 GMT  
		Size: 7.0 MB (7037156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:6af3f751b44d76d0baf982c2bbfaeb53371a8734c2e3d048d2b67ab46193d2aa
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
$ docker pull buildpack-deps@sha256:e36315391256b7d6a3ba998e79a79407cea73f31833db51054cc6026ba00f9e7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77016838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f80613a6709b5141dfdd2cdeece96d50d63beebb30174277191707e01e8a353`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed3c1f7e733f659785f3ec09fc5aafb7181463dfde5fd621ff4e755186f295c`  
		Last Modified: Wed, 05 Jun 2024 04:48:21 GMT  
		Size: 39.5 MB (39455122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8cd9d2105860c293542c7d8e47469dba804445be065563ab6a15324f34558b5b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76800585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cc51016500e4b010486cd9d8b6f6a99804f31527a8a2660c7097edfbd77d44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca9608aaaded7216940920cf94566cf760f1f392ee5dcb044dffd51f2680344`  
		Last Modified: Wed, 05 Jun 2024 03:52:39 GMT  
		Size: 7.0 MB (7020980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b616962298953cec573067317321f9ed107e558b2aaa8c7f347d76f0129ebd9`  
		Last Modified: Wed, 05 Jun 2024 03:52:57 GMT  
		Size: 42.2 MB (42244717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b9fddc77e5b4ac6c63e7dafd1fae57c12204a602d0cdef1031fcaf77ea25ec63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74851615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f159a46f5a8caa981a762f469ea255e46b32a780c2a3bc152c759b243ad91b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcea6186f66b83759565293824604721be05055657a93197754d875e87759a3`  
		Last Modified: Wed, 05 Jun 2024 04:35:09 GMT  
		Size: 39.4 MB (39379473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f38198fe72172fc55ee9693fc3090218c36c0f9652efff83e882194cb1c5d9c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87599061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081d69f98e0049b442e431ac29633f8d959ac27978b836dc78fdcb006110a210`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c0335cfd20faf41c2684df8db8c0918fc181307423fe4a1ded886aa9f7918`  
		Last Modified: Wed, 05 Jun 2024 03:48:08 GMT  
		Size: 8.2 MB (8244447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a89acddeaf8bc6c6da6eb663640c72d2949562aa1209b43a9d83b6e4edb2f`  
		Last Modified: Wed, 05 Jun 2024 03:48:30 GMT  
		Size: 43.8 MB (43766282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:11ff4021d9c999c9b1a47dbbfbe435f1eb91a4d5d23bace2679e05edc8bc0c04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75094933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89834543756364fdbc7fc709b2abe49c2064f33540fff730cddb5f90ed0cb35d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d1f4280511cf001472a1d4614c2482b39c5f1c36f22bdb5bdf1d80b6f34e1`  
		Last Modified: Wed, 05 Jun 2024 03:35:35 GMT  
		Size: 7.0 MB (7037156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d800481ca4a578ffd6afacde055d5c9b10f15aa78ed7e6f1f58003583f17ab0`  
		Last Modified: Wed, 05 Jun 2024 03:35:46 GMT  
		Size: 39.4 MB (39420378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10`

```console
$ docker pull buildpack-deps@sha256:cd16e8a7877285c6b425da617bcbe0934864820cd39e6cd6dac94be66353080b
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
$ docker pull buildpack-deps@sha256:39e11b0343b39ba1729463f73ec8aa2f3192ae4db6df33d76ef6cf2d3556e99d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279881501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52f4321c594152af94c764f0cd48892290fa8ad5dfb752ac7af9b9c0d411d9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:41:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea509a29544edd67ece4c5006665316329880fdef08c2b42d62e31799e97bd9d`  
		Last Modified: Wed, 05 Jun 2024 04:49:16 GMT  
		Size: 44.8 MB (44778339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1086ac34d156d78afcae383fe5097fca7cdbccbfd64d127cd602668ce24cc1f`  
		Last Modified: Wed, 05 Jun 2024 04:49:48 GMT  
		Size: 197.2 MB (197154166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:15959ae0ea998982c4f9020b571c183a74b8ecd6173975dadf221a7b1172f8cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246497968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac5fadc348a3fa3c9c0ead1dc43b82d56a7d9bf9c632203e12e1787cd66406e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:45:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76642a0d8c917f8b4762138fba3c9de67689f5a5e5de9b64d3f6f72b20f70709`  
		Last Modified: Wed, 05 Jun 2024 03:53:52 GMT  
		Size: 48.9 MB (48942204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8865e47fb8518fbe3850de6b634b5678c01dd50ca46ea099fda5505a3460b2f`  
		Last Modified: Wed, 05 Jun 2024 03:54:21 GMT  
		Size: 162.7 MB (162714941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7f457a5344fd7435aad4d247de7e5c3d08dca96ec1e92001b2ab61ecda6cfdab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272058036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af0c0ee269d424283ceb8d57861c59cba924e5c4a445e47decf8fe5531fcd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:26:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a7640621fe982a10d3dda8496aea07502c6024b26780042604c39f807ebd4`  
		Last Modified: Wed, 05 Jun 2024 04:35:56 GMT  
		Size: 44.7 MB (44747249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6965e4a49555791cd958de7368bd1b08abb6d5e505e32016cd339f2851aa4cf`  
		Last Modified: Wed, 05 Jun 2024 04:36:22 GMT  
		Size: 190.3 MB (190264334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c5518ee43966f4d3aadc3036aed440186d365ac1c31e3537dd3873c9a702b57e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293830944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f909253f1cb306f8cc9d72a734c9aa127c4f96619e546a80603402f14165c71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:39:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb7ced059bf2a43a1fe9d833ce19fe75a8eaf293da574dd45c14836e77cdf4`  
		Last Modified: Wed, 05 Jun 2024 03:49:35 GMT  
		Size: 49.6 MB (49618077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7ee833f24770d2de6172bc5a24ff710d08064d7ed5d5c58cc56080e319e1f`  
		Last Modified: Wed, 05 Jun 2024 03:50:12 GMT  
		Size: 200.3 MB (200276421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8be834fc55e85de04be1a4be2b720b896375063e368195c5c61df37086dec2b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259174294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daafee1e2949c467e190a77fefda1291dc30bfc1d91720ac40807974b783772`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:29:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8180965f353999389ac9a5a3880e73af3fe29a168b55d1e7cf69c49184ef1d`  
		Last Modified: Wed, 05 Jun 2024 03:36:33 GMT  
		Size: 46.0 MB (46047739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6c8bf19011470468580af2c58176f51e586eef8ee879c216bc083a94efa7e`  
		Last Modified: Wed, 05 Jun 2024 03:37:00 GMT  
		Size: 175.5 MB (175476132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-curl`

```console
$ docker pull buildpack-deps@sha256:64ff1d51b7db55077ca438e19afe2e88a08e0be2fcf5a79be2dc1228e246c6ec
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
$ docker pull buildpack-deps@sha256:9f65957280e34d727d025322bcf7d314be2ce0ae97063ce89e54ab88a65ff982
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37948996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d10deaee54420e6c10878f9ee930340477d0dc33c7423164068882dc40bbcf2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:585ae91beeff1e302e8fbffd7436e9db6f46e13a973139c2d4a56b34be0e8fc1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34840823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16789df5390866049611449ffd67171d93c081cf31f97b0e08cfd4464a55044f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:07a9da40434d6a8c2d5a35ca88d92f930ee9f1b6e7a65e8a6b02b4c44de57835
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37046453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d05d326c25364894e9f656270859b9ded72374cce2b4b34df0334f7001f943b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:49bc816c335208a1aa228d93eb5249ad6517463820a934617e7d29528f2b1e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43936446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5588bb15e96c780644c9ac6b12ff154eaeb9dfeb06b4e5bd45a117ad2671204`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d10b27e68cdbb7838a0eed6aa15639f6d6d4d98d060a945857105e94a0205a67
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37650423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee0ef73519b656095be7272b6cecb34c401a7c464dd7e85646659d8b55d566`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-scm`

```console
$ docker pull buildpack-deps@sha256:16b936981452b9f44a0a58d93eed6d0a35006f36e6fe677bd073e94751c9b314
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
$ docker pull buildpack-deps@sha256:7ac32abbc5bd894e66ca36355e4212564fcd2887d97a91990b4ca4f7310cffe8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82727335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb289c2b2e169763b6524ce729573508c902bb6de42094621683a77c16840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea509a29544edd67ece4c5006665316329880fdef08c2b42d62e31799e97bd9d`  
		Last Modified: Wed, 05 Jun 2024 04:49:16 GMT  
		Size: 44.8 MB (44778339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dffdddc92193eb796ffb33065b30796f20d7c1df54f8671fca0fbbe6df617272
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83783027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec225f12da4434d781ad9b074870e390b9605010ac72f3262a67900eaf8b87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76642a0d8c917f8b4762138fba3c9de67689f5a5e5de9b64d3f6f72b20f70709`  
		Last Modified: Wed, 05 Jun 2024 03:53:52 GMT  
		Size: 48.9 MB (48942204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:825dfb37fcb76a6ccf6308a4dd9750b16454cef52968f7d78a658e6a864e02ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81793702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb2aa33211a1c117b30f56ba7edbdee935c9c5afed0dcdad799e3f0d6764541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a7640621fe982a10d3dda8496aea07502c6024b26780042604c39f807ebd4`  
		Last Modified: Wed, 05 Jun 2024 04:35:56 GMT  
		Size: 44.7 MB (44747249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2d41584f5bfc5f74f4c9ee4219d2aade02e1784f0d21489120454fa0324cc094
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93554523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5df9795dcc60d79106b41a88b1d51bc5d039e9e8d9c75343bb8e632b4d8813`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb7ced059bf2a43a1fe9d833ce19fe75a8eaf293da574dd45c14836e77cdf4`  
		Last Modified: Wed, 05 Jun 2024 03:49:35 GMT  
		Size: 49.6 MB (49618077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:81f715a4d61d44a0bf4f15848f950e8b70995191779291a6e65abe51232a7597
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83698162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370f2491b2f8c94c9a815eee1e1e01960197280f0ccae7e259ca143c5dd045ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8180965f353999389ac9a5a3880e73af3fe29a168b55d1e7cf69c49184ef1d`  
		Last Modified: Wed, 05 Jun 2024 03:36:33 GMT  
		Size: 46.0 MB (46047739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:9f35d074ab95834d6be3e55f54306ebe6bc53bf79e68601b46a8ba7f8cd4adfd
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
$ docker pull buildpack-deps@sha256:f3b09bda3b5c0919cd33180d172afb9ecd882a51269d6f4629a563f987e56072
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279729402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e4aeef9b47b481ea5ac3f679eaa9d4b0478067b672521cce966285f2c424a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:46:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87947638455b11c231fb8b483c07d47962e0468c49594803a3b86c4e901efba5`  
		Last Modified: Wed, 05 Jun 2024 04:49:57 GMT  
		Size: 14.5 MB (14471023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc27c5d51b891b5c5ef9ada2ceda9378dfeb6aaa6443443df4b986e5fd5aca5`  
		Last Modified: Wed, 05 Jun 2024 04:50:13 GMT  
		Size: 45.5 MB (45472926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974fa8c03c6f2f34a8f09b0645c4e1629876fc31b84c1d77684ec3eef5b343ed`  
		Last Modified: Wed, 05 Jun 2024 04:50:44 GMT  
		Size: 190.1 MB (190080677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1d37137547549d646fd57c80777473ef45ae08123b5ac09fbf5c4fde3067832f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239981834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ece3e854961aad2be5695cc18d54a9e4b7f8cc59e34f8d8fa83a93434b92b81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:50:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c8d02626362e73446fe59044c18a39c72b337463c7d3893055fa2f243d418`  
		Last Modified: Wed, 05 Jun 2024 03:54:49 GMT  
		Size: 49.0 MB (49014700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f34590d25db915d57bedf55001f29ec4ebdfb48c7ea83504b8482e68e45c0ba`  
		Last Modified: Wed, 05 Jun 2024 03:55:18 GMT  
		Size: 150.5 MB (150516385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8918e8ad34c286976bef24fb3a4d1d444e191b0a0ea2bbfa77062cb547b94a4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270819353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0589a5e0efcc86c91b3cda343b05e2911762976bd7e6cefb955b6ab7395c87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:33:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd7e72a53977344ea977a1fec5263450b6d1384d18ec232e10b2457a0e59d7`  
		Last Modified: Wed, 05 Jun 2024 04:36:32 GMT  
		Size: 14.3 MB (14303235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458f17b6ebb02a21b5aef3f00ad6e8c8df1dcf0ac11d9da63522e84c01392c96`  
		Last Modified: Wed, 05 Jun 2024 04:36:47 GMT  
		Size: 45.4 MB (45432069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccebc1c9f46d7f19aaf713f2fbf0f3783831ddaa6c5692c9ecb6c64ad4dd1ad`  
		Last Modified: Wed, 05 Jun 2024 04:37:12 GMT  
		Size: 182.0 MB (182040127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9619e7c9339fe5bdb325c8d01555ce2746158470af37a237ff1e3cf8b202a949
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299075645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdc7c63c45b23130d981ac8d546c3afcdaed68df9000044e7e2a5c7708517c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:46:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a2f6408ac8504d2696bad50727125bba3b8fcbd3f4cdb16db364d82f071b65`  
		Last Modified: Wed, 05 Jun 2024 03:50:44 GMT  
		Size: 50.7 MB (50707829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b25879c4fdce10703def064e54c010daf1b8184181400403c00faa9efd17e96`  
		Last Modified: Wed, 05 Jun 2024 03:51:22 GMT  
		Size: 196.8 MB (196751435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dddd9fe0920094e9fa26ae39d8dfc7d4bc5125416bdf0e36d08a7ebbd36d9e77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262135650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46582e245ff1dd4d81eb347b044e99e2f37966f0581b541e144665050b053d63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:33:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d620b15b28615214d0c65c6af1f9e67a03ef2f4b497937d254d6730cbfab1d8`  
		Last Modified: Wed, 05 Jun 2024 03:37:23 GMT  
		Size: 47.1 MB (47119774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cc128cc05544c139bf7bea282e63242ff37d44a9bb2ae723d3ca4960faf099`  
		Last Modified: Wed, 05 Jun 2024 03:37:50 GMT  
		Size: 169.3 MB (169340116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:039da1e7ebbd5f7fc301722b4b0d18e3cd55456f908abaae07f28628ab61b35b
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
$ docker pull buildpack-deps@sha256:b2dc16166dc335a8243b2c059e45f67ec2730b67af36d2ed46f8b64af7427f31
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44175799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbeab00184d80f11b993746c2f754e7409eb90af725db353ef314480890deeb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87947638455b11c231fb8b483c07d47962e0468c49594803a3b86c4e901efba5`  
		Last Modified: Wed, 05 Jun 2024 04:49:57 GMT  
		Size: 14.5 MB (14471023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:95473b4b84a9ecb58b5f00999164d858b82f209123c313edc3d59ccc17459e12
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40450749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7c54d27f963db7485deaf9d0b0e69078d4395ee7839f208c22b2c3b5dce577`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:10e9f558f47001d6f621d3cdbc3ea932ca1b645fe9bfe56e488a1ec4805072da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43347157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccffde84727391d35a03c3f7b8c0f9170c63d8e60bd2b8f14d7e0cfb7a74e219`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd7e72a53977344ea977a1fec5263450b6d1384d18ec232e10b2457a0e59d7`  
		Last Modified: Wed, 05 Jun 2024 04:36:32 GMT  
		Size: 14.3 MB (14303235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8427bfb305d7e972fd03e0fc0f799d537170330fa53f119a34b8452e0af5962c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51616381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c7168c2d96a978da33b4a6a45abd17e6f7b5470e186819b7272308b416ad74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0aded05b0749fd5bcf1b632be0ccb7a071c0a03403fe5e218e80cad3030d97f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45675760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8702617203377c2d995dd6ddf3bcc5b3af6717281b550a5e33ec66ac1eacf3ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:83787c9033f6651c6665db0b08a0f66857d74954c03f667d88a932cc46611171
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
$ docker pull buildpack-deps@sha256:c5e776d37879320ced0c09678ecc460340d40212e54ffbe5e698b508936ec1e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89648725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1585bd8d7b4034b37684810605e00e7ec1c968ba75ef062091feea7e066930`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87947638455b11c231fb8b483c07d47962e0468c49594803a3b86c4e901efba5`  
		Last Modified: Wed, 05 Jun 2024 04:49:57 GMT  
		Size: 14.5 MB (14471023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc27c5d51b891b5c5ef9ada2ceda9378dfeb6aaa6443443df4b986e5fd5aca5`  
		Last Modified: Wed, 05 Jun 2024 04:50:13 GMT  
		Size: 45.5 MB (45472926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8c02868790f8655786d780dffc39d21842375831267fe3124ab936f9dac3fac8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89465449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f32f7bdb3e04437215dfc7bd9bad8d6106895f414b066856629105d10050799`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c8d02626362e73446fe59044c18a39c72b337463c7d3893055fa2f243d418`  
		Last Modified: Wed, 05 Jun 2024 03:54:49 GMT  
		Size: 49.0 MB (49014700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:afa1ebd742604b095f4901cdb5171d6675ea594eb5ccc392b36a05bf4095a082
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88779226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff5a1ca5b3cbbbb79e03910f323884e2df231af55389389975fb5117f6ec911`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd7e72a53977344ea977a1fec5263450b6d1384d18ec232e10b2457a0e59d7`  
		Last Modified: Wed, 05 Jun 2024 04:36:32 GMT  
		Size: 14.3 MB (14303235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458f17b6ebb02a21b5aef3f00ad6e8c8df1dcf0ac11d9da63522e84c01392c96`  
		Last Modified: Wed, 05 Jun 2024 04:36:47 GMT  
		Size: 45.4 MB (45432069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d0f48e3478728a9701660e623006d9992d4fdf7f241c5891f16409282f9cbca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102324210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc277f900685ae7d741614024adea8818fe29ba0202c9dc9c245178fec3b51b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a2f6408ac8504d2696bad50727125bba3b8fcbd3f4cdb16db364d82f071b65`  
		Last Modified: Wed, 05 Jun 2024 03:50:44 GMT  
		Size: 50.7 MB (50707829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6ec31897dcd9987850bccd08acfa048868e830b0ab57816586a161c597975b9e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92795534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa38465a229c4d42a0140519a9a3f7dcab6f88ca6085473f76700c6f198dc4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d620b15b28615214d0c65c6af1f9e67a03ef2f4b497937d254d6730cbfab1d8`  
		Last Modified: Wed, 05 Jun 2024 03:37:23 GMT  
		Size: 47.1 MB (47119774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:605f54c6cc897f95091bfb9972147f5de88ba0054278579b0fb12f9460b61401
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
$ docker pull buildpack-deps@sha256:1687ab7814a17df3aec0f31a20b31096b4b3361bacd3e7043787c8cd66fde314
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348976046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98709eacae3957ac0547846ed05ee63cc92428cbcdfc096c8ba12faf130cecd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c3e352f3d2eed4eda4feeed44a1022a881058df20ac0584db70c138b041e2`  
		Last Modified: Tue, 14 May 2024 03:05:02 GMT  
		Size: 211.2 MB (211207185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d992b823c77691e80a9731b308d4e6b56e46768cf3d026a0b7691daaa68efbd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316106610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137d197ce9f7674911d41eba9ebbcf2a0a7599ac8cc26d8b667b34b73e2767c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0475d9394b70464b90e234102b87625699171564d5f8cad8ec2f1d4de8fae2`  
		Last Modified: Thu, 13 Jun 2024 01:25:04 GMT  
		Size: 184.5 MB (184522344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fba40e013300dca943a346c53dfe423b82f7c9a46e86f260e65f761c376a3a4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301521074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c2e45bdfcb18fe68e2ffa3712c98ee0b3b4a394260f3d0f2626418a86c0f17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21d8970e0ba89fca18dc8a8432adc4570843d9db8e5e79d0ffb8099ce62748f`  
		Last Modified: Thu, 13 Jun 2024 01:34:03 GMT  
		Size: 175.2 MB (175175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b0d4f4ec2b8d73474c3cc9e0107ff9cc410fe737b23e618ee5502d7555b0567b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339788038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2ba4bdb71e9c0e6a4bd3fe19433338243cdc077789bbbd309588d18962d979`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222cb3bce424c387cc9f91f975242473b8be06d3426252fad4895105c051ad28`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 202.6 MB (202593329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:29414bea5343ab5bae4d1ee32c791dd2533ca26de259d76798a3ad5fe9279d4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351608036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1316642d0447c1d49296da3a2369562964bb569120c55c707de83aee2780157e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:07:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba812ec2feb1a698e5c5b1fda0a47d8bbba6cb3f887e520925c9fc376b01836`  
		Last Modified: Thu, 13 Jun 2024 01:20:01 GMT  
		Size: 210.1 MB (210128099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a4c89a334218312fd44b5f1d955cf30de87a03fc71c0ba36986383f6fa0a65f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325760195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d28dc9ef3fd0759c67fad11e737dabdf7b209dbcea9f335533d31f87f9e94d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:07:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3514ef59a25de65d0663fc4a360de7a712214c493290dd77858247edbd0dac`  
		Last Modified: Tue, 14 May 2024 11:40:05 GMT  
		Size: 189.8 MB (189771182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a544662c4f116d28f8d9392b218bbc9aea51cc8044fcb58153e3d5aa840ec8b7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363098165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01108acde413231d079df110cb9507133f84d976be2070d019e5814693cc74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:57:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80be54620660eb7b908f8c79a7ad14bedcac29ae46f620f4ede820441dc65d`  
		Last Modified: Tue, 14 May 2024 07:11:29 GMT  
		Size: 214.2 MB (214234653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d922b4f1ae136f4b4936921081d6d4fdd4f4f0e59502bb3cb09a7108979a23cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318356016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8130953b75a002b98650046e574455a2ad02eb7b9ee79889870697f5c0f7e51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:231dfed2d44ccf0c0b589bb631cde1b5bdfe875f468cc13ea0e43b870d5ce18e
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
$ docker pull buildpack-deps@sha256:a69b982f62d7bb630caab917e4569cc560be701cd441d4aa2e8f1f8b111959df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73626490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455623d6bb6491f83205d9f69de70ed5a5bc70e61aac57d827e2efa733d75324`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:303b096eef41800a1c02bfcbb3dbc07bb67281e4f22b20f95c714835f7aa4eac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70066810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b56bd6b007ed413621e7a0b48f2d41fc6093153047c4a00cde86395796e29`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:80d27697996c7840c53a4342aa5464b325a25b220c873005fc1cf1b95be2c45f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67128818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbde1c9da59699fbc0c744a3c5438f5a8d013154787e1077c45f1526d1a58b0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db6be8e4d0ebef4a6af57304c890a87caea1988737d72c8972789ae4e5bdf6f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1655b481f30a7aa209f341e88541070569e03c3488c2fc0860e8546d81d080fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abd1412796e09c71e6a50980f7d3af6f136894c619abfae59c08cdf63891a9cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75490919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aae593ab7e2abe2d66141cae6dc3e52712746e79492516b4ba29d44d832376`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2c1e371988b4586288f0b89736f9ec00075c5a90ec207cf590c0982dc03e46e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73020502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c086dfa4c627be61aa7eb1c8515aa5597126a6533f7fbff8d2d83029dc223`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a33fd0d3726fed3d4bc388d8f0371396b35dbd572838c8ae08199b6348962e99
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79279424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fce485682ba3603437b1f85c5c3416023adeb67e564daebe1ffa69293fb4af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8eb4b2b46fb45c8d6ad4a25b823b73f75dc124aebc9a113da6229ff7e92bdfce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71989047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e515dfe7d427d18f2d8935ba66f12b8cc1602cae1f6413eae5977798c2dbc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:a6d0207fe155f31e08a110c60ab94726f8f333ae6fab89b0ed5a20a555ee3430
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
$ docker pull buildpack-deps@sha256:cafa7552464a8e435f617ed9ce54db28cd69754040e60b3e1d8e3da9e240fb4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137768861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e822656587a2d640e11855cc11ae31480cfc3593678b3d6e7c221dcd215e71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:772c90ad5e828cf03adc31eb0a9fa1bdd4852259e4e5dbda10722ca4107bf0db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131584266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bc94d15114006a866db4bd4c7322ba8cb7db980f6fcc7576a60b49ab50fa21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:396d3e22ca837d6dc7fcbbc1eb72ddd0a287bdcc719a70e88b81da2d37ec30b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126346044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8771b9bbff94993882551c3970c872d8dbf62e2b6d78509f2b4d632f054b2fa1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bd92687ac56e76373303a1181e86f7e93fb7a2c7a3d248d04755ff557871290d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137194709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583fcf8f489e99fbb1dff9fae70e159d13c3b1e52012a1ef58deab3e9530429`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a88627846763b57606a8c341c6fefe0c692bbac1f4d632d206cc2997cab59e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141479937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a52dd664035d222019a260edd64c5ab6f717800cdcdca5fb1132d25886e3105`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:07:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8cf747af094998ee527bd33e348e9ef1c22c349757f3cde7ea7a0fe0a5b60fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135989013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1510421a679e334d18d89b5e06c07eb5401fa8dccbc83c12a27396d10b0950e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3b8246fbba99cc2e0111674a50e104b1d8137b9d16da58c380178086ef2bce0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148863512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bafc88136a64496ea3d6748a3c9a8fe760025c3d36d49e43e9da7352a658e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59256abb2252e0cda7425a81f7eb7e0b7f4d75fbf878b6bfda2e53dd42bcf37c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135119229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c8dd30373e0a52b50ba369650c99250c095db7eb2bad40372909251e1f35a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:001b60168847adaca546117ccb57aee6bfe9f2435b39172f8ad3bbaca5bede77
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
$ docker pull buildpack-deps@sha256:e4d025916e47a96e384860b14a7b557682e34a9f7e898d60815a4408dfa0a042
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322467989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194ca5518838e2de21da2f6eaec2fa7aecd742455d5edc27148bc014aecfa113`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6043113e1c69109f845390049c3534bbf0249241ce681aafd8e6d4bc4306dcb2`  
		Last Modified: Tue, 14 May 2024 03:06:01 GMT  
		Size: 197.0 MB (197014118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b0b2a0e4e4799a38d68655af4fd07f31a710bccc18f59599a017a61f4950f430
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295524173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a766bf7f3d8dfcd47fb388a09c62067d8a9de3fb12889173ef3b584527a55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:17:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cab5068a9c028c7944d8c796ef2a3f2f0405e6777b233048bc9107bb87a65e`  
		Last Modified: Thu, 13 Jun 2024 01:25:35 GMT  
		Size: 52.3 MB (52330351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44e3b2454499d7c1424bf7ddc4cd476d1413aa087ad671dd79a68e82543870`  
		Last Modified: Thu, 13 Jun 2024 01:26:12 GMT  
		Size: 175.2 MB (175214715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b32db2f9c6af34e6038df7534fc819eb754d7f0fab6f4b357b43fa7a7a6d7c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282975663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4917bfe4856245bd09bc3f3722de40b3137927a58b107a049a3160efdd2a9813`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:25:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d33379b30e1ceb9b87b34482bff5906df43a22892099a6815c383a940044f8`  
		Last Modified: Thu, 13 Jun 2024 01:35:16 GMT  
		Size: 167.5 MB (167479604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4080cadee28202ed429666d670b3d1c1d92cc8c0688040c35f66c04d393d3fbb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314121806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64482ebb6c736604cbea29716fdc0834b3463956f14cc88a98999c97dd8ad9a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315e6e292ef6ca0113f94dbf806ecbea714420b97b385d4138e3cb84616995e3`  
		Last Modified: Thu, 13 Jun 2024 01:31:54 GMT  
		Size: 189.9 MB (189935383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:51507984c7f84283125a3a7218bad561d49bd684fe07717966557af083957584
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328192875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dbb2053708b8c142d26097a23648bfb41d722006f5daa020137f40705accfd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:11:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4e6f3cca702057a7a6cdbd9b2d2f758e1d85524fdc9fc26824db70376bce11`  
		Last Modified: Thu, 13 Jun 2024 01:20:33 GMT  
		Size: 55.9 MB (55929392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4267f96413a024e086769e096a862097360934db8c089f130cf1a23d340ab836`  
		Last Modified: Thu, 13 Jun 2024 01:21:16 GMT  
		Size: 199.9 MB (199918065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3f2ede943ad3e38ba4d4d4344842fe6ea87a61e4da4632c71d04247ae54724ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301297067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0333b5693b777f28d86f796678d85126330da0c996c232488eadd8708e7909`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:15:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5c693cc8c99f19e173787a1971e0d4a76aa939dbd2b62fe612add7ec9c0e7`  
		Last Modified: Tue, 14 May 2024 11:43:06 GMT  
		Size: 179.1 MB (179132072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a7e5a95fc3ce6a58d5d6488104b3f6e9074c08fa68e6e96cf7cb193a4f0c8059
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330973531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a982f067c0803b07d8fb756018b2a98406cde4858656d215dee4e9f781cb385`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:01:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d0e9056be49b56fb034ae67015f749411fff8fbd5b427d798c9847f60a8251`  
		Last Modified: Tue, 14 May 2024 07:12:37 GMT  
		Size: 196.4 MB (196363387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6df620f843eee47a26b4f082f55655756ad856b4b2b874f85d1f12dcc164917
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296082692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76854a8011768dd4c02eb73f732ff1c8787e3e6570c9a4338cf538aa254ab367`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:23:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c7ec963ac714a2f94b076f8e287270d7deb6f725c170e54c73463524ff8f0a`  
		Last Modified: Tue, 14 May 2024 01:30:55 GMT  
		Size: 173.0 MB (173025883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:bb0d17256fa57b9d6bacf1b74fddc8a510356161519a182dc28cf9e01c6c519c
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
$ docker pull buildpack-deps@sha256:0bf0aee11419e80a8fb33d389ead5f7968f48201150572d532da38bc1389aba9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70864266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0bdab4b2f868715425fb9150dba135510f9018a8785ac1090b9111a8910a21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2b2f1f685532327796e804134544ddfec3fde6773762e27096b0066a97fc52e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67979107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a1d4c7209fa1fbe40e1ee1325a134d9d96acc1d504361bf97e915c5c101c4f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e51ee971a62d9c5dab65dc9a1a66524ec3f1a31966334b215e47f32fb0897fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65136600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1d5a3aeba0427820070a3571004591e217c496fce7bbbbbb05f4d45984e71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9359bb6986f3f0ac4b4f1ec25c7f43779528d66b11e344603a5756ee6a6880eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69490048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d1fbcf54cfbbf4fd1ed5aa60b5733e4156545dec11b7f73364b2a3791ce3f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:23a702ab32e94ffed98ac05892a52e75723505616d572bf856c49ada8d7468c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72345418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7af04d557eded6f95a75be4618bd44bbd28b44b15adc95793da9d9f8b0a2dd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13748c446c41dab3c38922b2065bcc4bd2678076424a0001764069c527d2761d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68852398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63c8bec0b6ef36e7adf04e70dedeeee6c35be164dd1a3cb83f3d573fe87076`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:145755a231fddd2b044c4fbea7a3b42e0e6a1520fd6b41a9cdf73bb5cbec5d16
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75736359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7ae016308cd2d9178f4e3e52a44bdf2161d137139a59997200ed8be4176860`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4394c08db48cbf1e845fbfb3411ee8fec119006c580147493cf64d2f6c170652
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68979966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcb2524a0cd6b3cedc2e7cf1f359f191ee373805fd6a0d946661ff4e532c3b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:f7a2112a19163f18d7e27db7b5f22ce895c6bd4bdf16746065a8e10214e35d38
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
$ docker pull buildpack-deps@sha256:b9442185675e2e9874b661d6eec33ef42d5c5330fc73b0ddfe40074d49ed4642
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125453871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00afe6b457f0a039f2c3a3d817d46b533f25c54dfe23745575e7847d057f557f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:80fea9df2b0bd76af9b4344849e42a975859c4035b5f448f5063418de4c51569
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120309458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d957d7700016f5284abc1d02f1f63dee513923246df56449b954a86c38218949`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cab5068a9c028c7944d8c796ef2a3f2f0405e6777b233048bc9107bb87a65e`  
		Last Modified: Thu, 13 Jun 2024 01:25:35 GMT  
		Size: 52.3 MB (52330351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d02805b0cef84e51319634baccbd0f558c40bb630a39c563b6f6462ebaf8ffdc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115496059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e9b43fdc65ee88e04d5b4a276a84d014d45006160ff1ad4a42f75081def9ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:edb9eda62914d58ff0edb1fc4035cb32c24a3e50f676a8da8b64e7d0aeeed44a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124186423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba35868c87f3ab37b7d05c65c772d38d0b877bf1aeb211e5f298c3b5641dbbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0c519e89989efdac4290b4b0ea4aed2b2f2b94a00bc40e72c70a635c4cc85cf6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128274810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbfe0bd56d456be29159feb9764fa1d354e52dbf6e4c441978817e04929c6b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4e6f3cca702057a7a6cdbd9b2d2f758e1d85524fdc9fc26824db70376bce11`  
		Last Modified: Thu, 13 Jun 2024 01:20:33 GMT  
		Size: 55.9 MB (55929392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:821aee856c729bd832b14ca707a0329f3bd8b297c10e83ad65d463a887c6080b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122164995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900c2fd919ec262abba050df8179b3456994f4ed1764832d0c8e52dfc9fe15dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5817662c9007e71058aef9f7c7d3931f04d9b6ebe960ed655bbe857daad9e757
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134610144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f4ebffb81ceb900b6653e82e4baef03422bb8488653295a9d3da2eb2f81abb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c87b179715aebeac49997fc2fc35590b0915357ea1f70d2fc616aa7a4d80f0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123056809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67375d8f56e852eac4e52ba0bd29d4c420f4a7b715068e92ff06c0ab7a7cf5f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:135be49be552feb6af1580b95462c1456db788d230f123d1e91677744c355dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f6c766d2340071d06e69ddab69dde8f348118050930de690cd448c4d66da1cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312095112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19d1123dc98839be934851144435b5375e3c1c28cc877de748cf1cc3ecf3250`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:59:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bc40752dd2cf0f18dcf07e73c1c85269734230ce7b22f18f4a4d120f54e608`  
		Last Modified: Tue, 14 May 2024 03:07:00 GMT  
		Size: 192.0 MB (191957446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff09ed26f09978f2506aab2a677256e431d42b649a990de694aaaeeef9c77bde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277928086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac0397ce0d875a3aff73514751b99eb6718c4af2e057c5f6d7f91d3f4f4cd32`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:27:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38716c4e5c9c098df6d6fe31c91df92948117751c7c1013c686dbf50412911c7`  
		Last Modified: Thu, 13 Jun 2024 01:35:42 GMT  
		Size: 47.4 MB (47411218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab4bbcbf00be5a105a2cebda6ada1b414a3d28291fd966b1738ab058d8851e`  
		Last Modified: Thu, 13 Jun 2024 01:36:16 GMT  
		Size: 168.2 MB (168170017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ac377838101002a2c4476832e37b148fc6f8d9afe88c32bc309edc8f5b6a6b8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302675972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e484f8a7fc76509c49428349168a71ad9a2d33963e7dada7d7508bc504775c45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:25:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afdcf6433347dce5e44f4ff0bc3de90b44a9fa538fa39a22d9b21f9ee5365d4`  
		Last Modified: Thu, 13 Jun 2024 01:32:18 GMT  
		Size: 52.2 MB (52231551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d462078a4e654dfe4d03086b828f77c76e47c0d5d14062aab137912bd0047683`  
		Last Modified: Thu, 13 Jun 2024 01:32:42 GMT  
		Size: 183.5 MB (183534120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4529e0e9fd84e87e73aff215e139080e163dd58f6fba754c6aad3f319ac26a8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321501563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff816cbeaf88f2d4d9f7ac1f222036ed2a211083066361364827029b0d34da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40f693ac8434364b7489c467dd31e0263396e4e0f3102204854d8530f11116f`  
		Last Modified: Thu, 13 Jun 2024 01:22:28 GMT  
		Size: 198.5 MB (198491652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:4c0c297bd2aab3401d945f9cf68887fbbc579c03e7a5f6b56e98539f8e7e3861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:19a2d958686d6939dbf5fa1594deeb163f77017bbfd9c8d89f7670a566bcc51d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc71f9e4bcb7ede51c9b809fada6708d652cf5ecdbf1cb837c36c1aa3b154a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b2b08e5f7d65e57a63584b81a2f05fc6772eb7a7f1fa2d4c1ddfdd33d82e8e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13269db2769cd336ff6d9cc88c9faf8953c1c9907361cef468f271064f526437`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0a12206ccc16be1f39097d53710a573d58d225fb96770065f783ac17adf5dada
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66910301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28be86697782ffdff28be275c56e51b574c799aceea87e8c6e2e5de642b36331`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aeb938e48735722eb9cff265ba97fbd08b28ec796222f5c1aa450f6eb0a0d3d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69518207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e623017bf02e26de81c186a51fa3c6c450384b948113c06ef36885c744a4d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:8c53a7e0190d12012da2b972d5e6d6f9899f507d976381246f4418eb7d8a1d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d6033b7f2d2dc5f9bf1860f5e59ebf4d4901774a9a6ac1d918ffc7213db46df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120137666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6549d95b040b11fe6a80c17ce9911246b5c40ea472af8a5f819e387c70128c94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89e831c74e06f0da076ba1cd9b94ea39b4cc812f83a01b73cdb45f8117719ef7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109758069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629a02dec12f34ac8b0e7d5296927fcaa21462913bb2277cf7d4de351d86b326`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38716c4e5c9c098df6d6fe31c91df92948117751c7c1013c686dbf50412911c7`  
		Last Modified: Thu, 13 Jun 2024 01:35:42 GMT  
		Size: 47.4 MB (47411218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:70b5b500a26771201bf14d42d178c1aa5947c2180ace836d958968d87e98c8bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119141852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a854abbbcc018be755cf89aa2c6799fb1ebbb42dec58ef32d1755febcf79969b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afdcf6433347dce5e44f4ff0bc3de90b44a9fa538fa39a22d9b21f9ee5365d4`  
		Last Modified: Thu, 13 Jun 2024 01:32:18 GMT  
		Size: 52.2 MB (52231551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aaf4ab111ccd4cc110ef841c71d265dbf97042efa29841b0e1ed4b55d2e7f083
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123009911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb6af7cbe4b117b6cba60a1c63815a41dc0add378ef6c1fdecc5cc66648686`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:231dfed2d44ccf0c0b589bb631cde1b5bdfe875f468cc13ea0e43b870d5ce18e
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
$ docker pull buildpack-deps@sha256:a69b982f62d7bb630caab917e4569cc560be701cd441d4aa2e8f1f8b111959df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73626490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455623d6bb6491f83205d9f69de70ed5a5bc70e61aac57d827e2efa733d75324`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:303b096eef41800a1c02bfcbb3dbc07bb67281e4f22b20f95c714835f7aa4eac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70066810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b56bd6b007ed413621e7a0b48f2d41fc6093153047c4a00cde86395796e29`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:80d27697996c7840c53a4342aa5464b325a25b220c873005fc1cf1b95be2c45f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67128818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbde1c9da59699fbc0c744a3c5438f5a8d013154787e1077c45f1526d1a58b0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db6be8e4d0ebef4a6af57304c890a87caea1988737d72c8972789ae4e5bdf6f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1655b481f30a7aa209f341e88541070569e03c3488c2fc0860e8546d81d080fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abd1412796e09c71e6a50980f7d3af6f136894c619abfae59c08cdf63891a9cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75490919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aae593ab7e2abe2d66141cae6dc3e52712746e79492516b4ba29d44d832376`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2c1e371988b4586288f0b89736f9ec00075c5a90ec207cf590c0982dc03e46e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73020502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c086dfa4c627be61aa7eb1c8515aa5597126a6533f7fbff8d2d83029dc223`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a33fd0d3726fed3d4bc388d8f0371396b35dbd572838c8ae08199b6348962e99
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79279424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fce485682ba3603437b1f85c5c3416023adeb67e564daebe1ffa69293fb4af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8eb4b2b46fb45c8d6ad4a25b823b73f75dc124aebc9a113da6229ff7e92bdfce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71989047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e515dfe7d427d18f2d8935ba66f12b8cc1602cae1f6413eae5977798c2dbc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
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
$ docker pull buildpack-deps@sha256:dbcaa5e6d9a2781212cf407729c39653cd32b2fc9c872d7b08f83c74697c65f1
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
$ docker pull buildpack-deps@sha256:045167f341265e83e50fcbc0739476bf0c2f9056e29d3edf85a810d33a6b99a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250119475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5603ea9d4e5f0860302e6cf426c1b9e0d54144f8c1ecbb1fcfd97e076b30faa4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:36:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed3c1f7e733f659785f3ec09fc5aafb7181463dfde5fd621ff4e755186f295c`  
		Last Modified: Wed, 05 Jun 2024 04:48:21 GMT  
		Size: 39.5 MB (39455122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59c778615bbd8bcc1be2d1888085cc6c6bf77a833779e4735d3976c6a7f7ef`  
		Last Modified: Wed, 05 Jun 2024 04:48:50 GMT  
		Size: 173.1 MB (173102637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7ac0497be5df83242ab5725cd28b64ffbdbe23c98b2d45456d6cbf1f7a176d1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217380055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1bf7033391d1a0b7cc1504eac0fa6cb1c2af14699869963af9880e2b07e228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:40:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca9608aaaded7216940920cf94566cf760f1f392ee5dcb044dffd51f2680344`  
		Last Modified: Wed, 05 Jun 2024 03:52:39 GMT  
		Size: 7.0 MB (7020980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b616962298953cec573067317321f9ed107e558b2aaa8c7f347d76f0129ebd9`  
		Last Modified: Wed, 05 Jun 2024 03:52:57 GMT  
		Size: 42.2 MB (42244717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e1e99ce186e310dbea71f5e194c20e0ae8ac0eff0f6ccd1439adc547184991`  
		Last Modified: Wed, 05 Jun 2024 03:53:24 GMT  
		Size: 140.6 MB (140579470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8740d6bcb54a076b11bb490e55a3af5c59a9c55f978a7eb2fa307640ab32e030
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241436596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6370b15f514326099ac8c4c3a558bb94d21c8e1c836cdbc491040755315b230a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:20:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcea6186f66b83759565293824604721be05055657a93197754d875e87759a3`  
		Last Modified: Wed, 05 Jun 2024 04:35:09 GMT  
		Size: 39.4 MB (39379473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d0ccb2a4ca3cac708a2c81e02a99813751e077a7558cf776e9ec6f0d48574`  
		Last Modified: Wed, 05 Jun 2024 04:35:33 GMT  
		Size: 166.6 MB (166584981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:35099699803f52697799371d71ca3a0bae89e112c13ea26b3116997a8a2e8073
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271240786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392776700688bd2613331e7b45d886a5e930bbc7ca2684ee1a97434a3bed4a2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:32:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c0335cfd20faf41c2684df8db8c0918fc181307423fe4a1ded886aa9f7918`  
		Last Modified: Wed, 05 Jun 2024 03:48:08 GMT  
		Size: 8.2 MB (8244447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a89acddeaf8bc6c6da6eb663640c72d2949562aa1209b43a9d83b6e4edb2f`  
		Last Modified: Wed, 05 Jun 2024 03:48:30 GMT  
		Size: 43.8 MB (43766282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18c46025e7dda290c1af9e27ec11bcf37af08631611eca1861819bbe77e8169`  
		Last Modified: Wed, 05 Jun 2024 03:49:05 GMT  
		Size: 183.6 MB (183641725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c7444befe6d944d10a9fb4ffd8b1b3f59cf8fd8fbcf3a7cdd3496315b08329ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223848864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02c9e254fc06ea48788748be5b571a06c32e5a72c91ed7eebdc6c170e7d3f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:25:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d1f4280511cf001472a1d4614c2482b39c5f1c36f22bdb5bdf1d80b6f34e1`  
		Last Modified: Wed, 05 Jun 2024 03:35:35 GMT  
		Size: 7.0 MB (7037156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d800481ca4a578ffd6afacde055d5c9b10f15aa78ed7e6f1f58003583f17ab0`  
		Last Modified: Wed, 05 Jun 2024 03:35:46 GMT  
		Size: 39.4 MB (39420378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8b47e75b6d22e0e3356eb110bee36d391172e58eec7a70d59e9b6a8aa219f0`  
		Last Modified: Wed, 05 Jun 2024 03:36:11 GMT  
		Size: 148.8 MB (148753931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:7779a591a40bfc86721dcbc2469adc533308056e5c6e7d674b89a04af56878f6
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
$ docker pull buildpack-deps@sha256:07cada24341288e2f2385b80b296dcb2bf94e13ba9370fd356d85cb1b18887db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37561716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f4668081a46b8c4134c13f9ac41f3bdb01170347d3f013436cc01b42bb5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bf8af84c64e569c3169c20c5c12e27b2869cdb73c88379cff4530418ffb26cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34555868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e057aece6c48fc6b656907bbeafb0862c0915a57b38a68c8a8d5cc0fa4ee47f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca9608aaaded7216940920cf94566cf760f1f392ee5dcb044dffd51f2680344`  
		Last Modified: Wed, 05 Jun 2024 03:52:39 GMT  
		Size: 7.0 MB (7020980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cbbd8a1f4560a08ebd715d246bd20d10753c50b8375de73afebda5f0d5d87c3f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35472142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444e5d79c70daed061f0ad6f19046b658de60a386af1502ef9b0d794794de955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:792e24bd13799c76879a0e6c5a61863c354cf7510f7e133bb490660368a1f23d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43832779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aba8a170045e6e319505c0d24c89181e999a4f34d96144f1f9c1cc257b36b3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c0335cfd20faf41c2684df8db8c0918fc181307423fe4a1ded886aa9f7918`  
		Last Modified: Wed, 05 Jun 2024 03:48:08 GMT  
		Size: 8.2 MB (8244447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9237ce3f5fcd17c4ff1d8162c7496b9664174362acaaf12ce58e122ce6b8d33a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35674555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfffd16e235800517314ce93c25987f978d9b772f1505c682c27c0ec36c862d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d1f4280511cf001472a1d4614c2482b39c5f1c36f22bdb5bdf1d80b6f34e1`  
		Last Modified: Wed, 05 Jun 2024 03:35:35 GMT  
		Size: 7.0 MB (7037156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:6af3f751b44d76d0baf982c2bbfaeb53371a8734c2e3d048d2b67ab46193d2aa
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
$ docker pull buildpack-deps@sha256:e36315391256b7d6a3ba998e79a79407cea73f31833db51054cc6026ba00f9e7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77016838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f80613a6709b5141dfdd2cdeece96d50d63beebb30174277191707e01e8a353`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed3c1f7e733f659785f3ec09fc5aafb7181463dfde5fd621ff4e755186f295c`  
		Last Modified: Wed, 05 Jun 2024 04:48:21 GMT  
		Size: 39.5 MB (39455122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8cd9d2105860c293542c7d8e47469dba804445be065563ab6a15324f34558b5b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76800585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cc51016500e4b010486cd9d8b6f6a99804f31527a8a2660c7097edfbd77d44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca9608aaaded7216940920cf94566cf760f1f392ee5dcb044dffd51f2680344`  
		Last Modified: Wed, 05 Jun 2024 03:52:39 GMT  
		Size: 7.0 MB (7020980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b616962298953cec573067317321f9ed107e558b2aaa8c7f347d76f0129ebd9`  
		Last Modified: Wed, 05 Jun 2024 03:52:57 GMT  
		Size: 42.2 MB (42244717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b9fddc77e5b4ac6c63e7dafd1fae57c12204a602d0cdef1031fcaf77ea25ec63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74851615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f159a46f5a8caa981a762f469ea255e46b32a780c2a3bc152c759b243ad91b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcea6186f66b83759565293824604721be05055657a93197754d875e87759a3`  
		Last Modified: Wed, 05 Jun 2024 04:35:09 GMT  
		Size: 39.4 MB (39379473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f38198fe72172fc55ee9693fc3090218c36c0f9652efff83e882194cb1c5d9c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87599061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081d69f98e0049b442e431ac29633f8d959ac27978b836dc78fdcb006110a210`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c0335cfd20faf41c2684df8db8c0918fc181307423fe4a1ded886aa9f7918`  
		Last Modified: Wed, 05 Jun 2024 03:48:08 GMT  
		Size: 8.2 MB (8244447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a89acddeaf8bc6c6da6eb663640c72d2949562aa1209b43a9d83b6e4edb2f`  
		Last Modified: Wed, 05 Jun 2024 03:48:30 GMT  
		Size: 43.8 MB (43766282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:11ff4021d9c999c9b1a47dbbfbe435f1eb91a4d5d23bace2679e05edc8bc0c04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75094933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89834543756364fdbc7fc709b2abe49c2064f33540fff730cddb5f90ed0cb35d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d1f4280511cf001472a1d4614c2482b39c5f1c36f22bdb5bdf1d80b6f34e1`  
		Last Modified: Wed, 05 Jun 2024 03:35:35 GMT  
		Size: 7.0 MB (7037156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d800481ca4a578ffd6afacde055d5c9b10f15aa78ed7e6f1f58003583f17ab0`  
		Last Modified: Wed, 05 Jun 2024 03:35:46 GMT  
		Size: 39.4 MB (39420378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:605f54c6cc897f95091bfb9972147f5de88ba0054278579b0fb12f9460b61401
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
$ docker pull buildpack-deps@sha256:1687ab7814a17df3aec0f31a20b31096b4b3361bacd3e7043787c8cd66fde314
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348976046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98709eacae3957ac0547846ed05ee63cc92428cbcdfc096c8ba12faf130cecd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c3e352f3d2eed4eda4feeed44a1022a881058df20ac0584db70c138b041e2`  
		Last Modified: Tue, 14 May 2024 03:05:02 GMT  
		Size: 211.2 MB (211207185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d992b823c77691e80a9731b308d4e6b56e46768cf3d026a0b7691daaa68efbd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316106610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137d197ce9f7674911d41eba9ebbcf2a0a7599ac8cc26d8b667b34b73e2767c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0475d9394b70464b90e234102b87625699171564d5f8cad8ec2f1d4de8fae2`  
		Last Modified: Thu, 13 Jun 2024 01:25:04 GMT  
		Size: 184.5 MB (184522344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fba40e013300dca943a346c53dfe423b82f7c9a46e86f260e65f761c376a3a4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301521074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c2e45bdfcb18fe68e2ffa3712c98ee0b3b4a394260f3d0f2626418a86c0f17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21d8970e0ba89fca18dc8a8432adc4570843d9db8e5e79d0ffb8099ce62748f`  
		Last Modified: Thu, 13 Jun 2024 01:34:03 GMT  
		Size: 175.2 MB (175175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b0d4f4ec2b8d73474c3cc9e0107ff9cc410fe737b23e618ee5502d7555b0567b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339788038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2ba4bdb71e9c0e6a4bd3fe19433338243cdc077789bbbd309588d18962d979`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222cb3bce424c387cc9f91f975242473b8be06d3426252fad4895105c051ad28`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 202.6 MB (202593329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:29414bea5343ab5bae4d1ee32c791dd2533ca26de259d76798a3ad5fe9279d4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351608036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1316642d0447c1d49296da3a2369562964bb569120c55c707de83aee2780157e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:07:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba812ec2feb1a698e5c5b1fda0a47d8bbba6cb3f887e520925c9fc376b01836`  
		Last Modified: Thu, 13 Jun 2024 01:20:01 GMT  
		Size: 210.1 MB (210128099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a4c89a334218312fd44b5f1d955cf30de87a03fc71c0ba36986383f6fa0a65f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325760195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d28dc9ef3fd0759c67fad11e737dabdf7b209dbcea9f335533d31f87f9e94d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:07:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3514ef59a25de65d0663fc4a360de7a712214c493290dd77858247edbd0dac`  
		Last Modified: Tue, 14 May 2024 11:40:05 GMT  
		Size: 189.8 MB (189771182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a544662c4f116d28f8d9392b218bbc9aea51cc8044fcb58153e3d5aa840ec8b7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363098165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01108acde413231d079df110cb9507133f84d976be2070d019e5814693cc74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:57:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80be54620660eb7b908f8c79a7ad14bedcac29ae46f620f4ede820441dc65d`  
		Last Modified: Tue, 14 May 2024 07:11:29 GMT  
		Size: 214.2 MB (214234653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d922b4f1ae136f4b4936921081d6d4fdd4f4f0e59502bb3cb09a7108979a23cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318356016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8130953b75a002b98650046e574455a2ad02eb7b9ee79889870697f5c0f7e51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:cd16e8a7877285c6b425da617bcbe0934864820cd39e6cd6dac94be66353080b
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
$ docker pull buildpack-deps@sha256:39e11b0343b39ba1729463f73ec8aa2f3192ae4db6df33d76ef6cf2d3556e99d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279881501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52f4321c594152af94c764f0cd48892290fa8ad5dfb752ac7af9b9c0d411d9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:41:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea509a29544edd67ece4c5006665316329880fdef08c2b42d62e31799e97bd9d`  
		Last Modified: Wed, 05 Jun 2024 04:49:16 GMT  
		Size: 44.8 MB (44778339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1086ac34d156d78afcae383fe5097fca7cdbccbfd64d127cd602668ce24cc1f`  
		Last Modified: Wed, 05 Jun 2024 04:49:48 GMT  
		Size: 197.2 MB (197154166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:15959ae0ea998982c4f9020b571c183a74b8ecd6173975dadf221a7b1172f8cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246497968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac5fadc348a3fa3c9c0ead1dc43b82d56a7d9bf9c632203e12e1787cd66406e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:45:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76642a0d8c917f8b4762138fba3c9de67689f5a5e5de9b64d3f6f72b20f70709`  
		Last Modified: Wed, 05 Jun 2024 03:53:52 GMT  
		Size: 48.9 MB (48942204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8865e47fb8518fbe3850de6b634b5678c01dd50ca46ea099fda5505a3460b2f`  
		Last Modified: Wed, 05 Jun 2024 03:54:21 GMT  
		Size: 162.7 MB (162714941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7f457a5344fd7435aad4d247de7e5c3d08dca96ec1e92001b2ab61ecda6cfdab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272058036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af0c0ee269d424283ceb8d57861c59cba924e5c4a445e47decf8fe5531fcd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:26:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a7640621fe982a10d3dda8496aea07502c6024b26780042604c39f807ebd4`  
		Last Modified: Wed, 05 Jun 2024 04:35:56 GMT  
		Size: 44.7 MB (44747249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6965e4a49555791cd958de7368bd1b08abb6d5e505e32016cd339f2851aa4cf`  
		Last Modified: Wed, 05 Jun 2024 04:36:22 GMT  
		Size: 190.3 MB (190264334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c5518ee43966f4d3aadc3036aed440186d365ac1c31e3537dd3873c9a702b57e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293830944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f909253f1cb306f8cc9d72a734c9aa127c4f96619e546a80603402f14165c71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:39:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb7ced059bf2a43a1fe9d833ce19fe75a8eaf293da574dd45c14836e77cdf4`  
		Last Modified: Wed, 05 Jun 2024 03:49:35 GMT  
		Size: 49.6 MB (49618077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7ee833f24770d2de6172bc5a24ff710d08064d7ed5d5c58cc56080e319e1f`  
		Last Modified: Wed, 05 Jun 2024 03:50:12 GMT  
		Size: 200.3 MB (200276421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8be834fc55e85de04be1a4be2b720b896375063e368195c5c61df37086dec2b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259174294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daafee1e2949c467e190a77fefda1291dc30bfc1d91720ac40807974b783772`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:29:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8180965f353999389ac9a5a3880e73af3fe29a168b55d1e7cf69c49184ef1d`  
		Last Modified: Wed, 05 Jun 2024 03:36:33 GMT  
		Size: 46.0 MB (46047739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6c8bf19011470468580af2c58176f51e586eef8ee879c216bc083a94efa7e`  
		Last Modified: Wed, 05 Jun 2024 03:37:00 GMT  
		Size: 175.5 MB (175476132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:64ff1d51b7db55077ca438e19afe2e88a08e0be2fcf5a79be2dc1228e246c6ec
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
$ docker pull buildpack-deps@sha256:9f65957280e34d727d025322bcf7d314be2ce0ae97063ce89e54ab88a65ff982
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37948996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d10deaee54420e6c10878f9ee930340477d0dc33c7423164068882dc40bbcf2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:585ae91beeff1e302e8fbffd7436e9db6f46e13a973139c2d4a56b34be0e8fc1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34840823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16789df5390866049611449ffd67171d93c081cf31f97b0e08cfd4464a55044f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:07a9da40434d6a8c2d5a35ca88d92f930ee9f1b6e7a65e8a6b02b4c44de57835
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37046453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d05d326c25364894e9f656270859b9ded72374cce2b4b34df0334f7001f943b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:49bc816c335208a1aa228d93eb5249ad6517463820a934617e7d29528f2b1e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43936446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5588bb15e96c780644c9ac6b12ff154eaeb9dfeb06b4e5bd45a117ad2671204`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d10b27e68cdbb7838a0eed6aa15639f6d6d4d98d060a945857105e94a0205a67
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37650423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee0ef73519b656095be7272b6cecb34c401a7c464dd7e85646659d8b55d566`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:16b936981452b9f44a0a58d93eed6d0a35006f36e6fe677bd073e94751c9b314
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
$ docker pull buildpack-deps@sha256:7ac32abbc5bd894e66ca36355e4212564fcd2887d97a91990b4ca4f7310cffe8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82727335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb289c2b2e169763b6524ce729573508c902bb6de42094621683a77c16840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea509a29544edd67ece4c5006665316329880fdef08c2b42d62e31799e97bd9d`  
		Last Modified: Wed, 05 Jun 2024 04:49:16 GMT  
		Size: 44.8 MB (44778339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dffdddc92193eb796ffb33065b30796f20d7c1df54f8671fca0fbbe6df617272
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83783027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec225f12da4434d781ad9b074870e390b9605010ac72f3262a67900eaf8b87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76642a0d8c917f8b4762138fba3c9de67689f5a5e5de9b64d3f6f72b20f70709`  
		Last Modified: Wed, 05 Jun 2024 03:53:52 GMT  
		Size: 48.9 MB (48942204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:825dfb37fcb76a6ccf6308a4dd9750b16454cef52968f7d78a658e6a864e02ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81793702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb2aa33211a1c117b30f56ba7edbdee935c9c5afed0dcdad799e3f0d6764541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a7640621fe982a10d3dda8496aea07502c6024b26780042604c39f807ebd4`  
		Last Modified: Wed, 05 Jun 2024 04:35:56 GMT  
		Size: 44.7 MB (44747249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2d41584f5bfc5f74f4c9ee4219d2aade02e1784f0d21489120454fa0324cc094
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93554523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5df9795dcc60d79106b41a88b1d51bc5d039e9e8d9c75343bb8e632b4d8813`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb7ced059bf2a43a1fe9d833ce19fe75a8eaf293da574dd45c14836e77cdf4`  
		Last Modified: Wed, 05 Jun 2024 03:49:35 GMT  
		Size: 49.6 MB (49618077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:81f715a4d61d44a0bf4f15848f950e8b70995191779291a6e65abe51232a7597
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83698162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370f2491b2f8c94c9a815eee1e1e01960197280f0ccae7e259ca143c5dd045ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8180965f353999389ac9a5a3880e73af3fe29a168b55d1e7cf69c49184ef1d`  
		Last Modified: Wed, 05 Jun 2024 03:36:33 GMT  
		Size: 46.0 MB (46047739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:9f35d074ab95834d6be3e55f54306ebe6bc53bf79e68601b46a8ba7f8cd4adfd
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
$ docker pull buildpack-deps@sha256:f3b09bda3b5c0919cd33180d172afb9ecd882a51269d6f4629a563f987e56072
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279729402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e4aeef9b47b481ea5ac3f679eaa9d4b0478067b672521cce966285f2c424a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:46:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87947638455b11c231fb8b483c07d47962e0468c49594803a3b86c4e901efba5`  
		Last Modified: Wed, 05 Jun 2024 04:49:57 GMT  
		Size: 14.5 MB (14471023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc27c5d51b891b5c5ef9ada2ceda9378dfeb6aaa6443443df4b986e5fd5aca5`  
		Last Modified: Wed, 05 Jun 2024 04:50:13 GMT  
		Size: 45.5 MB (45472926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974fa8c03c6f2f34a8f09b0645c4e1629876fc31b84c1d77684ec3eef5b343ed`  
		Last Modified: Wed, 05 Jun 2024 04:50:44 GMT  
		Size: 190.1 MB (190080677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1d37137547549d646fd57c80777473ef45ae08123b5ac09fbf5c4fde3067832f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239981834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ece3e854961aad2be5695cc18d54a9e4b7f8cc59e34f8d8fa83a93434b92b81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:50:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c8d02626362e73446fe59044c18a39c72b337463c7d3893055fa2f243d418`  
		Last Modified: Wed, 05 Jun 2024 03:54:49 GMT  
		Size: 49.0 MB (49014700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f34590d25db915d57bedf55001f29ec4ebdfb48c7ea83504b8482e68e45c0ba`  
		Last Modified: Wed, 05 Jun 2024 03:55:18 GMT  
		Size: 150.5 MB (150516385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8918e8ad34c286976bef24fb3a4d1d444e191b0a0ea2bbfa77062cb547b94a4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270819353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0589a5e0efcc86c91b3cda343b05e2911762976bd7e6cefb955b6ab7395c87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:33:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd7e72a53977344ea977a1fec5263450b6d1384d18ec232e10b2457a0e59d7`  
		Last Modified: Wed, 05 Jun 2024 04:36:32 GMT  
		Size: 14.3 MB (14303235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458f17b6ebb02a21b5aef3f00ad6e8c8df1dcf0ac11d9da63522e84c01392c96`  
		Last Modified: Wed, 05 Jun 2024 04:36:47 GMT  
		Size: 45.4 MB (45432069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccebc1c9f46d7f19aaf713f2fbf0f3783831ddaa6c5692c9ecb6c64ad4dd1ad`  
		Last Modified: Wed, 05 Jun 2024 04:37:12 GMT  
		Size: 182.0 MB (182040127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9619e7c9339fe5bdb325c8d01555ce2746158470af37a237ff1e3cf8b202a949
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299075645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdc7c63c45b23130d981ac8d546c3afcdaed68df9000044e7e2a5c7708517c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:46:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a2f6408ac8504d2696bad50727125bba3b8fcbd3f4cdb16db364d82f071b65`  
		Last Modified: Wed, 05 Jun 2024 03:50:44 GMT  
		Size: 50.7 MB (50707829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b25879c4fdce10703def064e54c010daf1b8184181400403c00faa9efd17e96`  
		Last Modified: Wed, 05 Jun 2024 03:51:22 GMT  
		Size: 196.8 MB (196751435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dddd9fe0920094e9fa26ae39d8dfc7d4bc5125416bdf0e36d08a7ebbd36d9e77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262135650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46582e245ff1dd4d81eb347b044e99e2f37966f0581b541e144665050b053d63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:33:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d620b15b28615214d0c65c6af1f9e67a03ef2f4b497937d254d6730cbfab1d8`  
		Last Modified: Wed, 05 Jun 2024 03:37:23 GMT  
		Size: 47.1 MB (47119774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cc128cc05544c139bf7bea282e63242ff37d44a9bb2ae723d3ca4960faf099`  
		Last Modified: Wed, 05 Jun 2024 03:37:50 GMT  
		Size: 169.3 MB (169340116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:039da1e7ebbd5f7fc301722b4b0d18e3cd55456f908abaae07f28628ab61b35b
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
$ docker pull buildpack-deps@sha256:b2dc16166dc335a8243b2c059e45f67ec2730b67af36d2ed46f8b64af7427f31
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44175799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbeab00184d80f11b993746c2f754e7409eb90af725db353ef314480890deeb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87947638455b11c231fb8b483c07d47962e0468c49594803a3b86c4e901efba5`  
		Last Modified: Wed, 05 Jun 2024 04:49:57 GMT  
		Size: 14.5 MB (14471023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:95473b4b84a9ecb58b5f00999164d858b82f209123c313edc3d59ccc17459e12
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40450749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7c54d27f963db7485deaf9d0b0e69078d4395ee7839f208c22b2c3b5dce577`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:10e9f558f47001d6f621d3cdbc3ea932ca1b645fe9bfe56e488a1ec4805072da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43347157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccffde84727391d35a03c3f7b8c0f9170c63d8e60bd2b8f14d7e0cfb7a74e219`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd7e72a53977344ea977a1fec5263450b6d1384d18ec232e10b2457a0e59d7`  
		Last Modified: Wed, 05 Jun 2024 04:36:32 GMT  
		Size: 14.3 MB (14303235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8427bfb305d7e972fd03e0fc0f799d537170330fa53f119a34b8452e0af5962c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51616381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c7168c2d96a978da33b4a6a45abd17e6f7b5470e186819b7272308b416ad74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0aded05b0749fd5bcf1b632be0ccb7a071c0a03403fe5e218e80cad3030d97f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45675760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8702617203377c2d995dd6ddf3bcc5b3af6717281b550a5e33ec66ac1eacf3ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:83787c9033f6651c6665db0b08a0f66857d74954c03f667d88a932cc46611171
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
$ docker pull buildpack-deps@sha256:c5e776d37879320ced0c09678ecc460340d40212e54ffbe5e698b508936ec1e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89648725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1585bd8d7b4034b37684810605e00e7ec1c968ba75ef062091feea7e066930`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87947638455b11c231fb8b483c07d47962e0468c49594803a3b86c4e901efba5`  
		Last Modified: Wed, 05 Jun 2024 04:49:57 GMT  
		Size: 14.5 MB (14471023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc27c5d51b891b5c5ef9ada2ceda9378dfeb6aaa6443443df4b986e5fd5aca5`  
		Last Modified: Wed, 05 Jun 2024 04:50:13 GMT  
		Size: 45.5 MB (45472926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8c02868790f8655786d780dffc39d21842375831267fe3124ab936f9dac3fac8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89465449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f32f7bdb3e04437215dfc7bd9bad8d6106895f414b066856629105d10050799`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c8d02626362e73446fe59044c18a39c72b337463c7d3893055fa2f243d418`  
		Last Modified: Wed, 05 Jun 2024 03:54:49 GMT  
		Size: 49.0 MB (49014700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:afa1ebd742604b095f4901cdb5171d6675ea594eb5ccc392b36a05bf4095a082
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88779226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff5a1ca5b3cbbbb79e03910f323884e2df231af55389389975fb5117f6ec911`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 04:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd7e72a53977344ea977a1fec5263450b6d1384d18ec232e10b2457a0e59d7`  
		Last Modified: Wed, 05 Jun 2024 04:36:32 GMT  
		Size: 14.3 MB (14303235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458f17b6ebb02a21b5aef3f00ad6e8c8df1dcf0ac11d9da63522e84c01392c96`  
		Last Modified: Wed, 05 Jun 2024 04:36:47 GMT  
		Size: 45.4 MB (45432069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d0f48e3478728a9701660e623006d9992d4fdf7f241c5891f16409282f9cbca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102324210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc277f900685ae7d741614024adea8818fe29ba0202c9dc9c245178fec3b51b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a2f6408ac8504d2696bad50727125bba3b8fcbd3f4cdb16db364d82f071b65`  
		Last Modified: Wed, 05 Jun 2024 03:50:44 GMT  
		Size: 50.7 MB (50707829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6ec31897dcd9987850bccd08acfa048868e830b0ab57816586a161c597975b9e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92795534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa38465a229c4d42a0140519a9a3f7dcab6f88ca6085473f76700c6f198dc4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d620b15b28615214d0c65c6af1f9e67a03ef2f4b497937d254d6730cbfab1d8`  
		Last Modified: Wed, 05 Jun 2024 03:37:23 GMT  
		Size: 47.1 MB (47119774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:135be49be552feb6af1580b95462c1456db788d230f123d1e91677744c355dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f6c766d2340071d06e69ddab69dde8f348118050930de690cd448c4d66da1cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312095112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19d1123dc98839be934851144435b5375e3c1c28cc877de748cf1cc3ecf3250`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:59:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bc40752dd2cf0f18dcf07e73c1c85269734230ce7b22f18f4a4d120f54e608`  
		Last Modified: Tue, 14 May 2024 03:07:00 GMT  
		Size: 192.0 MB (191957446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff09ed26f09978f2506aab2a677256e431d42b649a990de694aaaeeef9c77bde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277928086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac0397ce0d875a3aff73514751b99eb6718c4af2e057c5f6d7f91d3f4f4cd32`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:27:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38716c4e5c9c098df6d6fe31c91df92948117751c7c1013c686dbf50412911c7`  
		Last Modified: Thu, 13 Jun 2024 01:35:42 GMT  
		Size: 47.4 MB (47411218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab4bbcbf00be5a105a2cebda6ada1b414a3d28291fd966b1738ab058d8851e`  
		Last Modified: Thu, 13 Jun 2024 01:36:16 GMT  
		Size: 168.2 MB (168170017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ac377838101002a2c4476832e37b148fc6f8d9afe88c32bc309edc8f5b6a6b8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302675972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e484f8a7fc76509c49428349168a71ad9a2d33963e7dada7d7508bc504775c45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:25:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afdcf6433347dce5e44f4ff0bc3de90b44a9fa538fa39a22d9b21f9ee5365d4`  
		Last Modified: Thu, 13 Jun 2024 01:32:18 GMT  
		Size: 52.2 MB (52231551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d462078a4e654dfe4d03086b828f77c76e47c0d5d14062aab137912bd0047683`  
		Last Modified: Thu, 13 Jun 2024 01:32:42 GMT  
		Size: 183.5 MB (183534120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4529e0e9fd84e87e73aff215e139080e163dd58f6fba754c6aad3f319ac26a8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321501563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff816cbeaf88f2d4d9f7ac1f222036ed2a211083066361364827029b0d34da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40f693ac8434364b7489c467dd31e0263396e4e0f3102204854d8530f11116f`  
		Last Modified: Thu, 13 Jun 2024 01:22:28 GMT  
		Size: 198.5 MB (198491652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:4c0c297bd2aab3401d945f9cf68887fbbc579c03e7a5f6b56e98539f8e7e3861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:19a2d958686d6939dbf5fa1594deeb163f77017bbfd9c8d89f7670a566bcc51d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc71f9e4bcb7ede51c9b809fada6708d652cf5ecdbf1cb837c36c1aa3b154a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b2b08e5f7d65e57a63584b81a2f05fc6772eb7a7f1fa2d4c1ddfdd33d82e8e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13269db2769cd336ff6d9cc88c9faf8953c1c9907361cef468f271064f526437`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0a12206ccc16be1f39097d53710a573d58d225fb96770065f783ac17adf5dada
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66910301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28be86697782ffdff28be275c56e51b574c799aceea87e8c6e2e5de642b36331`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aeb938e48735722eb9cff265ba97fbd08b28ec796222f5c1aa450f6eb0a0d3d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69518207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e623017bf02e26de81c186a51fa3c6c450384b948113c06ef36885c744a4d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:8c53a7e0190d12012da2b972d5e6d6f9899f507d976381246f4418eb7d8a1d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d6033b7f2d2dc5f9bf1860f5e59ebf4d4901774a9a6ac1d918ffc7213db46df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120137666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6549d95b040b11fe6a80c17ce9911246b5c40ea472af8a5f819e387c70128c94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89e831c74e06f0da076ba1cd9b94ea39b4cc812f83a01b73cdb45f8117719ef7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109758069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629a02dec12f34ac8b0e7d5296927fcaa21462913bb2277cf7d4de351d86b326`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38716c4e5c9c098df6d6fe31c91df92948117751c7c1013c686dbf50412911c7`  
		Last Modified: Thu, 13 Jun 2024 01:35:42 GMT  
		Size: 47.4 MB (47411218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:70b5b500a26771201bf14d42d178c1aa5947c2180ace836d958968d87e98c8bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119141852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a854abbbcc018be755cf89aa2c6799fb1ebbb42dec58ef32d1755febcf79969b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afdcf6433347dce5e44f4ff0bc3de90b44a9fa538fa39a22d9b21f9ee5365d4`  
		Last Modified: Thu, 13 Jun 2024 01:32:18 GMT  
		Size: 52.2 MB (52231551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aaf4ab111ccd4cc110ef841c71d265dbf97042efa29841b0e1ed4b55d2e7f083
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123009911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb6af7cbe4b117b6cba60a1c63815a41dc0add378ef6c1fdecc5cc66648686`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:001b60168847adaca546117ccb57aee6bfe9f2435b39172f8ad3bbaca5bede77
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
$ docker pull buildpack-deps@sha256:e4d025916e47a96e384860b14a7b557682e34a9f7e898d60815a4408dfa0a042
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322467989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194ca5518838e2de21da2f6eaec2fa7aecd742455d5edc27148bc014aecfa113`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6043113e1c69109f845390049c3534bbf0249241ce681aafd8e6d4bc4306dcb2`  
		Last Modified: Tue, 14 May 2024 03:06:01 GMT  
		Size: 197.0 MB (197014118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b0b2a0e4e4799a38d68655af4fd07f31a710bccc18f59599a017a61f4950f430
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295524173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a766bf7f3d8dfcd47fb388a09c62067d8a9de3fb12889173ef3b584527a55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:17:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cab5068a9c028c7944d8c796ef2a3f2f0405e6777b233048bc9107bb87a65e`  
		Last Modified: Thu, 13 Jun 2024 01:25:35 GMT  
		Size: 52.3 MB (52330351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44e3b2454499d7c1424bf7ddc4cd476d1413aa087ad671dd79a68e82543870`  
		Last Modified: Thu, 13 Jun 2024 01:26:12 GMT  
		Size: 175.2 MB (175214715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b32db2f9c6af34e6038df7534fc819eb754d7f0fab6f4b357b43fa7a7a6d7c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282975663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4917bfe4856245bd09bc3f3722de40b3137927a58b107a049a3160efdd2a9813`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:25:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d33379b30e1ceb9b87b34482bff5906df43a22892099a6815c383a940044f8`  
		Last Modified: Thu, 13 Jun 2024 01:35:16 GMT  
		Size: 167.5 MB (167479604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4080cadee28202ed429666d670b3d1c1d92cc8c0688040c35f66c04d393d3fbb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314121806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64482ebb6c736604cbea29716fdc0834b3463956f14cc88a98999c97dd8ad9a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315e6e292ef6ca0113f94dbf806ecbea714420b97b385d4138e3cb84616995e3`  
		Last Modified: Thu, 13 Jun 2024 01:31:54 GMT  
		Size: 189.9 MB (189935383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:51507984c7f84283125a3a7218bad561d49bd684fe07717966557af083957584
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328192875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dbb2053708b8c142d26097a23648bfb41d722006f5daa020137f40705accfd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:11:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4e6f3cca702057a7a6cdbd9b2d2f758e1d85524fdc9fc26824db70376bce11`  
		Last Modified: Thu, 13 Jun 2024 01:20:33 GMT  
		Size: 55.9 MB (55929392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4267f96413a024e086769e096a862097360934db8c089f130cf1a23d340ab836`  
		Last Modified: Thu, 13 Jun 2024 01:21:16 GMT  
		Size: 199.9 MB (199918065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3f2ede943ad3e38ba4d4d4344842fe6ea87a61e4da4632c71d04247ae54724ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301297067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0333b5693b777f28d86f796678d85126330da0c996c232488eadd8708e7909`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:15:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5c693cc8c99f19e173787a1971e0d4a76aa939dbd2b62fe612add7ec9c0e7`  
		Last Modified: Tue, 14 May 2024 11:43:06 GMT  
		Size: 179.1 MB (179132072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a7e5a95fc3ce6a58d5d6488104b3f6e9074c08fa68e6e96cf7cb193a4f0c8059
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330973531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a982f067c0803b07d8fb756018b2a98406cde4858656d215dee4e9f781cb385`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:01:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d0e9056be49b56fb034ae67015f749411fff8fbd5b427d798c9847f60a8251`  
		Last Modified: Tue, 14 May 2024 07:12:37 GMT  
		Size: 196.4 MB (196363387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6df620f843eee47a26b4f082f55655756ad856b4b2b874f85d1f12dcc164917
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296082692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76854a8011768dd4c02eb73f732ff1c8787e3e6570c9a4338cf538aa254ab367`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:23:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c7ec963ac714a2f94b076f8e287270d7deb6f725c170e54c73463524ff8f0a`  
		Last Modified: Tue, 14 May 2024 01:30:55 GMT  
		Size: 173.0 MB (173025883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:bb0d17256fa57b9d6bacf1b74fddc8a510356161519a182dc28cf9e01c6c519c
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
$ docker pull buildpack-deps@sha256:0bf0aee11419e80a8fb33d389ead5f7968f48201150572d532da38bc1389aba9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70864266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0bdab4b2f868715425fb9150dba135510f9018a8785ac1090b9111a8910a21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2b2f1f685532327796e804134544ddfec3fde6773762e27096b0066a97fc52e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67979107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a1d4c7209fa1fbe40e1ee1325a134d9d96acc1d504361bf97e915c5c101c4f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e51ee971a62d9c5dab65dc9a1a66524ec3f1a31966334b215e47f32fb0897fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65136600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1d5a3aeba0427820070a3571004591e217c496fce7bbbbbb05f4d45984e71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9359bb6986f3f0ac4b4f1ec25c7f43779528d66b11e344603a5756ee6a6880eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69490048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d1fbcf54cfbbf4fd1ed5aa60b5733e4156545dec11b7f73364b2a3791ce3f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:23a702ab32e94ffed98ac05892a52e75723505616d572bf856c49ada8d7468c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72345418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7af04d557eded6f95a75be4618bd44bbd28b44b15adc95793da9d9f8b0a2dd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13748c446c41dab3c38922b2065bcc4bd2678076424a0001764069c527d2761d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68852398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63c8bec0b6ef36e7adf04e70dedeeee6c35be164dd1a3cb83f3d573fe87076`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:145755a231fddd2b044c4fbea7a3b42e0e6a1520fd6b41a9cdf73bb5cbec5d16
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75736359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7ae016308cd2d9178f4e3e52a44bdf2161d137139a59997200ed8be4176860`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4394c08db48cbf1e845fbfb3411ee8fec119006c580147493cf64d2f6c170652
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68979966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcb2524a0cd6b3cedc2e7cf1f359f191ee373805fd6a0d946661ff4e532c3b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:f7a2112a19163f18d7e27db7b5f22ce895c6bd4bdf16746065a8e10214e35d38
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
$ docker pull buildpack-deps@sha256:b9442185675e2e9874b661d6eec33ef42d5c5330fc73b0ddfe40074d49ed4642
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125453871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00afe6b457f0a039f2c3a3d817d46b533f25c54dfe23745575e7847d057f557f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:80fea9df2b0bd76af9b4344849e42a975859c4035b5f448f5063418de4c51569
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120309458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d957d7700016f5284abc1d02f1f63dee513923246df56449b954a86c38218949`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cab5068a9c028c7944d8c796ef2a3f2f0405e6777b233048bc9107bb87a65e`  
		Last Modified: Thu, 13 Jun 2024 01:25:35 GMT  
		Size: 52.3 MB (52330351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d02805b0cef84e51319634baccbd0f558c40bb630a39c563b6f6462ebaf8ffdc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115496059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e9b43fdc65ee88e04d5b4a276a84d014d45006160ff1ad4a42f75081def9ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:edb9eda62914d58ff0edb1fc4035cb32c24a3e50f676a8da8b64e7d0aeeed44a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124186423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba35868c87f3ab37b7d05c65c772d38d0b877bf1aeb211e5f298c3b5641dbbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0c519e89989efdac4290b4b0ea4aed2b2f2b94a00bc40e72c70a635c4cc85cf6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128274810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbfe0bd56d456be29159feb9764fa1d354e52dbf6e4c441978817e04929c6b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4e6f3cca702057a7a6cdbd9b2d2f758e1d85524fdc9fc26824db70376bce11`  
		Last Modified: Thu, 13 Jun 2024 01:20:33 GMT  
		Size: 55.9 MB (55929392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:821aee856c729bd832b14ca707a0329f3bd8b297c10e83ad65d463a887c6080b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122164995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900c2fd919ec262abba050df8179b3456994f4ed1764832d0c8e52dfc9fe15dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5817662c9007e71058aef9f7c7d3931f04d9b6ebe960ed655bbe857daad9e757
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134610144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f4ebffb81ceb900b6653e82e4baef03422bb8488653295a9d3da2eb2f81abb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c87b179715aebeac49997fc2fc35590b0915357ea1f70d2fc616aa7a4d80f0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123056809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67375d8f56e852eac4e52ba0bd29d4c420f4a7b715068e92ff06c0ab7a7cf5f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:a6d0207fe155f31e08a110c60ab94726f8f333ae6fab89b0ed5a20a555ee3430
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
$ docker pull buildpack-deps@sha256:cafa7552464a8e435f617ed9ce54db28cd69754040e60b3e1d8e3da9e240fb4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137768861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e822656587a2d640e11855cc11ae31480cfc3593678b3d6e7c221dcd215e71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:772c90ad5e828cf03adc31eb0a9fa1bdd4852259e4e5dbda10722ca4107bf0db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131584266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bc94d15114006a866db4bd4c7322ba8cb7db980f6fcc7576a60b49ab50fa21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:396d3e22ca837d6dc7fcbbc1eb72ddd0a287bdcc719a70e88b81da2d37ec30b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126346044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8771b9bbff94993882551c3970c872d8dbf62e2b6d78509f2b4d632f054b2fa1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bd92687ac56e76373303a1181e86f7e93fb7a2c7a3d248d04755ff557871290d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137194709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583fcf8f489e99fbb1dff9fae70e159d13c3b1e52012a1ef58deab3e9530429`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a88627846763b57606a8c341c6fefe0c692bbac1f4d632d206cc2997cab59e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141479937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a52dd664035d222019a260edd64c5ab6f717800cdcdca5fb1132d25886e3105`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:07:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8cf747af094998ee527bd33e348e9ef1c22c349757f3cde7ea7a0fe0a5b60fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135989013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1510421a679e334d18d89b5e06c07eb5401fa8dccbc83c12a27396d10b0950e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3b8246fbba99cc2e0111674a50e104b1d8137b9d16da58c380178086ef2bce0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148863512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bafc88136a64496ea3d6748a3c9a8fe760025c3d36d49e43e9da7352a658e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59256abb2252e0cda7425a81f7eb7e0b7f4d75fbf878b6bfda2e53dd42bcf37c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135119229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c8dd30373e0a52b50ba369650c99250c095db7eb2bad40372909251e1f35a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:8224ad404883c97eec11c4487defc24f4a135f8ba2db20d2183d45517b3b21a2
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
$ docker pull buildpack-deps@sha256:510629bf7ce9533a231f49951f789b23afdf54922c1505c96da14394e0222d5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 MB (390247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f61a281502e7231809486544e2dfc46a5b2be4dd982295d8a5670aa527f4445`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 02:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1c456d7bfe2b9bf229bd339b2bf174e56648e3dfbc34de48bd637651d2f40`  
		Last Modified: Tue, 14 May 2024 03:07:31 GMT  
		Size: 66.2 MB (66150169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac544ac355064026ba785eadccce3f97f0eaf50205a8f46a879294788785684b`  
		Last Modified: Tue, 14 May 2024 03:08:10 GMT  
		Size: 246.6 MB (246637499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:23742a24d183ff420647512e78ce459cb89eb479cea30d180cdec0175fc077b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345912159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c42b3df689e76f103c1d1bb86546c10817577f7bb4471423d09c057e1f925b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:21:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56a60eda8fe51134230ba91fc34d75d688a8e8668d0bc0836c49f14c886c82`  
		Last Modified: Thu, 13 Jun 2024 01:26:43 GMT  
		Size: 64.4 MB (64414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae581ede8f2c1d7302c93ac10d87cd470c5a5641bdbc563bc1606c09aa60177`  
		Last Modified: Thu, 13 Jun 2024 01:27:28 GMT  
		Size: 214.0 MB (214025639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:477914b6fbdfc2a5308d84f4d0557e828580fc5fb583a97d294638388eaba72d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326696137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794beec7cc73358bed5b7ff44b555cf6e4c8f21b8bc10dcce4f2f234d5cc7644`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:30:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3f6ffc5c655060a11e9801093c4f6da417ab1bd25c0ed1d7f810badd59a1e`  
		Last Modified: Thu, 13 Jun 2024 01:36:46 GMT  
		Size: 61.8 MB (61768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59e48a8a26ae4b39d549817d9f6485a412bea366150e0b4cf93a1dc2ff4c20c`  
		Last Modified: Thu, 13 Jun 2024 01:37:23 GMT  
		Size: 200.5 MB (200549606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daa240adc3a26e2cfccc8f82dd71f77925f6e95bc18d608dd874c8899a15943f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369902961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9399dafa2937341b2f8e58f15cff1becc501382148d41cfe86b2f9edcbdb6e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2611f13f4ded7c5c4db9cec62d32aa647f19b894c8d49a71181242d891cdaa`  
		Last Modified: Thu, 13 Jun 2024 01:33:37 GMT  
		Size: 231.5 MB (231457189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:333e240091ae3ba55acd6c3de0b1975631a7acd0458fb0a447556bc4617a26b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382952788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aeac83bac56baf8646254d28495861d39e591245e6bcc85a9fc2cf80e0079`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97408847bd4bc01a7750cb15d364c1b778603f2d0c10e350ab59c571a518c4f`  
		Last Modified: Thu, 13 Jun 2024 01:23:01 GMT  
		Size: 68.6 MB (68587764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a44d02da26a64e916b188437fc3eb829bf06dc211923352addff42906c24621`  
		Last Modified: Thu, 13 Jun 2024 01:23:52 GMT  
		Size: 241.0 MB (241023248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84e1d4e2b5b3643c67a7dec4bb189b32e2cff2f9c9500de31a98e0bf3c42f3df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359708966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867490fd8a8761f0b11b7e2ead79189e24a94657b0d08b60eecee6681c4a1d8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:27:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2989fc28155b5fa118ba37bab607b8e502b0c3d87d6857cadfcbb97fff7b9`  
		Last Modified: Tue, 14 May 2024 11:44:22 GMT  
		Size: 65.2 MB (65196404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0b2c691a41774071c0d9dd21f2ac31d580543d1b70cd9eb6e4ca27aae33b3`  
		Last Modified: Tue, 14 May 2024 11:46:47 GMT  
		Size: 217.7 MB (217669143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44994ebe239276f8c148f94904212fe0e082dd7a6a06509a0b841baba3204e9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.1 MB (404129957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c27e94800d6d03b5ef7856567848c95031b762ed4d0284cf0eff3b0c9d93ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:05:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb418175c6418b6d04d65091d4af4454b996b35118eb49bfd7288fa5a5eeaf`  
		Last Modified: Tue, 14 May 2024 07:13:09 GMT  
		Size: 71.7 MB (71704756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666e37da3df3c94824cb116466c272922f2a7c733cad8460357b2504dc816849`  
		Last Modified: Tue, 14 May 2024 07:13:53 GMT  
		Size: 248.9 MB (248903741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a8a6cba424fbb8acb65e7459c95265712378982cd5dfbbc849ab2fc0d182f18f
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.2 MB (425163913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c9e1fbf05033a4f4607b05de62de26b589467a64610c4aa368e44ed99ad6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:38:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee6c77bd5ae96b2a3d9ab1089946c965a1a40231cecbf5bd726f0d397837b2`  
		Last Modified: Tue, 14 May 2024 01:40:53 GMT  
		Size: 65.6 MB (65646012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe41b9eb8f07e9c6e67c4cf4ae6b4fe894f733f429286173f646100119905c`  
		Last Modified: Tue, 14 May 2024 01:45:57 GMT  
		Size: 284.5 MB (284524499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bc0f1580f7da7dd52f12f0fb6a45bc148ad7a5b1f37094d065634e86715364d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371563717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14b04d8b3d5f404a739ef30d225977273df38f670b35a7cdb00df85d22db2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1304310af4bca11dbfe21a9c4024e96521d8ac5f79eeb909c372706c5604a8`  
		Last Modified: Tue, 14 May 2024 01:31:19 GMT  
		Size: 67.5 MB (67453873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c512ee7e60445e2908d19d2738b076dfc41b764ba56a3e9509b8e8a8319a68`  
		Last Modified: Tue, 14 May 2024 01:31:53 GMT  
		Size: 226.3 MB (226268942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:639c568fb5e9efe5e00855ac7fa81a3bff1af12cecba6d7f7a4ddf2fcd925aae
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
$ docker pull buildpack-deps@sha256:d4940b76f809da1197d06e221d76a16f154fd99910005a1c2f7651772d7125a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77459604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0377e771a8165686d7b01131699352a03f3100e1b93531a23ed77ab1db9361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2727b522581a0e9d7e257ccaa991834af6fad6e44209e8339342c595ccf11160
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360d84e2c287393e6db6dfd2cb720264c45ee9f7f0d1c85135e8061dc40a060f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf257bbdb91866273bca56a40dd0290f25e4af8ac9569ecd3cb27493500f8ae4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64377753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f69a19347af70abb5d47d8401477a141e4acdea8fb3a2f3ba8cf5937aa01c9b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6883eaf68d2b828459a2901d2a401218c8d59a3edb2ab487d374300230f9c8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71454488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86afd40412d2678262f0f1f6ac3dfd9c7d739dcdec42cdd722003f7119be699`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a93d5eb754693132046b44e39b9895bf59057756f3d9d2afa9b661d0c3189d6c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73341776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900a196239184de5dd85c9ddddbd7d4b87efe0349298cc554566130f3d778991`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2a110606c0500501ab2283f8fd5f93387b7df8a4a764ffe33fe86b1daca59834
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76843419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc88dac12204d6c9e45e5df49ebdb34c3cdf7852c63478b1638d866e703dec7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:72b8bf372c37c39dcaae15721f9c6d237a4250a1b3a8d04880cdc1902f51f608
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83521460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a38354e5205110f751d5ab3755278ac1fb0a1b00900e2badecc806ced2ad3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2d71e44099f4aa392d0cf642f5fee30969cb1f140e417bb191651e88288a9ed6
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74993402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00d9e6291279d45ac74db77b396697e9458d7d76fe4f9bfe1080541b518ec2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d13b3b3fed7a5c88446c55e87f4cd26f81127cfada2b0a78434a934ed4c967e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd13938e979998201bdf409e7fd9c1432696ae28a2c50a7e76e28090a4625142`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:807d68f84f63c93381fe6397a41c78424abe337917844a0696abe2fb78c19649
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
$ docker pull buildpack-deps@sha256:1e3ca631311422e315676c930331a09897e7d5898bbe41a2ba0e7ba63905e2f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143609773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64e9a7ae7f6469eac6bf90e467c834468011edd15255f0e549f2cc50b9d854`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 02:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1c456d7bfe2b9bf229bd339b2bf174e56648e3dfbc34de48bd637651d2f40`  
		Last Modified: Tue, 14 May 2024 03:07:31 GMT  
		Size: 66.2 MB (66150169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:909cb9f1a10623e9c761927101e91287f44ab52bff44f94adaa99253cb589516
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131886520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2600724170e5a1e4a9386e07fb0ee5a5184861b1942cf0cdd49f29a4634614`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56a60eda8fe51134230ba91fc34d75d688a8e8668d0bc0836c49f14c886c82`  
		Last Modified: Thu, 13 Jun 2024 01:26:43 GMT  
		Size: 64.4 MB (64414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:408d27a2133cf51a03bc5eecfbdb39afcc210f8625c1d3ae8be4435e0c54f0d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126146531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310dc3a8ce2e4cb44ded5366bd44c40613e0916b145248fd6c4ace17dfc44d24`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3f6ffc5c655060a11e9801093c4f6da417ab1bd25c0ed1d7f810badd59a1e`  
		Last Modified: Thu, 13 Jun 2024 01:36:46 GMT  
		Size: 61.8 MB (61768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1cf41ee43f2dcebac58d3d31699511f01cb1fd6c33e6b87e9efaa2eb8c588c2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0753a5fa3df21365b12d290b55a52348ba29f83267c404d1b3a1b16cfc217`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:07fbf7ae17167ffeb7a74951ec46f9849000edc95e03dbe1c0f8b3ba64e56145
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141929540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080c12d20237b08343ef7ad97050a5e666eea3d177a34be4a6b5d2b5b0f78fd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97408847bd4bc01a7750cb15d364c1b778603f2d0c10e350ab59c571a518c4f`  
		Last Modified: Thu, 13 Jun 2024 01:23:01 GMT  
		Size: 68.6 MB (68587764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cc87cc93e6c5cdf8742d754c2d84fd9e166717917a1b2433ef9b53f4c73cec58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142039823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46be88449a9a4b2ac7783026c09f58b454209b63e3e33d62963e4cacdc579c65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2989fc28155b5fa118ba37bab607b8e502b0c3d87d6857cadfcbb97fff7b9`  
		Last Modified: Tue, 14 May 2024 11:44:22 GMT  
		Size: 65.2 MB (65196404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e9b6df3a59678eb610aafacb243928a39e9f386f7c0886d28421666f049b22be
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155226216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a86c3bb2022cc15ce35795687534202d8a99a852b457e1dbec39b4daeb701d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb418175c6418b6d04d65091d4af4454b996b35118eb49bfd7288fa5a5eeaf`  
		Last Modified: Tue, 14 May 2024 07:13:09 GMT  
		Size: 71.7 MB (71704756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f7a1aacae7ca04adeae11ca12635e611d0196f2c4d6d2f9f70b88dbe9eace5cf
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140639414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb9a2a02f5298cf8128e53b25754ff3ea4a28d32ea84bc618cb73c321d37fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee6c77bd5ae96b2a3d9ab1089946c965a1a40231cecbf5bd726f0d397837b2`  
		Last Modified: Tue, 14 May 2024 01:40:53 GMT  
		Size: 65.6 MB (65646012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41cf909b46af73d71ebfa9c9c0ac32fd9ff8404f5fdf01ce955a231a71542cf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145294775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a3b824b67d2afac3156b3f7551ff2584790a664671d72c836fba92989e5734`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1304310af4bca11dbfe21a9c4024e96521d8ac5f79eeb909c372706c5604a8`  
		Last Modified: Tue, 14 May 2024 01:31:19 GMT  
		Size: 67.5 MB (67453873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:605f54c6cc897f95091bfb9972147f5de88ba0054278579b0fb12f9460b61401
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
$ docker pull buildpack-deps@sha256:1687ab7814a17df3aec0f31a20b31096b4b3361bacd3e7043787c8cd66fde314
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348976046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98709eacae3957ac0547846ed05ee63cc92428cbcdfc096c8ba12faf130cecd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c3e352f3d2eed4eda4feeed44a1022a881058df20ac0584db70c138b041e2`  
		Last Modified: Tue, 14 May 2024 03:05:02 GMT  
		Size: 211.2 MB (211207185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d992b823c77691e80a9731b308d4e6b56e46768cf3d026a0b7691daaa68efbd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316106610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137d197ce9f7674911d41eba9ebbcf2a0a7599ac8cc26d8b667b34b73e2767c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0475d9394b70464b90e234102b87625699171564d5f8cad8ec2f1d4de8fae2`  
		Last Modified: Thu, 13 Jun 2024 01:25:04 GMT  
		Size: 184.5 MB (184522344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fba40e013300dca943a346c53dfe423b82f7c9a46e86f260e65f761c376a3a4a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301521074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c2e45bdfcb18fe68e2ffa3712c98ee0b3b4a394260f3d0f2626418a86c0f17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21d8970e0ba89fca18dc8a8432adc4570843d9db8e5e79d0ffb8099ce62748f`  
		Last Modified: Thu, 13 Jun 2024 01:34:03 GMT  
		Size: 175.2 MB (175175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b0d4f4ec2b8d73474c3cc9e0107ff9cc410fe737b23e618ee5502d7555b0567b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339788038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2ba4bdb71e9c0e6a4bd3fe19433338243cdc077789bbbd309588d18962d979`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222cb3bce424c387cc9f91f975242473b8be06d3426252fad4895105c051ad28`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 202.6 MB (202593329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:29414bea5343ab5bae4d1ee32c791dd2533ca26de259d76798a3ad5fe9279d4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351608036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1316642d0447c1d49296da3a2369562964bb569120c55c707de83aee2780157e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:07:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:09:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba812ec2feb1a698e5c5b1fda0a47d8bbba6cb3f887e520925c9fc376b01836`  
		Last Modified: Thu, 13 Jun 2024 01:20:01 GMT  
		Size: 210.1 MB (210128099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a4c89a334218312fd44b5f1d955cf30de87a03fc71c0ba36986383f6fa0a65f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325760195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d28dc9ef3fd0759c67fad11e737dabdf7b209dbcea9f335533d31f87f9e94d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:07:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3514ef59a25de65d0663fc4a360de7a712214c493290dd77858247edbd0dac`  
		Last Modified: Tue, 14 May 2024 11:40:05 GMT  
		Size: 189.8 MB (189771182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a544662c4f116d28f8d9392b218bbc9aea51cc8044fcb58153e3d5aa840ec8b7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363098165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01108acde413231d079df110cb9507133f84d976be2070d019e5814693cc74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:57:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80be54620660eb7b908f8c79a7ad14bedcac29ae46f620f4ede820441dc65d`  
		Last Modified: Tue, 14 May 2024 07:11:29 GMT  
		Size: 214.2 MB (214234653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d922b4f1ae136f4b4936921081d6d4fdd4f4f0e59502bb3cb09a7108979a23cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318356016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8130953b75a002b98650046e574455a2ad02eb7b9ee79889870697f5c0f7e51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:231dfed2d44ccf0c0b589bb631cde1b5bdfe875f468cc13ea0e43b870d5ce18e
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
$ docker pull buildpack-deps@sha256:a69b982f62d7bb630caab917e4569cc560be701cd441d4aa2e8f1f8b111959df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73626490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455623d6bb6491f83205d9f69de70ed5a5bc70e61aac57d827e2efa733d75324`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:303b096eef41800a1c02bfcbb3dbc07bb67281e4f22b20f95c714835f7aa4eac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70066810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b56bd6b007ed413621e7a0b48f2d41fc6093153047c4a00cde86395796e29`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:80d27697996c7840c53a4342aa5464b325a25b220c873005fc1cf1b95be2c45f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67128818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbde1c9da59699fbc0c744a3c5438f5a8d013154787e1077c45f1526d1a58b0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db6be8e4d0ebef4a6af57304c890a87caea1988737d72c8972789ae4e5bdf6f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1655b481f30a7aa209f341e88541070569e03c3488c2fc0860e8546d81d080fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abd1412796e09c71e6a50980f7d3af6f136894c619abfae59c08cdf63891a9cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75490919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aae593ab7e2abe2d66141cae6dc3e52712746e79492516b4ba29d44d832376`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2c1e371988b4586288f0b89736f9ec00075c5a90ec207cf590c0982dc03e46e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73020502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c086dfa4c627be61aa7eb1c8515aa5597126a6533f7fbff8d2d83029dc223`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a33fd0d3726fed3d4bc388d8f0371396b35dbd572838c8ae08199b6348962e99
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79279424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fce485682ba3603437b1f85c5c3416023adeb67e564daebe1ffa69293fb4af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8eb4b2b46fb45c8d6ad4a25b823b73f75dc124aebc9a113da6229ff7e92bdfce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71989047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e515dfe7d427d18f2d8935ba66f12b8cc1602cae1f6413eae5977798c2dbc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:a6d0207fe155f31e08a110c60ab94726f8f333ae6fab89b0ed5a20a555ee3430
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
$ docker pull buildpack-deps@sha256:cafa7552464a8e435f617ed9ce54db28cd69754040e60b3e1d8e3da9e240fb4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137768861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e822656587a2d640e11855cc11ae31480cfc3593678b3d6e7c221dcd215e71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:772c90ad5e828cf03adc31eb0a9fa1bdd4852259e4e5dbda10722ca4107bf0db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131584266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bc94d15114006a866db4bd4c7322ba8cb7db980f6fcc7576a60b49ab50fa21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:396d3e22ca837d6dc7fcbbc1eb72ddd0a287bdcc719a70e88b81da2d37ec30b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126346044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8771b9bbff94993882551c3970c872d8dbf62e2b6d78509f2b4d632f054b2fa1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:31 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Thu, 13 Jun 2024 00:57:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bd92687ac56e76373303a1181e86f7e93fb7a2c7a3d248d04755ff557871290d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137194709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583fcf8f489e99fbb1dff9fae70e159d13c3b1e52012a1ef58deab3e9530429`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a88627846763b57606a8c341c6fefe0c692bbac1f4d632d206cc2997cab59e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141479937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a52dd664035d222019a260edd64c5ab6f717800cdcdca5fb1132d25886e3105`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:46 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 13 Jun 2024 00:38:47 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:07:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8cf747af094998ee527bd33e348e9ef1c22c349757f3cde7ea7a0fe0a5b60fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135989013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1510421a679e334d18d89b5e06c07eb5401fa8dccbc83c12a27396d10b0950e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3b8246fbba99cc2e0111674a50e104b1d8137b9d16da58c380178086ef2bce0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148863512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bafc88136a64496ea3d6748a3c9a8fe760025c3d36d49e43e9da7352a658e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59256abb2252e0cda7425a81f7eb7e0b7f4d75fbf878b6bfda2e53dd42bcf37c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135119229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c8dd30373e0a52b50ba369650c99250c095db7eb2bad40372909251e1f35a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:f7fb20b09a5aaa4cb532be6e4b9d2c221c7cbe50fa40860cf837fde4d4ef3fee
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
$ docker pull buildpack-deps@sha256:a401721455f7cd3d304c82125885a0365f806debe4f5c4e20b29ebd2ce4aaa71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 MB (389791406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a2b5eb137453ffece174060255969de79c2dcd483596381d3dee274173e5a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:02:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9875430b07abbca2f54b7947832f4fbb3cd6cfb30ed102b17e5c02219d905d`  
		Last Modified: Tue, 14 May 2024 03:09:19 GMT  
		Size: 246.6 MB (246638653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:691ee229ebdd7db704cf488c4c65b015fd3f148f57764064ed7606b957a5ebce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346012868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebb0b0a27c1ed169e50e11db9ea570a2455ab53a86840c80a761b5b602d6c78`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:23:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec46f726aad0ec6492a2d4365f522b616a315262eae058ddae31bc48bb54536`  
		Last Modified: Thu, 13 Jun 2024 01:28:04 GMT  
		Size: 63.9 MB (63869461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f566f5647f549844c3114f30c34180fdc2fbf60373db5f8568cf8640c08acfb`  
		Last Modified: Thu, 13 Jun 2024 01:28:43 GMT  
		Size: 214.8 MB (214818434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e51af4938da7eae5a2731db67595e3a367250b460005520a5c6df3d91d6ad39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326769508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fba11ee4bacb01188d3fea61bdadf22c6249a1d10a60811df98d68e5f964e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:32:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1f736e76daaf801ffe0f5e18f4941fe63aa2a69c8cd6d41e58a0f35a8fbe86`  
		Last Modified: Thu, 13 Jun 2024 01:37:54 GMT  
		Size: 61.3 MB (61268135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a697d87d479ec6a0381ba0f5d19e355f93bc124e534f26d5e4a3258b33765`  
		Last Modified: Thu, 13 Jun 2024 01:38:35 GMT  
		Size: 201.3 MB (201277101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:74e90493e4b88de1d5f4bdab997cf68cff1a4a90235f148c421d9bd75ef85c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (369961938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e7bbe62b186251ff6708bbd2dcc44927924de7a0dafbe9acc2dc7efd9d7cc9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:29:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb32f6cc55be585ddde214c0068112a7e2fe0d22795409319c853d4d70757db7`  
		Last Modified: Thu, 13 Jun 2024 01:34:32 GMT  
		Size: 232.3 MB (232319137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7c0e45319c38b72c46ba31ce9e0bbeefdbd528f76e5f7e4f552f1883669ae8ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383055527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf25b60e38dd88e48e389387f8596930523a213ba06cd0eed4ae16ab1cc782`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fdde644c2537c8f96a9ec7f170c8d7998434f50a9cfebb6ede9ab2fbd6bbee`  
		Last Modified: Thu, 13 Jun 2024 01:24:27 GMT  
		Size: 67.9 MB (67907988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda544af678f150077336bae7b440115c498098fd52f36e0c9aef598688e21d3`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 242.0 MB (241966732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:57378db7f4c23f08e44ed387abce25dc157946c5d278e939c617d90a81d6399a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359235322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfd1ac2444346fa5faa73fee8ec7880ec8123e80e7fbb5a18cada43e1446190`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:36:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b2188576148a4180ee4eecdc60d183310d6da50fd577a6723544639ce191`  
		Last Modified: Tue, 14 May 2024 11:48:04 GMT  
		Size: 65.2 MB (65196959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd0490f57954354409d6530a9cee8fa6f67d1c87e7ad6f04857679d8210c2b`  
		Last Modified: Tue, 14 May 2024 11:50:30 GMT  
		Size: 217.7 MB (217662279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8a9fc4b0ddfa36db425e8b852ee1216cdcf85577a1b51f4cf6b073e9803d6b78
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403613644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b39bde83adcd03e2f6d7985f58e26d1b8dd832081a837d307ae4dcee6e70b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:09:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169ecdc07bedce89e0b8cdd6a09e00cecfd1b05f36ab6b7bcff1146b596777d`  
		Last Modified: Tue, 14 May 2024 07:14:26 GMT  
		Size: 71.7 MB (71710972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c804c1ff4e3c7dbd1fc56deb5f124b3b0c0ee135fad48f5777b22b5978eba636`  
		Last Modified: Tue, 14 May 2024 07:15:11 GMT  
		Size: 248.9 MB (248868485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f86256bb0174dc0a1bdb72c6c90ea174b8e42ca2656bf0a6327a79eb785cab83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371533960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbcab6a49e6679246b499f10a4946a4fc412b0bc67f4ceb3a5a6cbe6fe61599`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:26:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9cbe67e7bccd1433cf8a3d17879030af7f30729ba9616f025c0af6408214b7`  
		Last Modified: Tue, 14 May 2024 01:32:53 GMT  
		Size: 226.2 MB (226241254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:17e2446e63b1e7823519635831024697c59a0283c77a9c2df9ca53c06b6762d0
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
$ docker pull buildpack-deps@sha256:c660f96bdf8acb785cfbfd6ac0d68c7d8dd63a88884ba6eccf9db036c0875ebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77003837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313b5c46af83b08eeb74bf2683448dd049aea441d36a91cf66a8d67ea47de56f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:aeaf3f55b0e3a664abd6eec84e6c644234348a7f2af073d8b95966eb24931726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67324973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad76d64c3f4feb07e9e39361d872341106a4384b2bcffcc96718868496b3848`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c3c2d0172c1f96bb3f6fe6642ad60b077f1bd60837a4961442f434075218d9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64224272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0240b158ca01de67a1d7cd35d53ff9a5f4b7b4029fa4e95f0f5836d83298803`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a34c050a2acdfb8a3bb258beca9a4a587cb01039d379e95b4102451cbcd4f851
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4c9de2ca2a1fa682bcdd1352400587b9e254e9bffb1d3373dc43dd1db586c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cdbe30a0f3e833bc1134cf05690590b077194401ff05bd209f7dc5d16ca2369
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73180807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806f59aead0ee5dd5fae5e79c8102ba25a8a0627fed536080bee6a58ce53634`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13f073649092036357299277d04d7347ac4a7a70d90b4933e71daf6132143be7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76376084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da5697ef7d6a85b27bd6247774bb8050dac7e2aa75bf56acae14deb82e869ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7f3995ef2bfd3627cbb17c9038430063ddef76a0ef61ae9da9a469d4310eff20
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83034187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4795a36ee684164f7ee866ccf7900806708ac0d3e16315e774ebc57deabc2067`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21821cef67dbaf19dd6ab42d9b57bb10cf558b156869b3ba0f40276a3dc94ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77839233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96fad9bd52dcc2b83666a28ca8c7c4ee460c8493064bb9ec6e5b1d0d9ab825`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:87cc5cb73e9afb0a1d78dbf0f95fcba34667e7eaf7293b58c73b1e4dee5300a9
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
$ docker pull buildpack-deps@sha256:a34da2b9118ef97f6957c2679ef49fd464dba77f4ff6f319cc368a0208a8ccdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143152753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3a9948b9349fa7522fbdb1e093bc0e8f4c4f6e20eace5e7c5395e54a21e697`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d4eddc317c1626d430512efcd56711fbeb6b052430bf0eab58eaa6e7e09d3e1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131194434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd44a7db20e0827c98eedb880f842606707f49427f01dbda60a98f6b7a74535`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec46f726aad0ec6492a2d4365f522b616a315262eae058ddae31bc48bb54536`  
		Last Modified: Thu, 13 Jun 2024 01:28:04 GMT  
		Size: 63.9 MB (63869461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:218a78aa3747a001e7c44441197a0a9d951a5b61585a84fd2aba91ab38181f29
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125492407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e378133afaa75a5369d8bd2945c131aa46ad892500eba410f3dac977d2b4fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1f736e76daaf801ffe0f5e18f4941fe63aa2a69c8cd6d41e58a0f35a8fbe86`  
		Last Modified: Thu, 13 Jun 2024 01:37:54 GMT  
		Size: 61.3 MB (61268135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b41fff0b75cc30507ac62f4ac9a2880de7d734cc4cef4bb8a447d18e9edbe0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137642801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79c68243ec8ee65021f1ce3872499d665227b48543c6f16b5ed66449518f1da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6c4d4ebe4bfc568fd3648582fa49f610039786dea8e8bdb2e80252e5d22aa701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38566c60b6918b26840a47ec9109fdc647f311582ecc206134b5ce6688c8d08c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fdde644c2537c8f96a9ec7f170c8d7998434f50a9cfebb6ede9ab2fbd6bbee`  
		Last Modified: Thu, 13 Jun 2024 01:24:27 GMT  
		Size: 67.9 MB (67907988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6e04c5d621e0a6a9f69dd80fe0964942116ff2e89755c43ffcbdf67b3171c2d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141573043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c38199a3555ba63d7d336f29c424649fe338477854214bc9765d4d9e0a9407`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b2188576148a4180ee4eecdc60d183310d6da50fd577a6723544639ce191`  
		Last Modified: Tue, 14 May 2024 11:48:04 GMT  
		Size: 65.2 MB (65196959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:32baf20c2d82f32809fde80203a18549aedec9c918ea9231c91731c20d02c09d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154745159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328d204a07456036376484673dc1e889869487a0a8e0089bd5558e1871d40c52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169ecdc07bedce89e0b8cdd6a09e00cecfd1b05f36ab6b7bcff1146b596777d`  
		Last Modified: Tue, 14 May 2024 07:14:26 GMT  
		Size: 71.7 MB (71710972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e5c1a3992746e6832041bee53a8c59e76b89adf2545474dbc4535c28314d24d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145292706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e09e7693ba380c030f007b4b0993daa21b667a828f32c97efc09b9770fa9f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:f7fb20b09a5aaa4cb532be6e4b9d2c221c7cbe50fa40860cf837fde4d4ef3fee
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
$ docker pull buildpack-deps@sha256:a401721455f7cd3d304c82125885a0365f806debe4f5c4e20b29ebd2ce4aaa71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 MB (389791406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a2b5eb137453ffece174060255969de79c2dcd483596381d3dee274173e5a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:02:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9875430b07abbca2f54b7947832f4fbb3cd6cfb30ed102b17e5c02219d905d`  
		Last Modified: Tue, 14 May 2024 03:09:19 GMT  
		Size: 246.6 MB (246638653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:691ee229ebdd7db704cf488c4c65b015fd3f148f57764064ed7606b957a5ebce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346012868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebb0b0a27c1ed169e50e11db9ea570a2455ab53a86840c80a761b5b602d6c78`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:23:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec46f726aad0ec6492a2d4365f522b616a315262eae058ddae31bc48bb54536`  
		Last Modified: Thu, 13 Jun 2024 01:28:04 GMT  
		Size: 63.9 MB (63869461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f566f5647f549844c3114f30c34180fdc2fbf60373db5f8568cf8640c08acfb`  
		Last Modified: Thu, 13 Jun 2024 01:28:43 GMT  
		Size: 214.8 MB (214818434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e51af4938da7eae5a2731db67595e3a367250b460005520a5c6df3d91d6ad39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326769508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fba11ee4bacb01188d3fea61bdadf22c6249a1d10a60811df98d68e5f964e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:32:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1f736e76daaf801ffe0f5e18f4941fe63aa2a69c8cd6d41e58a0f35a8fbe86`  
		Last Modified: Thu, 13 Jun 2024 01:37:54 GMT  
		Size: 61.3 MB (61268135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a697d87d479ec6a0381ba0f5d19e355f93bc124e534f26d5e4a3258b33765`  
		Last Modified: Thu, 13 Jun 2024 01:38:35 GMT  
		Size: 201.3 MB (201277101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:74e90493e4b88de1d5f4bdab997cf68cff1a4a90235f148c421d9bd75ef85c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (369961938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e7bbe62b186251ff6708bbd2dcc44927924de7a0dafbe9acc2dc7efd9d7cc9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:29:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb32f6cc55be585ddde214c0068112a7e2fe0d22795409319c853d4d70757db7`  
		Last Modified: Thu, 13 Jun 2024 01:34:32 GMT  
		Size: 232.3 MB (232319137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7c0e45319c38b72c46ba31ce9e0bbeefdbd528f76e5f7e4f552f1883669ae8ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383055527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf25b60e38dd88e48e389387f8596930523a213ba06cd0eed4ae16ab1cc782`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fdde644c2537c8f96a9ec7f170c8d7998434f50a9cfebb6ede9ab2fbd6bbee`  
		Last Modified: Thu, 13 Jun 2024 01:24:27 GMT  
		Size: 67.9 MB (67907988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda544af678f150077336bae7b440115c498098fd52f36e0c9aef598688e21d3`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 242.0 MB (241966732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:57378db7f4c23f08e44ed387abce25dc157946c5d278e939c617d90a81d6399a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359235322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfd1ac2444346fa5faa73fee8ec7880ec8123e80e7fbb5a18cada43e1446190`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:36:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b2188576148a4180ee4eecdc60d183310d6da50fd577a6723544639ce191`  
		Last Modified: Tue, 14 May 2024 11:48:04 GMT  
		Size: 65.2 MB (65196959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd0490f57954354409d6530a9cee8fa6f67d1c87e7ad6f04857679d8210c2b`  
		Last Modified: Tue, 14 May 2024 11:50:30 GMT  
		Size: 217.7 MB (217662279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8a9fc4b0ddfa36db425e8b852ee1216cdcf85577a1b51f4cf6b073e9803d6b78
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403613644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b39bde83adcd03e2f6d7985f58e26d1b8dd832081a837d307ae4dcee6e70b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:09:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169ecdc07bedce89e0b8cdd6a09e00cecfd1b05f36ab6b7bcff1146b596777d`  
		Last Modified: Tue, 14 May 2024 07:14:26 GMT  
		Size: 71.7 MB (71710972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c804c1ff4e3c7dbd1fc56deb5f124b3b0c0ee135fad48f5777b22b5978eba636`  
		Last Modified: Tue, 14 May 2024 07:15:11 GMT  
		Size: 248.9 MB (248868485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f86256bb0174dc0a1bdb72c6c90ea174b8e42ca2656bf0a6327a79eb785cab83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371533960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbcab6a49e6679246b499f10a4946a4fc412b0bc67f4ceb3a5a6cbe6fe61599`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:26:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9cbe67e7bccd1433cf8a3d17879030af7f30729ba9616f025c0af6408214b7`  
		Last Modified: Tue, 14 May 2024 01:32:53 GMT  
		Size: 226.2 MB (226241254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:17e2446e63b1e7823519635831024697c59a0283c77a9c2df9ca53c06b6762d0
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
$ docker pull buildpack-deps@sha256:c660f96bdf8acb785cfbfd6ac0d68c7d8dd63a88884ba6eccf9db036c0875ebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77003837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313b5c46af83b08eeb74bf2683448dd049aea441d36a91cf66a8d67ea47de56f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:aeaf3f55b0e3a664abd6eec84e6c644234348a7f2af073d8b95966eb24931726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67324973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad76d64c3f4feb07e9e39361d872341106a4384b2bcffcc96718868496b3848`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c3c2d0172c1f96bb3f6fe6642ad60b077f1bd60837a4961442f434075218d9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64224272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0240b158ca01de67a1d7cd35d53ff9a5f4b7b4029fa4e95f0f5836d83298803`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a34c050a2acdfb8a3bb258beca9a4a587cb01039d379e95b4102451cbcd4f851
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4c9de2ca2a1fa682bcdd1352400587b9e254e9bffb1d3373dc43dd1db586c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cdbe30a0f3e833bc1134cf05690590b077194401ff05bd209f7dc5d16ca2369
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73180807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806f59aead0ee5dd5fae5e79c8102ba25a8a0627fed536080bee6a58ce53634`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13f073649092036357299277d04d7347ac4a7a70d90b4933e71daf6132143be7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76376084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da5697ef7d6a85b27bd6247774bb8050dac7e2aa75bf56acae14deb82e869ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7f3995ef2bfd3627cbb17c9038430063ddef76a0ef61ae9da9a469d4310eff20
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83034187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4795a36ee684164f7ee866ccf7900806708ac0d3e16315e774ebc57deabc2067`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21821cef67dbaf19dd6ab42d9b57bb10cf558b156869b3ba0f40276a3dc94ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77839233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96fad9bd52dcc2b83666a28ca8c7c4ee460c8493064bb9ec6e5b1d0d9ab825`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:87cc5cb73e9afb0a1d78dbf0f95fcba34667e7eaf7293b58c73b1e4dee5300a9
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
$ docker pull buildpack-deps@sha256:a34da2b9118ef97f6957c2679ef49fd464dba77f4ff6f319cc368a0208a8ccdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143152753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3a9948b9349fa7522fbdb1e093bc0e8f4c4f6e20eace5e7c5395e54a21e697`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d4eddc317c1626d430512efcd56711fbeb6b052430bf0eab58eaa6e7e09d3e1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131194434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd44a7db20e0827c98eedb880f842606707f49427f01dbda60a98f6b7a74535`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec46f726aad0ec6492a2d4365f522b616a315262eae058ddae31bc48bb54536`  
		Last Modified: Thu, 13 Jun 2024 01:28:04 GMT  
		Size: 63.9 MB (63869461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:218a78aa3747a001e7c44441197a0a9d951a5b61585a84fd2aba91ab38181f29
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125492407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e378133afaa75a5369d8bd2945c131aa46ad892500eba410f3dac977d2b4fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1f736e76daaf801ffe0f5e18f4941fe63aa2a69c8cd6d41e58a0f35a8fbe86`  
		Last Modified: Thu, 13 Jun 2024 01:37:54 GMT  
		Size: 61.3 MB (61268135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b41fff0b75cc30507ac62f4ac9a2880de7d734cc4cef4bb8a447d18e9edbe0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137642801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79c68243ec8ee65021f1ce3872499d665227b48543c6f16b5ed66449518f1da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6c4d4ebe4bfc568fd3648582fa49f610039786dea8e8bdb2e80252e5d22aa701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38566c60b6918b26840a47ec9109fdc647f311582ecc206134b5ce6688c8d08c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fdde644c2537c8f96a9ec7f170c8d7998434f50a9cfebb6ede9ab2fbd6bbee`  
		Last Modified: Thu, 13 Jun 2024 01:24:27 GMT  
		Size: 67.9 MB (67907988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6e04c5d621e0a6a9f69dd80fe0964942116ff2e89755c43ffcbdf67b3171c2d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141573043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c38199a3555ba63d7d336f29c424649fe338477854214bc9765d4d9e0a9407`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b2188576148a4180ee4eecdc60d183310d6da50fd577a6723544639ce191`  
		Last Modified: Tue, 14 May 2024 11:48:04 GMT  
		Size: 65.2 MB (65196959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:32baf20c2d82f32809fde80203a18549aedec9c918ea9231c91731c20d02c09d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154745159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328d204a07456036376484673dc1e889869487a0a8e0089bd5558e1871d40c52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169ecdc07bedce89e0b8cdd6a09e00cecfd1b05f36ab6b7bcff1146b596777d`  
		Last Modified: Tue, 14 May 2024 07:14:26 GMT  
		Size: 71.7 MB (71710972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e5c1a3992746e6832041bee53a8c59e76b89adf2545474dbc4535c28314d24d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145292706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e09e7693ba380c030f007b4b0993daa21b667a828f32c97efc09b9770fa9f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:8224ad404883c97eec11c4487defc24f4a135f8ba2db20d2183d45517b3b21a2
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
$ docker pull buildpack-deps@sha256:510629bf7ce9533a231f49951f789b23afdf54922c1505c96da14394e0222d5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 MB (390247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f61a281502e7231809486544e2dfc46a5b2be4dd982295d8a5670aa527f4445`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 02:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1c456d7bfe2b9bf229bd339b2bf174e56648e3dfbc34de48bd637651d2f40`  
		Last Modified: Tue, 14 May 2024 03:07:31 GMT  
		Size: 66.2 MB (66150169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac544ac355064026ba785eadccce3f97f0eaf50205a8f46a879294788785684b`  
		Last Modified: Tue, 14 May 2024 03:08:10 GMT  
		Size: 246.6 MB (246637499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:23742a24d183ff420647512e78ce459cb89eb479cea30d180cdec0175fc077b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345912159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c42b3df689e76f103c1d1bb86546c10817577f7bb4471423d09c057e1f925b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:21:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56a60eda8fe51134230ba91fc34d75d688a8e8668d0bc0836c49f14c886c82`  
		Last Modified: Thu, 13 Jun 2024 01:26:43 GMT  
		Size: 64.4 MB (64414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae581ede8f2c1d7302c93ac10d87cd470c5a5641bdbc563bc1606c09aa60177`  
		Last Modified: Thu, 13 Jun 2024 01:27:28 GMT  
		Size: 214.0 MB (214025639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:477914b6fbdfc2a5308d84f4d0557e828580fc5fb583a97d294638388eaba72d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326696137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794beec7cc73358bed5b7ff44b555cf6e4c8f21b8bc10dcce4f2f234d5cc7644`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:30:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3f6ffc5c655060a11e9801093c4f6da417ab1bd25c0ed1d7f810badd59a1e`  
		Last Modified: Thu, 13 Jun 2024 01:36:46 GMT  
		Size: 61.8 MB (61768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59e48a8a26ae4b39d549817d9f6485a412bea366150e0b4cf93a1dc2ff4c20c`  
		Last Modified: Thu, 13 Jun 2024 01:37:23 GMT  
		Size: 200.5 MB (200549606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daa240adc3a26e2cfccc8f82dd71f77925f6e95bc18d608dd874c8899a15943f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369902961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9399dafa2937341b2f8e58f15cff1becc501382148d41cfe86b2f9edcbdb6e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2611f13f4ded7c5c4db9cec62d32aa647f19b894c8d49a71181242d891cdaa`  
		Last Modified: Thu, 13 Jun 2024 01:33:37 GMT  
		Size: 231.5 MB (231457189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:333e240091ae3ba55acd6c3de0b1975631a7acd0458fb0a447556bc4617a26b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382952788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aeac83bac56baf8646254d28495861d39e591245e6bcc85a9fc2cf80e0079`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97408847bd4bc01a7750cb15d364c1b778603f2d0c10e350ab59c571a518c4f`  
		Last Modified: Thu, 13 Jun 2024 01:23:01 GMT  
		Size: 68.6 MB (68587764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a44d02da26a64e916b188437fc3eb829bf06dc211923352addff42906c24621`  
		Last Modified: Thu, 13 Jun 2024 01:23:52 GMT  
		Size: 241.0 MB (241023248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84e1d4e2b5b3643c67a7dec4bb189b32e2cff2f9c9500de31a98e0bf3c42f3df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359708966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867490fd8a8761f0b11b7e2ead79189e24a94657b0d08b60eecee6681c4a1d8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:27:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2989fc28155b5fa118ba37bab607b8e502b0c3d87d6857cadfcbb97fff7b9`  
		Last Modified: Tue, 14 May 2024 11:44:22 GMT  
		Size: 65.2 MB (65196404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0b2c691a41774071c0d9dd21f2ac31d580543d1b70cd9eb6e4ca27aae33b3`  
		Last Modified: Tue, 14 May 2024 11:46:47 GMT  
		Size: 217.7 MB (217669143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44994ebe239276f8c148f94904212fe0e082dd7a6a06509a0b841baba3204e9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.1 MB (404129957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c27e94800d6d03b5ef7856567848c95031b762ed4d0284cf0eff3b0c9d93ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:05:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb418175c6418b6d04d65091d4af4454b996b35118eb49bfd7288fa5a5eeaf`  
		Last Modified: Tue, 14 May 2024 07:13:09 GMT  
		Size: 71.7 MB (71704756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666e37da3df3c94824cb116466c272922f2a7c733cad8460357b2504dc816849`  
		Last Modified: Tue, 14 May 2024 07:13:53 GMT  
		Size: 248.9 MB (248903741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a8a6cba424fbb8acb65e7459c95265712378982cd5dfbbc849ab2fc0d182f18f
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.2 MB (425163913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c9e1fbf05033a4f4607b05de62de26b589467a64610c4aa368e44ed99ad6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:38:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee6c77bd5ae96b2a3d9ab1089946c965a1a40231cecbf5bd726f0d397837b2`  
		Last Modified: Tue, 14 May 2024 01:40:53 GMT  
		Size: 65.6 MB (65646012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe41b9eb8f07e9c6e67c4cf4ae6b4fe894f733f429286173f646100119905c`  
		Last Modified: Tue, 14 May 2024 01:45:57 GMT  
		Size: 284.5 MB (284524499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bc0f1580f7da7dd52f12f0fb6a45bc148ad7a5b1f37094d065634e86715364d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371563717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14b04d8b3d5f404a739ef30d225977273df38f670b35a7cdb00df85d22db2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1304310af4bca11dbfe21a9c4024e96521d8ac5f79eeb909c372706c5604a8`  
		Last Modified: Tue, 14 May 2024 01:31:19 GMT  
		Size: 67.5 MB (67453873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c512ee7e60445e2908d19d2738b076dfc41b764ba56a3e9509b8e8a8319a68`  
		Last Modified: Tue, 14 May 2024 01:31:53 GMT  
		Size: 226.3 MB (226268942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:639c568fb5e9efe5e00855ac7fa81a3bff1af12cecba6d7f7a4ddf2fcd925aae
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
$ docker pull buildpack-deps@sha256:d4940b76f809da1197d06e221d76a16f154fd99910005a1c2f7651772d7125a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77459604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0377e771a8165686d7b01131699352a03f3100e1b93531a23ed77ab1db9361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2727b522581a0e9d7e257ccaa991834af6fad6e44209e8339342c595ccf11160
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360d84e2c287393e6db6dfd2cb720264c45ee9f7f0d1c85135e8061dc40a060f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf257bbdb91866273bca56a40dd0290f25e4af8ac9569ecd3cb27493500f8ae4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64377753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f69a19347af70abb5d47d8401477a141e4acdea8fb3a2f3ba8cf5937aa01c9b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6883eaf68d2b828459a2901d2a401218c8d59a3edb2ab487d374300230f9c8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71454488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86afd40412d2678262f0f1f6ac3dfd9c7d739dcdec42cdd722003f7119be699`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a93d5eb754693132046b44e39b9895bf59057756f3d9d2afa9b661d0c3189d6c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73341776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900a196239184de5dd85c9ddddbd7d4b87efe0349298cc554566130f3d778991`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2a110606c0500501ab2283f8fd5f93387b7df8a4a764ffe33fe86b1daca59834
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76843419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc88dac12204d6c9e45e5df49ebdb34c3cdf7852c63478b1638d866e703dec7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:72b8bf372c37c39dcaae15721f9c6d237a4250a1b3a8d04880cdc1902f51f608
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83521460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a38354e5205110f751d5ab3755278ac1fb0a1b00900e2badecc806ced2ad3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2d71e44099f4aa392d0cf642f5fee30969cb1f140e417bb191651e88288a9ed6
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74993402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00d9e6291279d45ac74db77b396697e9458d7d76fe4f9bfe1080541b518ec2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d13b3b3fed7a5c88446c55e87f4cd26f81127cfada2b0a78434a934ed4c967e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd13938e979998201bdf409e7fd9c1432696ae28a2c50a7e76e28090a4625142`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:807d68f84f63c93381fe6397a41c78424abe337917844a0696abe2fb78c19649
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
$ docker pull buildpack-deps@sha256:1e3ca631311422e315676c930331a09897e7d5898bbe41a2ba0e7ba63905e2f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143609773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64e9a7ae7f6469eac6bf90e467c834468011edd15255f0e549f2cc50b9d854`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 02:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1c456d7bfe2b9bf229bd339b2bf174e56648e3dfbc34de48bd637651d2f40`  
		Last Modified: Tue, 14 May 2024 03:07:31 GMT  
		Size: 66.2 MB (66150169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:909cb9f1a10623e9c761927101e91287f44ab52bff44f94adaa99253cb589516
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131886520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2600724170e5a1e4a9386e07fb0ee5a5184861b1942cf0cdd49f29a4634614`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56a60eda8fe51134230ba91fc34d75d688a8e8668d0bc0836c49f14c886c82`  
		Last Modified: Thu, 13 Jun 2024 01:26:43 GMT  
		Size: 64.4 MB (64414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:408d27a2133cf51a03bc5eecfbdb39afcc210f8625c1d3ae8be4435e0c54f0d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126146531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310dc3a8ce2e4cb44ded5366bd44c40613e0916b145248fd6c4ace17dfc44d24`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3f6ffc5c655060a11e9801093c4f6da417ab1bd25c0ed1d7f810badd59a1e`  
		Last Modified: Thu, 13 Jun 2024 01:36:46 GMT  
		Size: 61.8 MB (61768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1cf41ee43f2dcebac58d3d31699511f01cb1fd6c33e6b87e9efaa2eb8c588c2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0753a5fa3df21365b12d290b55a52348ba29f83267c404d1b3a1b16cfc217`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:07fbf7ae17167ffeb7a74951ec46f9849000edc95e03dbe1c0f8b3ba64e56145
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141929540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080c12d20237b08343ef7ad97050a5e666eea3d177a34be4a6b5d2b5b0f78fd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97408847bd4bc01a7750cb15d364c1b778603f2d0c10e350ab59c571a518c4f`  
		Last Modified: Thu, 13 Jun 2024 01:23:01 GMT  
		Size: 68.6 MB (68587764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cc87cc93e6c5cdf8742d754c2d84fd9e166717917a1b2433ef9b53f4c73cec58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142039823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46be88449a9a4b2ac7783026c09f58b454209b63e3e33d62963e4cacdc579c65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2989fc28155b5fa118ba37bab607b8e502b0c3d87d6857cadfcbb97fff7b9`  
		Last Modified: Tue, 14 May 2024 11:44:22 GMT  
		Size: 65.2 MB (65196404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e9b6df3a59678eb610aafacb243928a39e9f386f7c0886d28421666f049b22be
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155226216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a86c3bb2022cc15ce35795687534202d8a99a852b457e1dbec39b4daeb701d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb418175c6418b6d04d65091d4af4454b996b35118eb49bfd7288fa5a5eeaf`  
		Last Modified: Tue, 14 May 2024 07:13:09 GMT  
		Size: 71.7 MB (71704756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f7a1aacae7ca04adeae11ca12635e611d0196f2c4d6d2f9f70b88dbe9eace5cf
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140639414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb9a2a02f5298cf8128e53b25754ff3ea4a28d32ea84bc618cb73c321d37fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee6c77bd5ae96b2a3d9ab1089946c965a1a40231cecbf5bd726f0d397837b2`  
		Last Modified: Tue, 14 May 2024 01:40:53 GMT  
		Size: 65.6 MB (65646012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41cf909b46af73d71ebfa9c9c0ac32fd9ff8404f5fdf01ce955a231a71542cf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145294775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a3b824b67d2afac3156b3f7551ff2584790a664671d72c836fba92989e5734`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1304310af4bca11dbfe21a9c4024e96521d8ac5f79eeb909c372706c5604a8`  
		Last Modified: Tue, 14 May 2024 01:31:19 GMT  
		Size: 67.5 MB (67453873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
