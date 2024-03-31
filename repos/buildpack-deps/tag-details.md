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
$ docker pull buildpack-deps@sha256:f256363b8d19c54f3d9d3073c3af8cc35a2f36fad37321a3a07521483953a1c8
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
$ docker pull buildpack-deps@sha256:43d3c37b0b77687dac2c85f36cc78a8d7ba9d75699df4a15837516767442e88d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245767248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d3054fd40eb8bac73c86d57a0840bb78a6f10e352fb09aead9f07e2fa02613`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:00:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4d70c07f54619a9053b20d9a7e6bdb6166b2c0fc92ac0d16c2fd1cd08e3c8a`  
		Last Modified: Wed, 06 Mar 2024 04:14:41 GMT  
		Size: 60.9 MB (60905037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786495634ea9b39ce8af363dc672e02cf79588e0ad80bcb2a1e8973f4a188ebc`  
		Last Modified: Wed, 06 Mar 2024 04:15:09 GMT  
		Size: 145.1 MB (145146731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bbe6d1306df1c36062b1e98a162a648bc63b0bf5e17f4d8da4b27fd99a7f1d0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211983091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bb4bec2065ee27d34023214713dc0f920d228a7c758360e797f5e18cba33ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:52:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9f0146508c64525bcfd4953b27c7bc27e67adc334304ff83b5aeae6662c74`  
		Last Modified: Wed, 06 Mar 2024 03:10:18 GMT  
		Size: 9.6 MB (9603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c590010ae329ae42a3f3d92d6d3ed12897e99e829fd5f3a7871b7fe749924b5`  
		Last Modified: Wed, 06 Mar 2024 03:10:38 GMT  
		Size: 55.8 MB (55824995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae87da7abe140f2cc4ac3a9cc942eda5b47996ae7267fc3091a639ffe3ca9fe`  
		Last Modified: Wed, 06 Mar 2024 03:11:08 GMT  
		Size: 122.0 MB (121953048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffa0a62a3ca08a64fc5f594dd3865f6466849059e9ea9990271035c565f7ac5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236009847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb940e7846b8085c7a2712e912b939964cd3f340df8ddee9298eb4c41091a3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:35:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b70f732816698b129506e28d62990303060cdb6a7e3648ecfe01939b8456b9`  
		Last Modified: Wed, 06 Mar 2024 03:49:50 GMT  
		Size: 11.0 MB (10982656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825501692e99efb3151808bc0e1e172221c3b5e177cc98f154198c4cd13cc9c`  
		Last Modified: Wed, 06 Mar 2024 03:50:06 GMT  
		Size: 61.0 MB (61012439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a76da96cc9e5dce0a9fef90bc56f0eaa801b1446afa74bd015e4faf20258f`  
		Last Modified: Wed, 06 Mar 2024 03:50:28 GMT  
		Size: 136.8 MB (136810465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7da210f5779ca763886b072703fec650e315ee5e7e629623cac30e837f272815
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269541604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7332f19d3175ee3933fe937e212c79ac0a51901ff1be57ac0899f1499e6a95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3c4671f11ceaf15eaa838e9bb48af73bd571bc62e8c73f16f42452c9879e0`  
		Last Modified: Wed, 06 Mar 2024 02:51:42 GMT  
		Size: 12.9 MB (12940566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7119467b1655cb90e1b0d916d873f5a33c39b88247a441ed1ec92219f1384fa7`  
		Last Modified: Wed, 06 Mar 2024 02:52:03 GMT  
		Size: 69.7 MB (69653454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea95096a68600f250a17a0068db72e82868688495868dc3313292869df9ec840`  
		Last Modified: Wed, 06 Mar 2024 02:52:38 GMT  
		Size: 153.6 MB (153631975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:34e4e5cf089fa656453136e74481ba72ebf631cee8bb2a08cba9567c1cfb8e0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226585031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e831621e03de7724d7bfc14d46353902b135492ee7d403b3ddd406531a01060f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695eff7bd6c3c722a97614ed18f70c79901aa397e0b9728ba6d390a6d79c0b`  
		Last Modified: Wed, 06 Mar 2024 04:46:22 GMT  
		Size: 10.7 MB (10690550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c9a922c9a515fecd2f06f0dbe92470942ff2d5fea6733260d1fd805ce4833c`  
		Last Modified: Wed, 06 Mar 2024 04:46:37 GMT  
		Size: 60.3 MB (60317321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1acace356fe61ec53b578b272b87ed519a18b63a721cf6adff1c3850d980b`  
		Last Modified: Wed, 06 Mar 2024 04:47:01 GMT  
		Size: 128.6 MB (128561095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:de45a190eca52f857c2159813a4e04c870b4b1dc060f80e0d1b98ce9df3898a7
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
$ docker pull buildpack-deps@sha256:93095312b7054939dfe29b5b71a732d37fbce82b86fc9e4c3089fd25a241e2a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b995f720eea62a403831fa719ba7b986350ef26882184d30d16248f5201d362d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:61c3af39ef5c4a1fc3d7d94e5a0efe5658d79de89bc76acaab85548f7ff423c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34205048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb51cecb76bf4270c3985f87edf86479dfad6fb0b8c868b86493c9d42f317de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9f0146508c64525bcfd4953b27c7bc27e67adc334304ff83b5aeae6662c74`  
		Last Modified: Wed, 06 Mar 2024 03:10:18 GMT  
		Size: 9.6 MB (9603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:780f091a85d8d9109be43edac1cc4bb1eba149bd02145129b2ff856c5e2e60fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38186943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95abdce3ef1c4988b5e5f7cfd3a5561aa851f2dbaaf1bd387eb30d56522f81b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b70f732816698b129506e28d62990303060cdb6a7e3648ecfe01939b8456b9`  
		Last Modified: Wed, 06 Mar 2024 03:49:50 GMT  
		Size: 11.0 MB (10982656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bd11d083e37d1d846674d6b0261fab753fe844a6eb7bd0079327ef5cc3ba835f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46256175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50151c2c5e0f6a187a2b915dcb743d9d92940f9ad1f33d51369b2e0588546691`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3c4671f11ceaf15eaa838e9bb48af73bd571bc62e8c73f16f42452c9879e0`  
		Last Modified: Wed, 06 Mar 2024 02:51:42 GMT  
		Size: 12.9 MB (12940566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d948151551f220922b4d4457871e595725779585a01085b5eb774fdc73e4b24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37706615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee05e4e8257d30fdf8a8bd7955db13f6922c9b2535855edb576a10088fb1837`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695eff7bd6c3c722a97614ed18f70c79901aa397e0b9728ba6d390a6d79c0b`  
		Last Modified: Wed, 06 Mar 2024 04:46:22 GMT  
		Size: 10.7 MB (10690550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:d0f7d7739fe9ec3eec069081fdf2caa440dc47642a9f2e4dfd0179590906608b
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
$ docker pull buildpack-deps@sha256:1e3e2ce08e857e35a43c63ae37175f4e660671d3f4083965e5ca0d901f8cb42f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100620517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0845dc47c291e59d26d0e5d0f2dda3347073ccf12b61bd23967b79f1d98a149`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:00:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4d70c07f54619a9053b20d9a7e6bdb6166b2c0fc92ac0d16c2fd1cd08e3c8a`  
		Last Modified: Wed, 06 Mar 2024 04:14:41 GMT  
		Size: 60.9 MB (60905037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f58e582ee6dfad771b2717c132a1a65917e76b56c8223eec9742b906077b6cf8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90030043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb18cea8d2f1053027c222e32a823b6e1fea22f98d5ecbf3c141614b87c352`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9f0146508c64525bcfd4953b27c7bc27e67adc334304ff83b5aeae6662c74`  
		Last Modified: Wed, 06 Mar 2024 03:10:18 GMT  
		Size: 9.6 MB (9603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c590010ae329ae42a3f3d92d6d3ed12897e99e829fd5f3a7871b7fe749924b5`  
		Last Modified: Wed, 06 Mar 2024 03:10:38 GMT  
		Size: 55.8 MB (55824995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:adb71aa7b372d1c6664c0eca285a06b0683f4a7a11a4312e68cbefee7be608bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99199382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ed358c6c66daf3aa0449000cace757a7bbfe5867ebc95a09c007b165efbe80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b70f732816698b129506e28d62990303060cdb6a7e3648ecfe01939b8456b9`  
		Last Modified: Wed, 06 Mar 2024 03:49:50 GMT  
		Size: 11.0 MB (10982656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825501692e99efb3151808bc0e1e172221c3b5e177cc98f154198c4cd13cc9c`  
		Last Modified: Wed, 06 Mar 2024 03:50:06 GMT  
		Size: 61.0 MB (61012439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:53d0f0e31dca61c598281b7a46c185bc4bccc1083d30502bbe7c91ab31245675
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115909629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461836c430ba635511e1f75bf41efdaf87b62800c3cefa3a24ecd38f600f836`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3c4671f11ceaf15eaa838e9bb48af73bd571bc62e8c73f16f42452c9879e0`  
		Last Modified: Wed, 06 Mar 2024 02:51:42 GMT  
		Size: 12.9 MB (12940566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7119467b1655cb90e1b0d916d873f5a33c39b88247a441ed1ec92219f1384fa7`  
		Last Modified: Wed, 06 Mar 2024 02:52:03 GMT  
		Size: 69.7 MB (69653454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:709ee2e2142e74642b093a5c8c05ca86b2f024d56a888c5d25328b4c779c5bf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98023936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83db2c966a7f686713e352fb1a1ffc3a0be52c2aae9ac8b66870d14cb330d3d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695eff7bd6c3c722a97614ed18f70c79901aa397e0b9728ba6d390a6d79c0b`  
		Last Modified: Wed, 06 Mar 2024 04:46:22 GMT  
		Size: 10.7 MB (10690550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c9a922c9a515fecd2f06f0dbe92470942ff2d5fea6733260d1fd805ce4833c`  
		Last Modified: Wed, 06 Mar 2024 04:46:37 GMT  
		Size: 60.3 MB (60317321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:f028439d1e21418883b8ea83670b1bb142aae932caa17602f4542cd33cb85094
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
$ docker pull buildpack-deps@sha256:ea6528431a9af0aacf1b5ad0f03c8b72a0fc9e49901401ef765b03c8872bcd43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250088348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f899440a738f36600d5a6f50192bd854357b38759a77fab51984c2b4ea4e2fd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:05:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49593e5760d417af1144c55c35eb9e0e2a7460c7656256f5998b9ae8fd257534`  
		Last Modified: Wed, 06 Mar 2024 04:15:23 GMT  
		Size: 7.1 MB (7121797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92589fe65e5594cf3e31809c66ed3274029643ca4cd99676bf7df67e566fba8c`  
		Last Modified: Wed, 06 Mar 2024 04:15:38 GMT  
		Size: 39.5 MB (39450394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadae4da62843bd526e310e7d6931f0c30d16eb92a924a3e436be5d45ba78aca`  
		Last Modified: Wed, 06 Mar 2024 04:16:10 GMT  
		Size: 173.1 MB (173064855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6790111010d47a222d10178b65a9fb3f5f6005cd13de42dcaa018342e2546d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217363067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc3658d0b2091f7b40475a6c7ec3adce3cfdf42bf655b3f261877cd374b3e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:52:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:57:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7fddbd99c87689c797128c33e1f1c9f61160d0051dcff2c4c3051e0caa54a`  
		Last Modified: Wed, 06 Mar 2024 03:11:18 GMT  
		Size: 7.0 MB (7019941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9ea7a997426b52cffbc09e40167bbee3b28329fa851e6e1e5700031231c406`  
		Last Modified: Wed, 06 Mar 2024 03:11:35 GMT  
		Size: 42.2 MB (42240423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb816ff59afcccb02e4382638892e5b8fde04045e946e9f32415b1eb6fa45f5f`  
		Last Modified: Wed, 06 Mar 2024 03:12:08 GMT  
		Size: 140.6 MB (140568769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:42ffd854e75daa213a3a90bbbb36c57e13a9317a767af239c64dd1130620383c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241373030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8332128d09686a1861494e0d65e5a487a1b6c9f0fe88575627fcd9ea5818a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:39:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a73d6c45ae19423adf83856e0bd5b156f302f22361a2da09d76f647b4f81b`  
		Last Modified: Wed, 06 Mar 2024 03:50:37 GMT  
		Size: 7.1 MB (7067410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92327d9c49efd4c50fc3e28a39cb60e6a3f304a87a6afe8f4885ac5763ec20d2`  
		Last Modified: Wed, 06 Mar 2024 03:50:50 GMT  
		Size: 39.4 MB (39365735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2aefef92435996ffb7df536c8882a73fd033bec4f2294acb94cd1a18aa2618`  
		Last Modified: Wed, 06 Mar 2024 03:51:14 GMT  
		Size: 166.5 MB (166539247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fd94324ba87b712f23141440d6b91347506f56b3443c4cc88262115e2a357cd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271270158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559f3af32fb08d7e12e483978d98ae96c6a6a42de87b0e0e4ddedb35a69d1a2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:33:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1cd6dd1d48531afc533d075d66a6fddaee5888dbba2b8247dcd3adcea1a763`  
		Last Modified: Wed, 06 Mar 2024 02:52:49 GMT  
		Size: 8.2 MB (8243679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2416321de37a426f77fbde63472628808acb699afc1e19ddacf4b3e909e93130`  
		Last Modified: Wed, 06 Mar 2024 02:53:07 GMT  
		Size: 43.8 MB (43763759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9841082859ded3148317fa252d4ab05c9e78b45a61c8a853bbac779be8c7f1`  
		Last Modified: Wed, 06 Mar 2024 02:53:44 GMT  
		Size: 183.6 MB (183639981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e898121e762fdc600376de850be35432faeaa4cbe15f9aaad87e2fb618f9b0f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223814934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73033ce3d671151a02ef921d0f0f48c400acf322bfb3cd355e84cac88fec8b8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a92f5c603f4c36022879efbb91489f2c52027f9e7ae958f0f61db3d2df3f1`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 7.0 MB (7036338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df445eb0e6484b70b95bc3da3debd8d0dfbca809dd62d47cefb8ca34f4c11fa0`  
		Last Modified: Wed, 06 Mar 2024 04:47:19 GMT  
		Size: 39.4 MB (39416503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634e85bbe96f4cad56d6662db0275b9dde4385eb833fa7b43795e88ad1106b`  
		Last Modified: Wed, 06 Mar 2024 04:47:43 GMT  
		Size: 148.7 MB (148725337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:6e50ae25cfaabfc5f6cb46195d224209c4c5909f8a9bf7f8e532fd52988b8c11
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
$ docker pull buildpack-deps@sha256:093e213de67157aad5e9363931b9dc7abb198df561d5ca7fd42ee05a0268b817
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37573099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc61e0ddf2f1265350aa7d2df4380e0c5e9be3fb88107a7d8c495039ecafe62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49593e5760d417af1144c55c35eb9e0e2a7460c7656256f5998b9ae8fd257534`  
		Last Modified: Wed, 06 Mar 2024 04:15:23 GMT  
		Size: 7.1 MB (7121797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d5614859dd275008e1346f3cb2f9a701bad80769a30d1b18712953bf7df3a842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34553875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bf063a2f2ab14728f503401f1fbed9f9bf89b86af66e16ed6cf9ec5c49f4a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:52:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7fddbd99c87689c797128c33e1f1c9f61160d0051dcff2c4c3051e0caa54a`  
		Last Modified: Wed, 06 Mar 2024 03:11:18 GMT  
		Size: 7.0 MB (7019941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c7a37bc43eb6b8da73f54b88efb3828d2cf1eb022635d042456111ce2acaff21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35468048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3dcec6ff2ec4a0a701056c03c48becc701d4f0105679f8a00c0c84085d145b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a73d6c45ae19423adf83856e0bd5b156f302f22361a2da09d76f647b4f81b`  
		Last Modified: Wed, 06 Mar 2024 03:50:37 GMT  
		Size: 7.1 MB (7067410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:91acb44d39f9102804b9850a5b17167e3d43889882f8a57c22b9346aa25b39ea
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43866418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984ef75217126be1dea3f9a48e846ceb4054593b4443180dd89a3b5380117891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1cd6dd1d48531afc533d075d66a6fddaee5888dbba2b8247dcd3adcea1a763`  
		Last Modified: Wed, 06 Mar 2024 02:52:49 GMT  
		Size: 8.2 MB (8243679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3fe00ad471a492cc6850f51abf635697501cb22733a201292980ba875a54951c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35673094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ea4456f1bd77a4dedafa9aa3a5afa9105940c800ffd5525914727bb0633891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a92f5c603f4c36022879efbb91489f2c52027f9e7ae958f0f61db3d2df3f1`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 7.0 MB (7036338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:44fd3f944013377caec06347436126c04837bbeebeffc6f1701f3ddd26f10b33
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
$ docker pull buildpack-deps@sha256:4b4aee6ab806ca1f70f2f32a7f359c5fbc05e5b0ff38a42348252c897a395b2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77023493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493ce92db0324f288231e41633bd2c1445eb59e22b226c85d06404fc7c82c441`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49593e5760d417af1144c55c35eb9e0e2a7460c7656256f5998b9ae8fd257534`  
		Last Modified: Wed, 06 Mar 2024 04:15:23 GMT  
		Size: 7.1 MB (7121797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92589fe65e5594cf3e31809c66ed3274029643ca4cd99676bf7df67e566fba8c`  
		Last Modified: Wed, 06 Mar 2024 04:15:38 GMT  
		Size: 39.5 MB (39450394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ed7545234b9f94ec0418e2b081b2bf084227c1f71cef8213e723b219450cea1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76794298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a340863c84c3549e70b82bae506ba95275e5e16a0e4d8668e8e7cc25599989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:52:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7fddbd99c87689c797128c33e1f1c9f61160d0051dcff2c4c3051e0caa54a`  
		Last Modified: Wed, 06 Mar 2024 03:11:18 GMT  
		Size: 7.0 MB (7019941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9ea7a997426b52cffbc09e40167bbee3b28329fa851e6e1e5700031231c406`  
		Last Modified: Wed, 06 Mar 2024 03:11:35 GMT  
		Size: 42.2 MB (42240423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0901fa440c1f905a96f06e70827ca1d05dc8d15002e464eba7fb5cef30635d8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74833783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7cdc334b48cc07b03d0feb8577106dff50fb6c520f8feb93ef1b641d20f0e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a73d6c45ae19423adf83856e0bd5b156f302f22361a2da09d76f647b4f81b`  
		Last Modified: Wed, 06 Mar 2024 03:50:37 GMT  
		Size: 7.1 MB (7067410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92327d9c49efd4c50fc3e28a39cb60e6a3f304a87a6afe8f4885ac5763ec20d2`  
		Last Modified: Wed, 06 Mar 2024 03:50:50 GMT  
		Size: 39.4 MB (39365735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f6cb4f947f2e59872ced21dc90dfe61e3b8cafeb9fdf54b5ab85dca0d38f492b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87630177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5683974fd5fec66709dd16f0694e8f33163111f9ae05cbdaa3f94876d731d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1cd6dd1d48531afc533d075d66a6fddaee5888dbba2b8247dcd3adcea1a763`  
		Last Modified: Wed, 06 Mar 2024 02:52:49 GMT  
		Size: 8.2 MB (8243679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2416321de37a426f77fbde63472628808acb699afc1e19ddacf4b3e909e93130`  
		Last Modified: Wed, 06 Mar 2024 02:53:07 GMT  
		Size: 43.8 MB (43763759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:405bcf3102e90966c04536e2699d5a877d9ecc36d137355101aa09ab3cf5feec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75089597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51541b954c6f35a7e17b244341e84398bc948fcf6abc5b7fd993c58d7b1c2f6b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a92f5c603f4c36022879efbb91489f2c52027f9e7ae958f0f61db3d2df3f1`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 7.0 MB (7036338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df445eb0e6484b70b95bc3da3debd8d0dfbca809dd62d47cefb8ca34f4c11fa0`  
		Last Modified: Wed, 06 Mar 2024 04:47:19 GMT  
		Size: 39.4 MB (39416503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10`

```console
$ docker pull buildpack-deps@sha256:5a2e19035cebac59a36067884b5ab60cc5eb21b536b7e4fd8a10da404752bd77
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
$ docker pull buildpack-deps@sha256:f918d4428aa964953d5aff1d5bab0b82c372f9d3d38a2d12b77458d37c3ca34a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279780099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641f1e177d185a2b62526fb65c672b0fac9bbfd5897ebd1aaf0eb1e1d8b13450`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:09:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b21ae994c2a096a3b04d9c7a1755c60179f67ca190f61936d6da7e1729ee588`  
		Last Modified: Wed, 06 Mar 2024 04:16:41 GMT  
		Size: 44.8 MB (44763285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a90bca93d1e62f99fd8cc0756b7bee297e054ae196104b9fdc912a38ff8fe2b`  
		Last Modified: Wed, 06 Mar 2024 04:17:15 GMT  
		Size: 197.1 MB (197070772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5289f79ac531efb8ad33bd0b0b6292dc4e2f62c9ce303580430f92ceeba1f221
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246446751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4c6acfd8c70545c484652739cb0d03b4027ea23f793b63b1e6b189a815dff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:03:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155ba03212deb920e05dc77749cc267b5b6fcdc16bda27f00864d27e0607886`  
		Last Modified: Wed, 06 Mar 2024 03:12:42 GMT  
		Size: 49.0 MB (48950883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181be50d83864dec48e37287e8806806c68c94293ef26ba5d9653a7ff9a4b7b`  
		Last Modified: Wed, 06 Mar 2024 03:13:17 GMT  
		Size: 162.7 MB (162659026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76c20fa0c78fc1271616d426ea1dbe616824c6c892c1bf9046e262596f505152
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271897474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d283ee2047a060b9e45a0d79315d06fbc480c77b2a3f50527f6c718f2adea4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:44:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d621ac8cadee2671e19aa461d0119c3f949da68efa86d87ba2fa18fbe4c9e4`  
		Last Modified: Wed, 06 Mar 2024 03:51:40 GMT  
		Size: 44.7 MB (44677268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d35f0efc15036eae5bb318b2e83575fd707a37e6dc72f457a6f570de89d772`  
		Last Modified: Wed, 06 Mar 2024 03:52:07 GMT  
		Size: 190.2 MB (190191833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ab7b2acc2516219c4ef73f4b519ca6601deef8c0a12945ec8150420b6b56bcd9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293684369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ffcb209559ecddada302e968d75fcc80963af851b66bb76f1f3c712f1bb074`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:42:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa179ccd4d1ba32381ba7b18ea7a19fe2a7be5021377e619dcd5ea87d94344d0`  
		Last Modified: Wed, 06 Mar 2024 02:54:21 GMT  
		Size: 49.6 MB (49556847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24aba2c716f2fa40ca775335da4d638dd85043cc5ed23691c0e7ff819d6012f4`  
		Last Modified: Wed, 06 Mar 2024 02:55:01 GMT  
		Size: 200.2 MB (200194410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bf563f492cfdf4136e50962e79781124e89f7ad8d3c83ee9a7ae7900c302bac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258272975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3b9652943dd3a8d4114303ffd5f985dcf0b6b5726a1399f28e21d58d48fe8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4dbb0d5afb81615197531053990f5a73783a82aa400fa0f09d685d800e4b3d`  
		Last Modified: Wed, 06 Mar 2024 04:48:04 GMT  
		Size: 45.2 MB (45232146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938a3723c4442291047678d7aaf3a42732033cd41bd537189884332a3986f57e`  
		Last Modified: Wed, 06 Mar 2024 04:48:30 GMT  
		Size: 175.4 MB (175394105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-curl`

```console
$ docker pull buildpack-deps@sha256:b2fb7a10e28652e02c3191ce47a15c8acfd40efe3c0321b90f0ca10151e5d7be
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
$ docker pull buildpack-deps@sha256:0fca5ff13f7f7b5e8298b93f28e15134e4b2df1daf8baf6222f533d87509be11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37946042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1bae1a972ac939e27c44ab147653e269f4987bb9df150221ac1d013ec897b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7dbdd2bed195883ab42ed0ad0b96818a1787ca8e95534f13c5d82a54621cef1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34836842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a886df4f2c14a8b0a45e16f024da28bd47814a1fbbd2a042287c8906a1fef3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4341891a0761c7bcd09df0d6c13682f3d1c1479160b0333bf1089308cb974b70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37028373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe26cb29e36768799cbb3f4712ea4afbdaf4140eb64b1b05e8c996880413533`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d305c5e6a0a1f1b89f5121496c829e2dd3e93d7fa8a139a2eecaa361e0c8fbaf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43933112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f789d7772d1087fb0373a1bca7a85cc9eded48bed7bb965aac975c8f30e81f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:72b4793c911a7c181fda7bfd7b1ac2c37d3283cf9cbe8fb031646d2175bbc135
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37646724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901ab9ff2fd6adaa5c1a48a8a562f7cfe812fd1b5f12594eb071e136f4bf200a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-scm`

```console
$ docker pull buildpack-deps@sha256:70f090b9c541b93b5f9ed34bd50da2aeb9a3ff4a427ae2f92f661d3f74c0b001
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
$ docker pull buildpack-deps@sha256:419609933b12ca00c8a73e76e6cc3495af03cc6a0a55fba48a6587ea534edf82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82709327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57264a7b401ab4cee2930269cd96560c3f9f21633772107aece54ae9ca0f535e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b21ae994c2a096a3b04d9c7a1755c60179f67ca190f61936d6da7e1729ee588`  
		Last Modified: Wed, 06 Mar 2024 04:16:41 GMT  
		Size: 44.8 MB (44763285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b1e9d9758301286327426af6e70aa5e7b8f216cbbd269c7edb29a983d63f446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83787725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9df0c6a52502c3869f438d017cae886cfeaf9e60f8fffd62af11e496fd0d92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155ba03212deb920e05dc77749cc267b5b6fcdc16bda27f00864d27e0607886`  
		Last Modified: Wed, 06 Mar 2024 03:12:42 GMT  
		Size: 49.0 MB (48950883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b013931b7d46ad0c87a33432be075b94d81143b739e990ba3e75f0c02f7dae3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81705641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e87fd7008850f0b06f056c883613692b0dfddedd35041aa7b0698c838e51d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d621ac8cadee2671e19aa461d0119c3f949da68efa86d87ba2fa18fbe4c9e4`  
		Last Modified: Wed, 06 Mar 2024 03:51:40 GMT  
		Size: 44.7 MB (44677268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bcdd59a28ed12834d023ba530aba7e94e8c017295320aa4f73958d863770616d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93489959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4557f6a8a7ff4ac3b6bdad4b5eba002b8979f1bf9ad6336c32e511facc61e88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa179ccd4d1ba32381ba7b18ea7a19fe2a7be5021377e619dcd5ea87d94344d0`  
		Last Modified: Wed, 06 Mar 2024 02:54:21 GMT  
		Size: 49.6 MB (49556847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:edb7558a64f98191228b4671e70d1a48492743b171a4f579192d2e969cafc1ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82878870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ffb3abe7aebbf4aa283e2d47a4d095cf8871f1e827a00c764dde4fd926c076`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4dbb0d5afb81615197531053990f5a73783a82aa400fa0f09d685d800e4b3d`  
		Last Modified: Wed, 06 Mar 2024 04:48:04 GMT  
		Size: 45.2 MB (45232146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:c39d69d10d0140c4c4bf04d1efea4fe2854fa91ff1ff38c0828f32bd9b9e404d
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
$ docker pull buildpack-deps@sha256:259dd02ae96f2d1babcf2983e064912b0e3b659930fc6be79a8522535248e9d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318695257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7c40ab633dffd0bfaf07763af95a466147808ffc85bc8c9eb79fb712220c04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adea66a5a529e25830935a61441a370c0563b30d99ea2da7a49e53bf8108fe9`  
		Last Modified: Wed, 06 Mar 2024 04:18:24 GMT  
		Size: 228.9 MB (228943762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ba0e14a02d5e19dcb27e9e14af9939b30f7878fb599510a1f00d51db45e47c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273230848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576daa73dca6305c7ad39ca45a2e5b80acdeddc0fb2197af8d139a7a5fb538e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:08:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e01583a141e97ef5a0aec445ed9f7e14e941b8b3e37745c1e36c3109b96554`  
		Last Modified: Wed, 06 Mar 2024 03:14:32 GMT  
		Size: 183.1 MB (183135775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:45ebb68136dfda231c4d3a51c9527ad2063b899981d8d6438edc8cb96f417dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305425921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d15e3ee41e130ebf4284b61a5e0347bffcb935d8c2be0e9fac98e091c91b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:48:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9974eadb59c4c8a7258a03bdd5d5182c454d60c821a9dd902e3c04eb031390`  
		Last Modified: Wed, 06 Mar 2024 03:52:35 GMT  
		Size: 45.8 MB (45805608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca642e4c3164d875c8a8e31782bb31faf2f4b630867d243eecba4e0ee7953bf4`  
		Last Modified: Wed, 06 Mar 2024 03:53:05 GMT  
		Size: 216.5 MB (216473828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:baf0bf3926067d244a5c186b6b0029a1b09ed610cc3e37331ba14cd48e9d5ff7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335846262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9481a6c3ca7d56bb183ace9f2a0e456ae608916c120ca6224e2675325199e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881ddf165df7bb2420e4acab24b0465182f8afbef4c4f87365c28ac2fb58bd85`  
		Last Modified: Wed, 06 Mar 2024 02:56:32 GMT  
		Size: 233.4 MB (233378799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6d1af75975c131519bbc8eeef86a9312c981a838d2fcfc00dccfdd4a7f99141
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301888562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def7e5ea62cb995f9b4683cfad978dd3e5956d619fb317798e5bca90d3796de1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1671ccd52fd4caa5e52f088375d19d5cc86ba163b0350c95ff464ebb872668a3`  
		Last Modified: Wed, 06 Mar 2024 04:48:54 GMT  
		Size: 47.3 MB (47346503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fd1b8866a23f60ebd429fa73528999c0080ab66d901f8ef47e7450888952ae`  
		Last Modified: Wed, 06 Mar 2024 04:49:26 GMT  
		Size: 209.1 MB (209074799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:de0d254873c7b223c0be69fb3fc44c87eae25c0c69f8cfacbe686902282ab12e
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
$ docker pull buildpack-deps@sha256:ee6619518234d5405ba8f94421cf0080c2c2e5951fe4e4b94bf2e6b5ef53dd93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44007564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e663bb54ee5c1f72bf54c4d90d616ceea2a986638d02a9ac69f807c6725c956`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:350010198cea3677c190329cf929db66bf1c1306a773c97edb58fa61e01a66a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40333879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2aff73dd21653f7ebd3038ae640fe1e4ce71c3188a91f5306f5335cd803db9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9cf4aef16cc9d6aa4a3c6a5fe99c6c6037ac19f9f553ede8bf3d67a2702e178f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43146485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa467416227b588463fbe2b6f19975d7c849d6cb4b7ca1de7c1894a75a0887d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4337421100410698f2134a79ffd494f3ffd953e745681509bf17625676957db2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51415051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926f624c8bcdf5f2ebb3a4d1d357cf9c18d80e976f254d0ea5352520e6ba7508`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:904cba7d3db15ea7e0ea12e99f42791db89e7df90cdb1bacfb3e7053d22c7015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45467260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8a74f855b84ab2d1fe6fc5fd545b465b0fcd64443b87db9434e77505df37b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:d6198b799cac296e3b53289f88e383aa1cc4f2b2fef634968cb3cd2dd9211a2e
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
$ docker pull buildpack-deps@sha256:e43c3e34a53dce68d563e649080229cbb53ac55992a35e06c4f23cb2f29a46e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89751495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97da8472260a449f47595b95361c39f80c26a5894437f82fce55171b89b43d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:27735ee07214b2f855072fcd4e72b7ad7424f03fc6e9df5c952927a8fda5a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bdee64687fff39f7a4891dd02e5902accecc0de732d5aee169f276d2af04cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:257020a2cf4445996e0a6d9e636c95960ae5535fa037c2f4618b9cddd4a5b649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88952093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27519f55dbc4b5484ee5cdac3b1b800f530a6d11c3700d462f995d64c53e97e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9974eadb59c4c8a7258a03bdd5d5182c454d60c821a9dd902e3c04eb031390`  
		Last Modified: Wed, 06 Mar 2024 03:52:35 GMT  
		Size: 45.8 MB (45805608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4abfcbfcbd30feb2b4bfa41fc5fd1b18dc1b0e215977949d3c6a6302f99ef900
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102467463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb035723872aeb49e171babb083d8929637be280313d4c03325efabf9a82b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2c4aa9aefe1b606f624d09a75c8bf230a5eef05c556dcf9246644e2a7944c1f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50aa33049ec903d31f3eac096479589f99fd99660e241a06945f6d97aa2e4e32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1671ccd52fd4caa5e52f088375d19d5cc86ba163b0350c95ff464ebb872668a3`  
		Last Modified: Wed, 06 Mar 2024 04:48:54 GMT  
		Size: 47.3 MB (47346503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:33fd523e6d918b2d066038992f814ff881eb6de323d3c70b7fea851ed1c36be0
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
$ docker pull buildpack-deps@sha256:db9fa21724f9ed2ea02b2b5ece7b9b33c539c1bc812e1f576c88854470db0c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348878735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a3793f3c6079a0170f05599f2735b64766d39d2c34374471d3bcc6ca540d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:54:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567db630df8d441ffe43e050ede26996c87e3b33c99f79d4fba0bf6b7ffa0213`  
		Last Modified: Tue, 12 Mar 2024 06:03:18 GMT  
		Size: 211.1 MB (211139445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:091d6742817a9012801ddba3c88d22130da8ec2a52a82fdab424cadb8c02672f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316009389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d577d2712bb80823634647f21b499b3b5950339ba80b463b1d5ec39552739bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:35:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9069b8edc3144ea7c7fba8c956dedcc448fc0ba006a12c9cfe4ac23f05569d`  
		Last Modified: Tue, 12 Mar 2024 01:44:12 GMT  
		Size: 184.5 MB (184456518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1919befcfca67d8372abe16832d32831608044d6022238cb362f0ad8296441a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301423265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c58b41f8b222deb6863d767951930f9431b526720e771a43ecb9c74e996cac2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:236f29b4631548c327b2d1d0590ef8011bff534a87f62bfa2a68a91f8d8c3c02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339703020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02567629c9e9c4dc92672656620fd7750ba05eb4c4fa2d86a63ac92419d2dbe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c418b37b4bcde3a68933365b172d45ae5f3b046050fde08b6eeca5d57994a08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351512027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f67448ff33c81527caf039ca97b379daa5a4deb989b5d2bba32c70ec9a07deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:41:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee485e7c553f7b1465ed88918f0904a411af3dbb0918703ec7b92192eda6417e`  
		Last Modified: Tue, 12 Mar 2024 07:54:34 GMT  
		Size: 210.1 MB (210058424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3e131fedd6c0a053f4d92db50d59e106405e5047e2b38db2db93bd1cbf4dc08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325858634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9827aaea1a13889e5939e08ab8f7c05be47b277bcb8f5da059cec0ab3b14c450`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02977c85a258d317066e5a1e6febc79a4caa2a830ee66f596c866db50d3361d7`  
		Last Modified: Tue, 12 Mar 2024 02:44:46 GMT  
		Size: 189.7 MB (189698984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d82d41cabf8e17cd142de9f607e0fa1c803e30fc7c1c11702fe2eff44af1d4c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363009215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6db4fb9bf6b421d4aadfcc2a56b963ee8771a5c2e2813078cc1e73b7a33733b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d9053a0f750316634df779ba70e4b32f8618c06678f58ba3e14bdbd7ec4d444
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0947a371e12fd46d0e731838049ffbbc92492031782ffcf22ec58497a4e57efd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6654b38164df76c1496278c128a09a6fc9ea1d703322ccb6eb98f578047b2b07`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 183.2 MB (183164991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:da13a0b5c77dc3e752cc9d9e185b9c09f2e2064d8e11218ffca5a57406a10bfc
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
$ docker pull buildpack-deps@sha256:cc05c08ca39e926630564a43219ac19163c7e528389960d2fe9e639025638618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c215ffce5e7490aba71d8dabf58ef741bced74521af2c5f27869e888e3d95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0240b8998a2b49677c6ca0a32e10689d5c0117ba74d967e8a6d98fe7a4ae3fa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70037013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca62b11afe7a8431a7e12380500c7c2eb46286dde03a2bf7cf121cb6e7d10708`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b872e7fd396a6833da36a5ef61e35ffddcffce622e76d99cd704ed9bc2bb9c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff330e85d6b2d9a434a86e0c5df03f2fc83d2d5fd31e47532edcdd9512873898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48cec1cd7e892dc51c4f2d7516b2ed8f391e116929b5460e3ae0c976ed050693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ea96e7d1339ff33f942f8cc1315e0731121520bcbfac53669df4bb05c253fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7bfebc01b0982fb9874fe5bc61cb62bf8dba226d5fa3477f593bdad7502621f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7410bad07bb558d5fe093b6a01893c3a2b26334e114a68a3644836299bf37f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b18588551c4d881828aa5f3317b0536cc51d3663c096fa4d1ff409b1a7837e4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a9c2db66277195f38df723d4eaf40817c0a38943d94badc968e39f17f98be7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9d2e59a230a9d4a04808ae004745f51e0e596953a2770503084886a3fb23f2e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79253819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5a24d3eb15d8f3b9ef6a936bb7a9d5b7a210c0779c7b2bbfc59ae6e0e14774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:95b1f86365edd875e362c6d47e79763e1f3b7504f29992ff6abf68cefbf731c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71960165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b776a30a72031edeaea3d61789f2250d8181bfb7503c9857a93cb931e569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:2c0c1638d1e037a1ab747f02c39b7e54fff548be0fe6f230a28c2b8301fbd20d
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
$ docker pull buildpack-deps@sha256:25f20fd3e3c8be1e9626c246986beb400ccfe19b0ab13d57127399927801d499
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3829553ca241eb6ec827e514210faab2db77d5f4a58764d0dd5a00f97f4a049`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4604b8d280097513158cce324d296dd8806f21056e09f659b28c7a0b236cc7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f5e6d0ea8c878fb6e49c35a11089dc2a50afecb3abe7942942297679e212bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cfb748d851e2e3cfdcbc1be1e1817fd84e8fff94498702a724beb1ed87b168ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126317289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2a90a637715c3c6bb9034dbf6c64f7ea86758a8c52109f24996208cf4d832d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd1553434a26aadad218bb6dacdecbc747db860969aaa45222d479b12c9fcdb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137164774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81cdaeb1cfb57a71b96eb9e0a8673ffde7936b504bd716ede73f435391fd8db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:651ed01e0f955ed10779074376f6fe0ecb8fe43cd832988c176b5c4fe3d8f4dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141453603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7e7c3092c37a6e5c2b8d528da777020e5b3d0cb69c67d216649c3d7c239f87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4ad06509257def2a4df2513623de0665e807666f3c0d942042e3228e12ab49d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136159650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d33af04fbcfe6b33eccfc1638aa0f25b79423288344805b88451266aa3eb56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9b03894e8f0ddcd1ee80a6112c6aab6e27a3532fbcae3e272cac191218353386
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148835718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f9a694cfc75a976c7f54142f0a5c4745f9d4f2a0ae27d4a673a3987c4888b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:793d4d8f8b9efc430bada65e9066cf9215dc96b03c605ae45dbaa4fb24ad830b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135086824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329d23986398ef8817d6d027b58b5b6edab632660cf8b81c3092f5ffe0a77816`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:f52498596f150be4024faf66fee96f08082c00a746085dc3dd2ebef34a64e12d
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
$ docker pull buildpack-deps@sha256:5525479c6bd58580e97a3ace40e7528bf8993dd51b88c9a04c14a8e9e130d6de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322422175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc59b5e9a715a4aba00120c58a0d109cb398f62d246f22fdd08dc70f5ed695c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6939aa9b63c6ee738fb4a9904fac366ecb96aec3d980993009e3b7ee3f7516`  
		Last Modified: Tue, 12 Mar 2024 06:04:18 GMT  
		Size: 197.0 MB (196985243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d6c8de5573c790dad1f0d4f5e6fc7c345370f46e3f87fc58045ee725f5e13b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295444734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3174601e5e1c389d2a7b21528e32c54c56c824dde8eef8591350957b9d5e97d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:38:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2f143fe44237c686e570db73ca8e79a407a12cd45adcb3067acff6628c74a2`  
		Last Modified: Tue, 12 Mar 2024 01:45:14 GMT  
		Size: 175.2 MB (175154282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c551c6dc6428f67f0448029cec06132e35b4812157ab96872a3f29b0c2f44c06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282917380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f56d6be33b4622a1fb72ecf376d307a70dc706ed4961f68488af7406739dfc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6e8fbfe95e9b8369601bc38a647238884aada5ae0bddd32c12e08f575d97422f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314080526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7fa0e4cf82f8321955d4c9516654fcc3ad4cdde3183ae19e37e2f7fb35168e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d317b4db41e297cffa1559c871d84437b3544f7a4c04d6cf339cd4e8caa94c76`  
		Last Modified: Tue, 12 Mar 2024 01:36:09 GMT  
		Size: 189.9 MB (189914923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:47f0366cedf269210ea0eb884035b03fb8784137998070a0cc96ea9f9b46f333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328144268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011ffd2d7f928a18305f2c51c05d951a8520f8d609612cce9b4dc7da52afbd27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:43:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632a01713bf6f27a1de411f14f1e21b375412e471fa832f03dc7ea3c86a0a51`  
		Last Modified: Tue, 12 Mar 2024 07:55:07 GMT  
		Size: 55.9 MB (55927686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfe6f6eb32ca002367ebec491da1c709c88fc7418bca1dc16043bf62ff525ff`  
		Last Modified: Tue, 12 Mar 2024 07:55:52 GMT  
		Size: 199.9 MB (199890619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:65bfe652bf6a879063dc90fab2ead606e4c8c5007949963d6d386bde1575d721
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301446653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f98dcd9cdd8c1aba9729a37d183692e64affc47fc9963aa5ee2e2aa200ebeb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:19:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f183b6f40e96072119ab41213733a9079dd8d43cd4a7c36f9f7e3531dd614`  
		Last Modified: Tue, 12 Mar 2024 02:45:50 GMT  
		Size: 53.3 MB (53310696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21edf61173913e6f42aa80ddb070961a6780a6703f5e284ec12292d725922b`  
		Last Modified: Tue, 12 Mar 2024 02:47:47 GMT  
		Size: 179.1 MB (179097827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:18c93cfdecb6b18bca3bdec1a55b31965e67effc9c501720d20a7b281f102f83
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330940717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa57c33a89d91a68809c39953c3546e688d9ab59fa0877c1c66e70959a068ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078e6b4fd896687174cc2013bea6ca7f49c8cd898255e8d37361b8486cb7fe25`  
		Last Modified: Tue, 12 Mar 2024 02:22:13 GMT  
		Size: 196.3 MB (196346975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ae021550b3144b31854c9a0860d42fbd41b41873c8452b715d6352026953d304
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296028247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf529bccc5415913766dae6191155093d8451c04b4eadf15a9c51c013729772a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:20:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dbe74529fc57e85a22f94e3442e33e7b5d04e9a4e5bfef8746df1fd2841eb8`  
		Last Modified: Tue, 12 Mar 2024 02:49:00 GMT  
		Size: 173.0 MB (172991681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:b8e2bc087998cb449bde0442739be8ff76da6d53707322d24a6bb7166b1437e7
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
$ docker pull buildpack-deps@sha256:a9ecf4ac7eed2d5a6601d74158afb6eb3a39ff06a98f23e53a9516a9986f1fb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb203964ec9feb91c764093f1aced9c543ade1c87ea002f782a9bcfa32ab536c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a67278d6f9005c7ac4434d07aae51d0d58c81354ca08af9d81a65326d9f47996
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67961591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb87e85efadec30a80462f3109359eb9c7e021644e1015a74de1bff8ebe2da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cb47374993facc2c740f43765774f17231eab30bba2e11689a4647ea5a205c1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b163ee51a07d82df4e4983f0ba5ddbe7596b7f223e0ac37636dba0048eb0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0b9a2f5356e7edf45a7dc9353c26553102e8f3ce722ba6240a23a1b49d6132e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69471302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0115b7e6179997944d5abffabfac54fccdef8a92587e427f5768a9c9de20880d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff0a5ddd9d781307de313da1795a608ac9ad369d6764056fbc13e7a64f89198b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72325963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec92a70eea4641cb7a6a60aa8a75b0981ffebfa175089e815dcff73ee1754808`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0083cf345719f184fe22aaf238217142b9c18b3a4aa7abceb916e0924b123281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69038130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da36f695074cd766511cc8a44b9629c55bd5e1999a49245479a39221b2fb53d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:92f9ed323d1b94f81fa714490e510187fdc47489e4e68c451511adb10f217626
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56413e6990944267231df1e0c2432576718f56e83808120185b375c50b89b503`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:754786485ef09e39e6946ba3605b887177a768e34aa803b1230314cab507d40e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68960835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81ec6160b5bfecebd05bc6c3b675a4a551c8a22dca8920e5e6902ce190090a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:302de6ccb1237785333412d7d70bdb64edad7f5c5c4bb80ee579b383d6f9319b
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
$ docker pull buildpack-deps@sha256:a46617c635cf7c885e2f741b3308f1e65c98a1e19515a0954959ef94081812d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125436932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9564ff86d3091c7760338926393f13187612898bbae224360fd36969581b1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b82a28618cd428cb303a3b3fed70c1fbaa15e2d7c0ec88a5213f7e5fb324f24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014ab67dc0681bc0aec86fe312177d276bf8643ab040b0b846c51bb075db4fe0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9dac4341f985ba6f6da87a345745251d4e1f1f88f5abbc11ff21dd613f0fbe1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115478050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd4d99544718ca88c6a40d99f13d278f6c4ab785d0fcac3d99148b6fe4aa000`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:50f9d48738e31a49e12cd8da39a4d5960ebea181dfc08c81fb3eed98f5ba53fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124165603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42ccb34be84e46eb9856d81064e642bfb16e932250605147287fc82f49f772a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9d2d1bbeb1a9c7d440ca0bbdce6e3b16fbcde367d9fa13057b28010dee90f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128253649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f814dcaa1597e9d66a274df2456808589086d74b54a14e03d9c850650bba5ee9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632a01713bf6f27a1de411f14f1e21b375412e471fa832f03dc7ea3c86a0a51`  
		Last Modified: Tue, 12 Mar 2024 07:55:07 GMT  
		Size: 55.9 MB (55927686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5fa1a7821881083e40ead9bf790cb63689f782905b96113519aa764c7b1636bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122348826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245a78fc3d28c1fba5c24a42c04a692d9b60f560c68e5aa3055dc5edfef73ba4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f183b6f40e96072119ab41213733a9079dd8d43cd4a7c36f9f7e3531dd614`  
		Last Modified: Tue, 12 Mar 2024 02:45:50 GMT  
		Size: 53.3 MB (53310696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ca5ed2831818a94c464ffdf78335acca49d1cd6e75f265e00fee6da1246bed8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71d28760fe78cfdc496496e01e97a5dba19414830d62e4ece7deb0bf643ad6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dff51578c019416cba8959947215e6ef4365bc531885e874fb8a3e4d552facc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123036566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200b30cd7082400a7d00f01fa2fff2d45ffcf3f75e979a708c121c5d07fc7ec1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:d58af141d3f29e8adebbb0e8338a2eb6834c13db0122b7b2859d30fb072d6c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ff80bd769b65dd85501684cdc4e819a46ed39638ec413258a90c08e6b962247
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311905592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea119635dd515e55aa2d8a34af1fa35d2a5d0c22998ae58ff28637215f9df67`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:57:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c719b870d0be3d68698a8ab9d2604ba1d9b85d3206a13ce6f1e5c50928dcc`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 51.9 MB (51877435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a275b8bae6bef10ec9dd71151b41617e72eac0780ecbfe93ee1dc86db2f5e9`  
		Last Modified: Tue, 12 Mar 2024 06:05:14 GMT  
		Size: 191.9 MB (191942628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b4761ce8f33fd0256c24ca66d9e214b4def4275f792ed17b05d5a0bd1f313539
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277728447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b3aac61bbb0a61c4a7044b56686673dc640b296ffa8d92bbe4f9451beb1940`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb7e022e9bc1cfbad07b9efb81d22c724a86aab30c7769950ea7a0d6ceac7130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302488134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5a5efe5c6052414a5d5ff289e9a2bddbc111ae796933875d6253560f57c555`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c2513d2262991ad3b0725da9db46b8706451ef2bb7a7617ef8d072bd83ac99eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321337763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6695a60050d69b4e529a4b0964e37e47ffb1250be9da9fa2db10edd9c6c64362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:46:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4053c8d16e2449fdbac1122e37652f53be8b607a093453ba6bf08e56bd9ba`  
		Last Modified: Tue, 12 Mar 2024 07:56:22 GMT  
		Size: 53.5 MB (53491671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611538514415c639eba0b1521fa6f33ff37569ea8882616480d31e1051e4242e`  
		Last Modified: Tue, 12 Mar 2024 07:57:06 GMT  
		Size: 198.5 MB (198491053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:0cc704fc1a7999e2180ad1fabafd497a64c6878627285694a2b4ccef23bc24ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e51e1b189a7ae90f38875e03231ec1558033fe3d59a714160fea3fc0675dd87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68085529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69123c5465280e07adf01a66e71dfe077eb93deb346ecbf80550e5c64893eada`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:39cace7737d92c1877b978b17ea755007f11fae3b0354febb96b926ea789a364
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a00299cf4b286e5c1a38ddaa2ef2181c0c8e4478765e738a82224dc5a27d73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e07c75aa1137c27d17351f9ae9f63806c460c994d42c8332b9e220d8c773e4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf536bc10e09dbf65f656f85df100c2d17a1ef16c0462ed8c2db153991ff5f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8275c22139b832f406cfbd9b9bc4ce66f57013e8dac1d64f3135d1335bf5415d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69355039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82149eada0485f28a9641351fd752fc666fb669e44e750855f16c629979cb5df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:4489872a1a88c55054fa6fd1f8b5c5b1e166efa10fc89e135cd2e17b6bf44a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:16b36fe965724b637f9cac1496ac57fd7bd3455b07809a8c242ed4856e011b18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119962964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9af31b6315761c93e7c05e123a139ac51f11ab859b941a1334e68f40456d56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c719b870d0be3d68698a8ab9d2604ba1d9b85d3206a13ce6f1e5c50928dcc`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 51.9 MB (51877435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e68bd043cc332cea5303fe5d70e40abba8babc905fe8242e633bfeff78515f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109594526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a938f58ea7b43cd5617321aeecf8da71571eaa469c87c48c4f70b9012268942`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8dd2c71b6ca885b1a3f1db72d9dd3f5eed70ad1091ee90e19e14b4e0e4523a8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118970337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9004ee3288570800fdae2c07356f979cc2b771241cdd524555c97c4bc5528727`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:761d54c1b6b40b43e2fb3064c1c46c25285ba78345f38705681d230f5d0bd9ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122846710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cfebe6aebb208ac18794628f017bc3b8f61288038d788e8a64dd2fa5b349df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4053c8d16e2449fdbac1122e37652f53be8b607a093453ba6bf08e56bd9ba`  
		Last Modified: Tue, 12 Mar 2024 07:56:22 GMT  
		Size: 53.5 MB (53491671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:da13a0b5c77dc3e752cc9d9e185b9c09f2e2064d8e11218ffca5a57406a10bfc
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
$ docker pull buildpack-deps@sha256:cc05c08ca39e926630564a43219ac19163c7e528389960d2fe9e639025638618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c215ffce5e7490aba71d8dabf58ef741bced74521af2c5f27869e888e3d95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0240b8998a2b49677c6ca0a32e10689d5c0117ba74d967e8a6d98fe7a4ae3fa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70037013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca62b11afe7a8431a7e12380500c7c2eb46286dde03a2bf7cf121cb6e7d10708`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b872e7fd396a6833da36a5ef61e35ffddcffce622e76d99cd704ed9bc2bb9c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff330e85d6b2d9a434a86e0c5df03f2fc83d2d5fd31e47532edcdd9512873898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48cec1cd7e892dc51c4f2d7516b2ed8f391e116929b5460e3ae0c976ed050693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ea96e7d1339ff33f942f8cc1315e0731121520bcbfac53669df4bb05c253fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7bfebc01b0982fb9874fe5bc61cb62bf8dba226d5fa3477f593bdad7502621f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7410bad07bb558d5fe093b6a01893c3a2b26334e114a68a3644836299bf37f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b18588551c4d881828aa5f3317b0536cc51d3663c096fa4d1ff409b1a7837e4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a9c2db66277195f38df723d4eaf40817c0a38943d94badc968e39f17f98be7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9d2e59a230a9d4a04808ae004745f51e0e596953a2770503084886a3fb23f2e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79253819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5a24d3eb15d8f3b9ef6a936bb7a9d5b7a210c0779c7b2bbfc59ae6e0e14774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:95b1f86365edd875e362c6d47e79763e1f3b7504f29992ff6abf68cefbf731c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71960165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b776a30a72031edeaea3d61789f2250d8181bfb7503c9857a93cb931e569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:f256363b8d19c54f3d9d3073c3af8cc35a2f36fad37321a3a07521483953a1c8
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
$ docker pull buildpack-deps@sha256:43d3c37b0b77687dac2c85f36cc78a8d7ba9d75699df4a15837516767442e88d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245767248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d3054fd40eb8bac73c86d57a0840bb78a6f10e352fb09aead9f07e2fa02613`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:00:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4d70c07f54619a9053b20d9a7e6bdb6166b2c0fc92ac0d16c2fd1cd08e3c8a`  
		Last Modified: Wed, 06 Mar 2024 04:14:41 GMT  
		Size: 60.9 MB (60905037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786495634ea9b39ce8af363dc672e02cf79588e0ad80bcb2a1e8973f4a188ebc`  
		Last Modified: Wed, 06 Mar 2024 04:15:09 GMT  
		Size: 145.1 MB (145146731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bbe6d1306df1c36062b1e98a162a648bc63b0bf5e17f4d8da4b27fd99a7f1d0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211983091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bb4bec2065ee27d34023214713dc0f920d228a7c758360e797f5e18cba33ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:52:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9f0146508c64525bcfd4953b27c7bc27e67adc334304ff83b5aeae6662c74`  
		Last Modified: Wed, 06 Mar 2024 03:10:18 GMT  
		Size: 9.6 MB (9603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c590010ae329ae42a3f3d92d6d3ed12897e99e829fd5f3a7871b7fe749924b5`  
		Last Modified: Wed, 06 Mar 2024 03:10:38 GMT  
		Size: 55.8 MB (55824995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae87da7abe140f2cc4ac3a9cc942eda5b47996ae7267fc3091a639ffe3ca9fe`  
		Last Modified: Wed, 06 Mar 2024 03:11:08 GMT  
		Size: 122.0 MB (121953048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffa0a62a3ca08a64fc5f594dd3865f6466849059e9ea9990271035c565f7ac5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236009847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb940e7846b8085c7a2712e912b939964cd3f340df8ddee9298eb4c41091a3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:35:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b70f732816698b129506e28d62990303060cdb6a7e3648ecfe01939b8456b9`  
		Last Modified: Wed, 06 Mar 2024 03:49:50 GMT  
		Size: 11.0 MB (10982656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825501692e99efb3151808bc0e1e172221c3b5e177cc98f154198c4cd13cc9c`  
		Last Modified: Wed, 06 Mar 2024 03:50:06 GMT  
		Size: 61.0 MB (61012439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a76da96cc9e5dce0a9fef90bc56f0eaa801b1446afa74bd015e4faf20258f`  
		Last Modified: Wed, 06 Mar 2024 03:50:28 GMT  
		Size: 136.8 MB (136810465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7da210f5779ca763886b072703fec650e315ee5e7e629623cac30e837f272815
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269541604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7332f19d3175ee3933fe937e212c79ac0a51901ff1be57ac0899f1499e6a95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3c4671f11ceaf15eaa838e9bb48af73bd571bc62e8c73f16f42452c9879e0`  
		Last Modified: Wed, 06 Mar 2024 02:51:42 GMT  
		Size: 12.9 MB (12940566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7119467b1655cb90e1b0d916d873f5a33c39b88247a441ed1ec92219f1384fa7`  
		Last Modified: Wed, 06 Mar 2024 02:52:03 GMT  
		Size: 69.7 MB (69653454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea95096a68600f250a17a0068db72e82868688495868dc3313292869df9ec840`  
		Last Modified: Wed, 06 Mar 2024 02:52:38 GMT  
		Size: 153.6 MB (153631975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:34e4e5cf089fa656453136e74481ba72ebf631cee8bb2a08cba9567c1cfb8e0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226585031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e831621e03de7724d7bfc14d46353902b135492ee7d403b3ddd406531a01060f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695eff7bd6c3c722a97614ed18f70c79901aa397e0b9728ba6d390a6d79c0b`  
		Last Modified: Wed, 06 Mar 2024 04:46:22 GMT  
		Size: 10.7 MB (10690550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c9a922c9a515fecd2f06f0dbe92470942ff2d5fea6733260d1fd805ce4833c`  
		Last Modified: Wed, 06 Mar 2024 04:46:37 GMT  
		Size: 60.3 MB (60317321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1acace356fe61ec53b578b272b87ed519a18b63a721cf6adff1c3850d980b`  
		Last Modified: Wed, 06 Mar 2024 04:47:01 GMT  
		Size: 128.6 MB (128561095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:de45a190eca52f857c2159813a4e04c870b4b1dc060f80e0d1b98ce9df3898a7
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
$ docker pull buildpack-deps@sha256:93095312b7054939dfe29b5b71a732d37fbce82b86fc9e4c3089fd25a241e2a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b995f720eea62a403831fa719ba7b986350ef26882184d30d16248f5201d362d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:61c3af39ef5c4a1fc3d7d94e5a0efe5658d79de89bc76acaab85548f7ff423c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34205048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb51cecb76bf4270c3985f87edf86479dfad6fb0b8c868b86493c9d42f317de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9f0146508c64525bcfd4953b27c7bc27e67adc334304ff83b5aeae6662c74`  
		Last Modified: Wed, 06 Mar 2024 03:10:18 GMT  
		Size: 9.6 MB (9603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:780f091a85d8d9109be43edac1cc4bb1eba149bd02145129b2ff856c5e2e60fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38186943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95abdce3ef1c4988b5e5f7cfd3a5561aa851f2dbaaf1bd387eb30d56522f81b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b70f732816698b129506e28d62990303060cdb6a7e3648ecfe01939b8456b9`  
		Last Modified: Wed, 06 Mar 2024 03:49:50 GMT  
		Size: 11.0 MB (10982656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bd11d083e37d1d846674d6b0261fab753fe844a6eb7bd0079327ef5cc3ba835f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46256175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50151c2c5e0f6a187a2b915dcb743d9d92940f9ad1f33d51369b2e0588546691`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3c4671f11ceaf15eaa838e9bb48af73bd571bc62e8c73f16f42452c9879e0`  
		Last Modified: Wed, 06 Mar 2024 02:51:42 GMT  
		Size: 12.9 MB (12940566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d948151551f220922b4d4457871e595725779585a01085b5eb774fdc73e4b24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37706615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee05e4e8257d30fdf8a8bd7955db13f6922c9b2535855edb576a10088fb1837`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695eff7bd6c3c722a97614ed18f70c79901aa397e0b9728ba6d390a6d79c0b`  
		Last Modified: Wed, 06 Mar 2024 04:46:22 GMT  
		Size: 10.7 MB (10690550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:d0f7d7739fe9ec3eec069081fdf2caa440dc47642a9f2e4dfd0179590906608b
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
$ docker pull buildpack-deps@sha256:1e3e2ce08e857e35a43c63ae37175f4e660671d3f4083965e5ca0d901f8cb42f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100620517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0845dc47c291e59d26d0e5d0f2dda3347073ccf12b61bd23967b79f1d98a149`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:00:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4d70c07f54619a9053b20d9a7e6bdb6166b2c0fc92ac0d16c2fd1cd08e3c8a`  
		Last Modified: Wed, 06 Mar 2024 04:14:41 GMT  
		Size: 60.9 MB (60905037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f58e582ee6dfad771b2717c132a1a65917e76b56c8223eec9742b906077b6cf8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90030043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb18cea8d2f1053027c222e32a823b6e1fea22f98d5ecbf3c141614b87c352`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9f0146508c64525bcfd4953b27c7bc27e67adc334304ff83b5aeae6662c74`  
		Last Modified: Wed, 06 Mar 2024 03:10:18 GMT  
		Size: 9.6 MB (9603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c590010ae329ae42a3f3d92d6d3ed12897e99e829fd5f3a7871b7fe749924b5`  
		Last Modified: Wed, 06 Mar 2024 03:10:38 GMT  
		Size: 55.8 MB (55824995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:adb71aa7b372d1c6664c0eca285a06b0683f4a7a11a4312e68cbefee7be608bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99199382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ed358c6c66daf3aa0449000cace757a7bbfe5867ebc95a09c007b165efbe80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b70f732816698b129506e28d62990303060cdb6a7e3648ecfe01939b8456b9`  
		Last Modified: Wed, 06 Mar 2024 03:49:50 GMT  
		Size: 11.0 MB (10982656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825501692e99efb3151808bc0e1e172221c3b5e177cc98f154198c4cd13cc9c`  
		Last Modified: Wed, 06 Mar 2024 03:50:06 GMT  
		Size: 61.0 MB (61012439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:53d0f0e31dca61c598281b7a46c185bc4bccc1083d30502bbe7c91ab31245675
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115909629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461836c430ba635511e1f75bf41efdaf87b62800c3cefa3a24ecd38f600f836`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3c4671f11ceaf15eaa838e9bb48af73bd571bc62e8c73f16f42452c9879e0`  
		Last Modified: Wed, 06 Mar 2024 02:51:42 GMT  
		Size: 12.9 MB (12940566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7119467b1655cb90e1b0d916d873f5a33c39b88247a441ed1ec92219f1384fa7`  
		Last Modified: Wed, 06 Mar 2024 02:52:03 GMT  
		Size: 69.7 MB (69653454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:709ee2e2142e74642b093a5c8c05ca86b2f024d56a888c5d25328b4c779c5bf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98023936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83db2c966a7f686713e352fb1a1ffc3a0be52c2aae9ac8b66870d14cb330d3d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695eff7bd6c3c722a97614ed18f70c79901aa397e0b9728ba6d390a6d79c0b`  
		Last Modified: Wed, 06 Mar 2024 04:46:22 GMT  
		Size: 10.7 MB (10690550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c9a922c9a515fecd2f06f0dbe92470942ff2d5fea6733260d1fd805ce4833c`  
		Last Modified: Wed, 06 Mar 2024 04:46:37 GMT  
		Size: 60.3 MB (60317321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:f028439d1e21418883b8ea83670b1bb142aae932caa17602f4542cd33cb85094
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
$ docker pull buildpack-deps@sha256:ea6528431a9af0aacf1b5ad0f03c8b72a0fc9e49901401ef765b03c8872bcd43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250088348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f899440a738f36600d5a6f50192bd854357b38759a77fab51984c2b4ea4e2fd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:05:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49593e5760d417af1144c55c35eb9e0e2a7460c7656256f5998b9ae8fd257534`  
		Last Modified: Wed, 06 Mar 2024 04:15:23 GMT  
		Size: 7.1 MB (7121797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92589fe65e5594cf3e31809c66ed3274029643ca4cd99676bf7df67e566fba8c`  
		Last Modified: Wed, 06 Mar 2024 04:15:38 GMT  
		Size: 39.5 MB (39450394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadae4da62843bd526e310e7d6931f0c30d16eb92a924a3e436be5d45ba78aca`  
		Last Modified: Wed, 06 Mar 2024 04:16:10 GMT  
		Size: 173.1 MB (173064855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6790111010d47a222d10178b65a9fb3f5f6005cd13de42dcaa018342e2546d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217363067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc3658d0b2091f7b40475a6c7ec3adce3cfdf42bf655b3f261877cd374b3e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:52:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:57:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7fddbd99c87689c797128c33e1f1c9f61160d0051dcff2c4c3051e0caa54a`  
		Last Modified: Wed, 06 Mar 2024 03:11:18 GMT  
		Size: 7.0 MB (7019941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9ea7a997426b52cffbc09e40167bbee3b28329fa851e6e1e5700031231c406`  
		Last Modified: Wed, 06 Mar 2024 03:11:35 GMT  
		Size: 42.2 MB (42240423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb816ff59afcccb02e4382638892e5b8fde04045e946e9f32415b1eb6fa45f5f`  
		Last Modified: Wed, 06 Mar 2024 03:12:08 GMT  
		Size: 140.6 MB (140568769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:42ffd854e75daa213a3a90bbbb36c57e13a9317a767af239c64dd1130620383c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241373030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8332128d09686a1861494e0d65e5a487a1b6c9f0fe88575627fcd9ea5818a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:39:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a73d6c45ae19423adf83856e0bd5b156f302f22361a2da09d76f647b4f81b`  
		Last Modified: Wed, 06 Mar 2024 03:50:37 GMT  
		Size: 7.1 MB (7067410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92327d9c49efd4c50fc3e28a39cb60e6a3f304a87a6afe8f4885ac5763ec20d2`  
		Last Modified: Wed, 06 Mar 2024 03:50:50 GMT  
		Size: 39.4 MB (39365735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2aefef92435996ffb7df536c8882a73fd033bec4f2294acb94cd1a18aa2618`  
		Last Modified: Wed, 06 Mar 2024 03:51:14 GMT  
		Size: 166.5 MB (166539247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fd94324ba87b712f23141440d6b91347506f56b3443c4cc88262115e2a357cd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271270158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559f3af32fb08d7e12e483978d98ae96c6a6a42de87b0e0e4ddedb35a69d1a2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:33:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1cd6dd1d48531afc533d075d66a6fddaee5888dbba2b8247dcd3adcea1a763`  
		Last Modified: Wed, 06 Mar 2024 02:52:49 GMT  
		Size: 8.2 MB (8243679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2416321de37a426f77fbde63472628808acb699afc1e19ddacf4b3e909e93130`  
		Last Modified: Wed, 06 Mar 2024 02:53:07 GMT  
		Size: 43.8 MB (43763759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9841082859ded3148317fa252d4ab05c9e78b45a61c8a853bbac779be8c7f1`  
		Last Modified: Wed, 06 Mar 2024 02:53:44 GMT  
		Size: 183.6 MB (183639981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e898121e762fdc600376de850be35432faeaa4cbe15f9aaad87e2fb618f9b0f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223814934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73033ce3d671151a02ef921d0f0f48c400acf322bfb3cd355e84cac88fec8b8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a92f5c603f4c36022879efbb91489f2c52027f9e7ae958f0f61db3d2df3f1`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 7.0 MB (7036338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df445eb0e6484b70b95bc3da3debd8d0dfbca809dd62d47cefb8ca34f4c11fa0`  
		Last Modified: Wed, 06 Mar 2024 04:47:19 GMT  
		Size: 39.4 MB (39416503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634e85bbe96f4cad56d6662db0275b9dde4385eb833fa7b43795e88ad1106b`  
		Last Modified: Wed, 06 Mar 2024 04:47:43 GMT  
		Size: 148.7 MB (148725337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:6e50ae25cfaabfc5f6cb46195d224209c4c5909f8a9bf7f8e532fd52988b8c11
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
$ docker pull buildpack-deps@sha256:093e213de67157aad5e9363931b9dc7abb198df561d5ca7fd42ee05a0268b817
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37573099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc61e0ddf2f1265350aa7d2df4380e0c5e9be3fb88107a7d8c495039ecafe62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49593e5760d417af1144c55c35eb9e0e2a7460c7656256f5998b9ae8fd257534`  
		Last Modified: Wed, 06 Mar 2024 04:15:23 GMT  
		Size: 7.1 MB (7121797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d5614859dd275008e1346f3cb2f9a701bad80769a30d1b18712953bf7df3a842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34553875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bf063a2f2ab14728f503401f1fbed9f9bf89b86af66e16ed6cf9ec5c49f4a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:52:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7fddbd99c87689c797128c33e1f1c9f61160d0051dcff2c4c3051e0caa54a`  
		Last Modified: Wed, 06 Mar 2024 03:11:18 GMT  
		Size: 7.0 MB (7019941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c7a37bc43eb6b8da73f54b88efb3828d2cf1eb022635d042456111ce2acaff21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35468048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3dcec6ff2ec4a0a701056c03c48becc701d4f0105679f8a00c0c84085d145b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a73d6c45ae19423adf83856e0bd5b156f302f22361a2da09d76f647b4f81b`  
		Last Modified: Wed, 06 Mar 2024 03:50:37 GMT  
		Size: 7.1 MB (7067410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:91acb44d39f9102804b9850a5b17167e3d43889882f8a57c22b9346aa25b39ea
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43866418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984ef75217126be1dea3f9a48e846ceb4054593b4443180dd89a3b5380117891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1cd6dd1d48531afc533d075d66a6fddaee5888dbba2b8247dcd3adcea1a763`  
		Last Modified: Wed, 06 Mar 2024 02:52:49 GMT  
		Size: 8.2 MB (8243679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3fe00ad471a492cc6850f51abf635697501cb22733a201292980ba875a54951c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35673094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ea4456f1bd77a4dedafa9aa3a5afa9105940c800ffd5525914727bb0633891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a92f5c603f4c36022879efbb91489f2c52027f9e7ae958f0f61db3d2df3f1`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 7.0 MB (7036338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:44fd3f944013377caec06347436126c04837bbeebeffc6f1701f3ddd26f10b33
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
$ docker pull buildpack-deps@sha256:4b4aee6ab806ca1f70f2f32a7f359c5fbc05e5b0ff38a42348252c897a395b2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77023493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493ce92db0324f288231e41633bd2c1445eb59e22b226c85d06404fc7c82c441`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49593e5760d417af1144c55c35eb9e0e2a7460c7656256f5998b9ae8fd257534`  
		Last Modified: Wed, 06 Mar 2024 04:15:23 GMT  
		Size: 7.1 MB (7121797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92589fe65e5594cf3e31809c66ed3274029643ca4cd99676bf7df67e566fba8c`  
		Last Modified: Wed, 06 Mar 2024 04:15:38 GMT  
		Size: 39.5 MB (39450394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ed7545234b9f94ec0418e2b081b2bf084227c1f71cef8213e723b219450cea1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76794298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a340863c84c3549e70b82bae506ba95275e5e16a0e4d8668e8e7cc25599989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:52:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7fddbd99c87689c797128c33e1f1c9f61160d0051dcff2c4c3051e0caa54a`  
		Last Modified: Wed, 06 Mar 2024 03:11:18 GMT  
		Size: 7.0 MB (7019941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9ea7a997426b52cffbc09e40167bbee3b28329fa851e6e1e5700031231c406`  
		Last Modified: Wed, 06 Mar 2024 03:11:35 GMT  
		Size: 42.2 MB (42240423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0901fa440c1f905a96f06e70827ca1d05dc8d15002e464eba7fb5cef30635d8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74833783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7cdc334b48cc07b03d0feb8577106dff50fb6c520f8feb93ef1b641d20f0e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a73d6c45ae19423adf83856e0bd5b156f302f22361a2da09d76f647b4f81b`  
		Last Modified: Wed, 06 Mar 2024 03:50:37 GMT  
		Size: 7.1 MB (7067410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92327d9c49efd4c50fc3e28a39cb60e6a3f304a87a6afe8f4885ac5763ec20d2`  
		Last Modified: Wed, 06 Mar 2024 03:50:50 GMT  
		Size: 39.4 MB (39365735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f6cb4f947f2e59872ced21dc90dfe61e3b8cafeb9fdf54b5ab85dca0d38f492b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87630177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5683974fd5fec66709dd16f0694e8f33163111f9ae05cbdaa3f94876d731d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1cd6dd1d48531afc533d075d66a6fddaee5888dbba2b8247dcd3adcea1a763`  
		Last Modified: Wed, 06 Mar 2024 02:52:49 GMT  
		Size: 8.2 MB (8243679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2416321de37a426f77fbde63472628808acb699afc1e19ddacf4b3e909e93130`  
		Last Modified: Wed, 06 Mar 2024 02:53:07 GMT  
		Size: 43.8 MB (43763759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:405bcf3102e90966c04536e2699d5a877d9ecc36d137355101aa09ab3cf5feec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75089597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51541b954c6f35a7e17b244341e84398bc948fcf6abc5b7fd993c58d7b1c2f6b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a92f5c603f4c36022879efbb91489f2c52027f9e7ae958f0f61db3d2df3f1`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 7.0 MB (7036338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df445eb0e6484b70b95bc3da3debd8d0dfbca809dd62d47cefb8ca34f4c11fa0`  
		Last Modified: Wed, 06 Mar 2024 04:47:19 GMT  
		Size: 39.4 MB (39416503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:33fd523e6d918b2d066038992f814ff881eb6de323d3c70b7fea851ed1c36be0
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
$ docker pull buildpack-deps@sha256:db9fa21724f9ed2ea02b2b5ece7b9b33c539c1bc812e1f576c88854470db0c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348878735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a3793f3c6079a0170f05599f2735b64766d39d2c34374471d3bcc6ca540d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:54:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567db630df8d441ffe43e050ede26996c87e3b33c99f79d4fba0bf6b7ffa0213`  
		Last Modified: Tue, 12 Mar 2024 06:03:18 GMT  
		Size: 211.1 MB (211139445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:091d6742817a9012801ddba3c88d22130da8ec2a52a82fdab424cadb8c02672f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316009389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d577d2712bb80823634647f21b499b3b5950339ba80b463b1d5ec39552739bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:35:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9069b8edc3144ea7c7fba8c956dedcc448fc0ba006a12c9cfe4ac23f05569d`  
		Last Modified: Tue, 12 Mar 2024 01:44:12 GMT  
		Size: 184.5 MB (184456518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1919befcfca67d8372abe16832d32831608044d6022238cb362f0ad8296441a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301423265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c58b41f8b222deb6863d767951930f9431b526720e771a43ecb9c74e996cac2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:236f29b4631548c327b2d1d0590ef8011bff534a87f62bfa2a68a91f8d8c3c02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339703020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02567629c9e9c4dc92672656620fd7750ba05eb4c4fa2d86a63ac92419d2dbe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c418b37b4bcde3a68933365b172d45ae5f3b046050fde08b6eeca5d57994a08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351512027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f67448ff33c81527caf039ca97b379daa5a4deb989b5d2bba32c70ec9a07deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:41:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee485e7c553f7b1465ed88918f0904a411af3dbb0918703ec7b92192eda6417e`  
		Last Modified: Tue, 12 Mar 2024 07:54:34 GMT  
		Size: 210.1 MB (210058424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3e131fedd6c0a053f4d92db50d59e106405e5047e2b38db2db93bd1cbf4dc08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325858634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9827aaea1a13889e5939e08ab8f7c05be47b277bcb8f5da059cec0ab3b14c450`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02977c85a258d317066e5a1e6febc79a4caa2a830ee66f596c866db50d3361d7`  
		Last Modified: Tue, 12 Mar 2024 02:44:46 GMT  
		Size: 189.7 MB (189698984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d82d41cabf8e17cd142de9f607e0fa1c803e30fc7c1c11702fe2eff44af1d4c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363009215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6db4fb9bf6b421d4aadfcc2a56b963ee8771a5c2e2813078cc1e73b7a33733b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d9053a0f750316634df779ba70e4b32f8618c06678f58ba3e14bdbd7ec4d444
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0947a371e12fd46d0e731838049ffbbc92492031782ffcf22ec58497a4e57efd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6654b38164df76c1496278c128a09a6fc9ea1d703322ccb6eb98f578047b2b07`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 183.2 MB (183164991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:5a2e19035cebac59a36067884b5ab60cc5eb21b536b7e4fd8a10da404752bd77
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
$ docker pull buildpack-deps@sha256:f918d4428aa964953d5aff1d5bab0b82c372f9d3d38a2d12b77458d37c3ca34a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279780099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641f1e177d185a2b62526fb65c672b0fac9bbfd5897ebd1aaf0eb1e1d8b13450`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:09:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b21ae994c2a096a3b04d9c7a1755c60179f67ca190f61936d6da7e1729ee588`  
		Last Modified: Wed, 06 Mar 2024 04:16:41 GMT  
		Size: 44.8 MB (44763285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a90bca93d1e62f99fd8cc0756b7bee297e054ae196104b9fdc912a38ff8fe2b`  
		Last Modified: Wed, 06 Mar 2024 04:17:15 GMT  
		Size: 197.1 MB (197070772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5289f79ac531efb8ad33bd0b0b6292dc4e2f62c9ce303580430f92ceeba1f221
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246446751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4c6acfd8c70545c484652739cb0d03b4027ea23f793b63b1e6b189a815dff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:03:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155ba03212deb920e05dc77749cc267b5b6fcdc16bda27f00864d27e0607886`  
		Last Modified: Wed, 06 Mar 2024 03:12:42 GMT  
		Size: 49.0 MB (48950883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181be50d83864dec48e37287e8806806c68c94293ef26ba5d9653a7ff9a4b7b`  
		Last Modified: Wed, 06 Mar 2024 03:13:17 GMT  
		Size: 162.7 MB (162659026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76c20fa0c78fc1271616d426ea1dbe616824c6c892c1bf9046e262596f505152
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271897474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d283ee2047a060b9e45a0d79315d06fbc480c77b2a3f50527f6c718f2adea4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:44:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d621ac8cadee2671e19aa461d0119c3f949da68efa86d87ba2fa18fbe4c9e4`  
		Last Modified: Wed, 06 Mar 2024 03:51:40 GMT  
		Size: 44.7 MB (44677268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d35f0efc15036eae5bb318b2e83575fd707a37e6dc72f457a6f570de89d772`  
		Last Modified: Wed, 06 Mar 2024 03:52:07 GMT  
		Size: 190.2 MB (190191833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ab7b2acc2516219c4ef73f4b519ca6601deef8c0a12945ec8150420b6b56bcd9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293684369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ffcb209559ecddada302e968d75fcc80963af851b66bb76f1f3c712f1bb074`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:42:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa179ccd4d1ba32381ba7b18ea7a19fe2a7be5021377e619dcd5ea87d94344d0`  
		Last Modified: Wed, 06 Mar 2024 02:54:21 GMT  
		Size: 49.6 MB (49556847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24aba2c716f2fa40ca775335da4d638dd85043cc5ed23691c0e7ff819d6012f4`  
		Last Modified: Wed, 06 Mar 2024 02:55:01 GMT  
		Size: 200.2 MB (200194410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bf563f492cfdf4136e50962e79781124e89f7ad8d3c83ee9a7ae7900c302bac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258272975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3b9652943dd3a8d4114303ffd5f985dcf0b6b5726a1399f28e21d58d48fe8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4dbb0d5afb81615197531053990f5a73783a82aa400fa0f09d685d800e4b3d`  
		Last Modified: Wed, 06 Mar 2024 04:48:04 GMT  
		Size: 45.2 MB (45232146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938a3723c4442291047678d7aaf3a42732033cd41bd537189884332a3986f57e`  
		Last Modified: Wed, 06 Mar 2024 04:48:30 GMT  
		Size: 175.4 MB (175394105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:b2fb7a10e28652e02c3191ce47a15c8acfd40efe3c0321b90f0ca10151e5d7be
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
$ docker pull buildpack-deps@sha256:0fca5ff13f7f7b5e8298b93f28e15134e4b2df1daf8baf6222f533d87509be11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37946042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1bae1a972ac939e27c44ab147653e269f4987bb9df150221ac1d013ec897b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7dbdd2bed195883ab42ed0ad0b96818a1787ca8e95534f13c5d82a54621cef1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34836842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a886df4f2c14a8b0a45e16f024da28bd47814a1fbbd2a042287c8906a1fef3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4341891a0761c7bcd09df0d6c13682f3d1c1479160b0333bf1089308cb974b70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37028373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe26cb29e36768799cbb3f4712ea4afbdaf4140eb64b1b05e8c996880413533`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d305c5e6a0a1f1b89f5121496c829e2dd3e93d7fa8a139a2eecaa361e0c8fbaf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43933112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f789d7772d1087fb0373a1bca7a85cc9eded48bed7bb965aac975c8f30e81f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:72b4793c911a7c181fda7bfd7b1ac2c37d3283cf9cbe8fb031646d2175bbc135
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37646724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901ab9ff2fd6adaa5c1a48a8a562f7cfe812fd1b5f12594eb071e136f4bf200a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:70f090b9c541b93b5f9ed34bd50da2aeb9a3ff4a427ae2f92f661d3f74c0b001
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
$ docker pull buildpack-deps@sha256:419609933b12ca00c8a73e76e6cc3495af03cc6a0a55fba48a6587ea534edf82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82709327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57264a7b401ab4cee2930269cd96560c3f9f21633772107aece54ae9ca0f535e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b21ae994c2a096a3b04d9c7a1755c60179f67ca190f61936d6da7e1729ee588`  
		Last Modified: Wed, 06 Mar 2024 04:16:41 GMT  
		Size: 44.8 MB (44763285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b1e9d9758301286327426af6e70aa5e7b8f216cbbd269c7edb29a983d63f446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83787725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9df0c6a52502c3869f438d017cae886cfeaf9e60f8fffd62af11e496fd0d92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155ba03212deb920e05dc77749cc267b5b6fcdc16bda27f00864d27e0607886`  
		Last Modified: Wed, 06 Mar 2024 03:12:42 GMT  
		Size: 49.0 MB (48950883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b013931b7d46ad0c87a33432be075b94d81143b739e990ba3e75f0c02f7dae3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81705641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e87fd7008850f0b06f056c883613692b0dfddedd35041aa7b0698c838e51d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d621ac8cadee2671e19aa461d0119c3f949da68efa86d87ba2fa18fbe4c9e4`  
		Last Modified: Wed, 06 Mar 2024 03:51:40 GMT  
		Size: 44.7 MB (44677268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bcdd59a28ed12834d023ba530aba7e94e8c017295320aa4f73958d863770616d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93489959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4557f6a8a7ff4ac3b6bdad4b5eba002b8979f1bf9ad6336c32e511facc61e88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa179ccd4d1ba32381ba7b18ea7a19fe2a7be5021377e619dcd5ea87d94344d0`  
		Last Modified: Wed, 06 Mar 2024 02:54:21 GMT  
		Size: 49.6 MB (49556847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:edb7558a64f98191228b4671e70d1a48492743b171a4f579192d2e969cafc1ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82878870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ffb3abe7aebbf4aa283e2d47a4d095cf8871f1e827a00c764dde4fd926c076`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4dbb0d5afb81615197531053990f5a73783a82aa400fa0f09d685d800e4b3d`  
		Last Modified: Wed, 06 Mar 2024 04:48:04 GMT  
		Size: 45.2 MB (45232146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:c39d69d10d0140c4c4bf04d1efea4fe2854fa91ff1ff38c0828f32bd9b9e404d
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
$ docker pull buildpack-deps@sha256:259dd02ae96f2d1babcf2983e064912b0e3b659930fc6be79a8522535248e9d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318695257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7c40ab633dffd0bfaf07763af95a466147808ffc85bc8c9eb79fb712220c04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adea66a5a529e25830935a61441a370c0563b30d99ea2da7a49e53bf8108fe9`  
		Last Modified: Wed, 06 Mar 2024 04:18:24 GMT  
		Size: 228.9 MB (228943762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ba0e14a02d5e19dcb27e9e14af9939b30f7878fb599510a1f00d51db45e47c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273230848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576daa73dca6305c7ad39ca45a2e5b80acdeddc0fb2197af8d139a7a5fb538e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:08:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e01583a141e97ef5a0aec445ed9f7e14e941b8b3e37745c1e36c3109b96554`  
		Last Modified: Wed, 06 Mar 2024 03:14:32 GMT  
		Size: 183.1 MB (183135775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:45ebb68136dfda231c4d3a51c9527ad2063b899981d8d6438edc8cb96f417dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305425921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d15e3ee41e130ebf4284b61a5e0347bffcb935d8c2be0e9fac98e091c91b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:48:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9974eadb59c4c8a7258a03bdd5d5182c454d60c821a9dd902e3c04eb031390`  
		Last Modified: Wed, 06 Mar 2024 03:52:35 GMT  
		Size: 45.8 MB (45805608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca642e4c3164d875c8a8e31782bb31faf2f4b630867d243eecba4e0ee7953bf4`  
		Last Modified: Wed, 06 Mar 2024 03:53:05 GMT  
		Size: 216.5 MB (216473828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:baf0bf3926067d244a5c186b6b0029a1b09ed610cc3e37331ba14cd48e9d5ff7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335846262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9481a6c3ca7d56bb183ace9f2a0e456ae608916c120ca6224e2675325199e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881ddf165df7bb2420e4acab24b0465182f8afbef4c4f87365c28ac2fb58bd85`  
		Last Modified: Wed, 06 Mar 2024 02:56:32 GMT  
		Size: 233.4 MB (233378799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6d1af75975c131519bbc8eeef86a9312c981a838d2fcfc00dccfdd4a7f99141
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301888562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def7e5ea62cb995f9b4683cfad978dd3e5956d619fb317798e5bca90d3796de1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1671ccd52fd4caa5e52f088375d19d5cc86ba163b0350c95ff464ebb872668a3`  
		Last Modified: Wed, 06 Mar 2024 04:48:54 GMT  
		Size: 47.3 MB (47346503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fd1b8866a23f60ebd429fa73528999c0080ab66d901f8ef47e7450888952ae`  
		Last Modified: Wed, 06 Mar 2024 04:49:26 GMT  
		Size: 209.1 MB (209074799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:de0d254873c7b223c0be69fb3fc44c87eae25c0c69f8cfacbe686902282ab12e
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
$ docker pull buildpack-deps@sha256:ee6619518234d5405ba8f94421cf0080c2c2e5951fe4e4b94bf2e6b5ef53dd93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44007564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e663bb54ee5c1f72bf54c4d90d616ceea2a986638d02a9ac69f807c6725c956`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:350010198cea3677c190329cf929db66bf1c1306a773c97edb58fa61e01a66a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40333879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2aff73dd21653f7ebd3038ae640fe1e4ce71c3188a91f5306f5335cd803db9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9cf4aef16cc9d6aa4a3c6a5fe99c6c6037ac19f9f553ede8bf3d67a2702e178f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43146485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa467416227b588463fbe2b6f19975d7c849d6cb4b7ca1de7c1894a75a0887d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4337421100410698f2134a79ffd494f3ffd953e745681509bf17625676957db2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51415051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926f624c8bcdf5f2ebb3a4d1d357cf9c18d80e976f254d0ea5352520e6ba7508`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:904cba7d3db15ea7e0ea12e99f42791db89e7df90cdb1bacfb3e7053d22c7015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45467260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8a74f855b84ab2d1fe6fc5fd545b465b0fcd64443b87db9434e77505df37b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:d6198b799cac296e3b53289f88e383aa1cc4f2b2fef634968cb3cd2dd9211a2e
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
$ docker pull buildpack-deps@sha256:e43c3e34a53dce68d563e649080229cbb53ac55992a35e06c4f23cb2f29a46e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89751495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97da8472260a449f47595b95361c39f80c26a5894437f82fce55171b89b43d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:27735ee07214b2f855072fcd4e72b7ad7424f03fc6e9df5c952927a8fda5a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bdee64687fff39f7a4891dd02e5902accecc0de732d5aee169f276d2af04cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:257020a2cf4445996e0a6d9e636c95960ae5535fa037c2f4618b9cddd4a5b649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88952093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27519f55dbc4b5484ee5cdac3b1b800f530a6d11c3700d462f995d64c53e97e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9974eadb59c4c8a7258a03bdd5d5182c454d60c821a9dd902e3c04eb031390`  
		Last Modified: Wed, 06 Mar 2024 03:52:35 GMT  
		Size: 45.8 MB (45805608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4abfcbfcbd30feb2b4bfa41fc5fd1b18dc1b0e215977949d3c6a6302f99ef900
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102467463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb035723872aeb49e171babb083d8929637be280313d4c03325efabf9a82b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2c4aa9aefe1b606f624d09a75c8bf230a5eef05c556dcf9246644e2a7944c1f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50aa33049ec903d31f3eac096479589f99fd99660e241a06945f6d97aa2e4e32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1671ccd52fd4caa5e52f088375d19d5cc86ba163b0350c95ff464ebb872668a3`  
		Last Modified: Wed, 06 Mar 2024 04:48:54 GMT  
		Size: 47.3 MB (47346503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:d58af141d3f29e8adebbb0e8338a2eb6834c13db0122b7b2859d30fb072d6c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ff80bd769b65dd85501684cdc4e819a46ed39638ec413258a90c08e6b962247
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311905592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea119635dd515e55aa2d8a34af1fa35d2a5d0c22998ae58ff28637215f9df67`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:57:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c719b870d0be3d68698a8ab9d2604ba1d9b85d3206a13ce6f1e5c50928dcc`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 51.9 MB (51877435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a275b8bae6bef10ec9dd71151b41617e72eac0780ecbfe93ee1dc86db2f5e9`  
		Last Modified: Tue, 12 Mar 2024 06:05:14 GMT  
		Size: 191.9 MB (191942628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b4761ce8f33fd0256c24ca66d9e214b4def4275f792ed17b05d5a0bd1f313539
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277728447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b3aac61bbb0a61c4a7044b56686673dc640b296ffa8d92bbe4f9451beb1940`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb7e022e9bc1cfbad07b9efb81d22c724a86aab30c7769950ea7a0d6ceac7130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302488134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5a5efe5c6052414a5d5ff289e9a2bddbc111ae796933875d6253560f57c555`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c2513d2262991ad3b0725da9db46b8706451ef2bb7a7617ef8d072bd83ac99eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321337763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6695a60050d69b4e529a4b0964e37e47ffb1250be9da9fa2db10edd9c6c64362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:46:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4053c8d16e2449fdbac1122e37652f53be8b607a093453ba6bf08e56bd9ba`  
		Last Modified: Tue, 12 Mar 2024 07:56:22 GMT  
		Size: 53.5 MB (53491671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611538514415c639eba0b1521fa6f33ff37569ea8882616480d31e1051e4242e`  
		Last Modified: Tue, 12 Mar 2024 07:57:06 GMT  
		Size: 198.5 MB (198491053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:0cc704fc1a7999e2180ad1fabafd497a64c6878627285694a2b4ccef23bc24ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e51e1b189a7ae90f38875e03231ec1558033fe3d59a714160fea3fc0675dd87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68085529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69123c5465280e07adf01a66e71dfe077eb93deb346ecbf80550e5c64893eada`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:39cace7737d92c1877b978b17ea755007f11fae3b0354febb96b926ea789a364
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a00299cf4b286e5c1a38ddaa2ef2181c0c8e4478765e738a82224dc5a27d73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e07c75aa1137c27d17351f9ae9f63806c460c994d42c8332b9e220d8c773e4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf536bc10e09dbf65f656f85df100c2d17a1ef16c0462ed8c2db153991ff5f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8275c22139b832f406cfbd9b9bc4ce66f57013e8dac1d64f3135d1335bf5415d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69355039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82149eada0485f28a9641351fd752fc666fb669e44e750855f16c629979cb5df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:4489872a1a88c55054fa6fd1f8b5c5b1e166efa10fc89e135cd2e17b6bf44a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:16b36fe965724b637f9cac1496ac57fd7bd3455b07809a8c242ed4856e011b18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119962964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9af31b6315761c93e7c05e123a139ac51f11ab859b941a1334e68f40456d56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c719b870d0be3d68698a8ab9d2604ba1d9b85d3206a13ce6f1e5c50928dcc`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 51.9 MB (51877435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e68bd043cc332cea5303fe5d70e40abba8babc905fe8242e633bfeff78515f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109594526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a938f58ea7b43cd5617321aeecf8da71571eaa469c87c48c4f70b9012268942`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8dd2c71b6ca885b1a3f1db72d9dd3f5eed70ad1091ee90e19e14b4e0e4523a8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118970337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9004ee3288570800fdae2c07356f979cc2b771241cdd524555c97c4bc5528727`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:761d54c1b6b40b43e2fb3064c1c46c25285ba78345f38705681d230f5d0bd9ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122846710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cfebe6aebb208ac18794628f017bc3b8f61288038d788e8a64dd2fa5b349df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4053c8d16e2449fdbac1122e37652f53be8b607a093453ba6bf08e56bd9ba`  
		Last Modified: Tue, 12 Mar 2024 07:56:22 GMT  
		Size: 53.5 MB (53491671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:f52498596f150be4024faf66fee96f08082c00a746085dc3dd2ebef34a64e12d
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
$ docker pull buildpack-deps@sha256:5525479c6bd58580e97a3ace40e7528bf8993dd51b88c9a04c14a8e9e130d6de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322422175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc59b5e9a715a4aba00120c58a0d109cb398f62d246f22fdd08dc70f5ed695c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6939aa9b63c6ee738fb4a9904fac366ecb96aec3d980993009e3b7ee3f7516`  
		Last Modified: Tue, 12 Mar 2024 06:04:18 GMT  
		Size: 197.0 MB (196985243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d6c8de5573c790dad1f0d4f5e6fc7c345370f46e3f87fc58045ee725f5e13b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295444734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3174601e5e1c389d2a7b21528e32c54c56c824dde8eef8591350957b9d5e97d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:38:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2f143fe44237c686e570db73ca8e79a407a12cd45adcb3067acff6628c74a2`  
		Last Modified: Tue, 12 Mar 2024 01:45:14 GMT  
		Size: 175.2 MB (175154282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c551c6dc6428f67f0448029cec06132e35b4812157ab96872a3f29b0c2f44c06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282917380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f56d6be33b4622a1fb72ecf376d307a70dc706ed4961f68488af7406739dfc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6e8fbfe95e9b8369601bc38a647238884aada5ae0bddd32c12e08f575d97422f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314080526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7fa0e4cf82f8321955d4c9516654fcc3ad4cdde3183ae19e37e2f7fb35168e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d317b4db41e297cffa1559c871d84437b3544f7a4c04d6cf339cd4e8caa94c76`  
		Last Modified: Tue, 12 Mar 2024 01:36:09 GMT  
		Size: 189.9 MB (189914923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:47f0366cedf269210ea0eb884035b03fb8784137998070a0cc96ea9f9b46f333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328144268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011ffd2d7f928a18305f2c51c05d951a8520f8d609612cce9b4dc7da52afbd27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:43:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632a01713bf6f27a1de411f14f1e21b375412e471fa832f03dc7ea3c86a0a51`  
		Last Modified: Tue, 12 Mar 2024 07:55:07 GMT  
		Size: 55.9 MB (55927686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfe6f6eb32ca002367ebec491da1c709c88fc7418bca1dc16043bf62ff525ff`  
		Last Modified: Tue, 12 Mar 2024 07:55:52 GMT  
		Size: 199.9 MB (199890619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:65bfe652bf6a879063dc90fab2ead606e4c8c5007949963d6d386bde1575d721
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301446653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f98dcd9cdd8c1aba9729a37d183692e64affc47fc9963aa5ee2e2aa200ebeb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:19:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f183b6f40e96072119ab41213733a9079dd8d43cd4a7c36f9f7e3531dd614`  
		Last Modified: Tue, 12 Mar 2024 02:45:50 GMT  
		Size: 53.3 MB (53310696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21edf61173913e6f42aa80ddb070961a6780a6703f5e284ec12292d725922b`  
		Last Modified: Tue, 12 Mar 2024 02:47:47 GMT  
		Size: 179.1 MB (179097827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:18c93cfdecb6b18bca3bdec1a55b31965e67effc9c501720d20a7b281f102f83
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330940717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa57c33a89d91a68809c39953c3546e688d9ab59fa0877c1c66e70959a068ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078e6b4fd896687174cc2013bea6ca7f49c8cd898255e8d37361b8486cb7fe25`  
		Last Modified: Tue, 12 Mar 2024 02:22:13 GMT  
		Size: 196.3 MB (196346975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ae021550b3144b31854c9a0860d42fbd41b41873c8452b715d6352026953d304
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296028247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf529bccc5415913766dae6191155093d8451c04b4eadf15a9c51c013729772a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:20:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dbe74529fc57e85a22f94e3442e33e7b5d04e9a4e5bfef8746df1fd2841eb8`  
		Last Modified: Tue, 12 Mar 2024 02:49:00 GMT  
		Size: 173.0 MB (172991681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:b8e2bc087998cb449bde0442739be8ff76da6d53707322d24a6bb7166b1437e7
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
$ docker pull buildpack-deps@sha256:a9ecf4ac7eed2d5a6601d74158afb6eb3a39ff06a98f23e53a9516a9986f1fb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb203964ec9feb91c764093f1aced9c543ade1c87ea002f782a9bcfa32ab536c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a67278d6f9005c7ac4434d07aae51d0d58c81354ca08af9d81a65326d9f47996
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67961591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb87e85efadec30a80462f3109359eb9c7e021644e1015a74de1bff8ebe2da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cb47374993facc2c740f43765774f17231eab30bba2e11689a4647ea5a205c1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b163ee51a07d82df4e4983f0ba5ddbe7596b7f223e0ac37636dba0048eb0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0b9a2f5356e7edf45a7dc9353c26553102e8f3ce722ba6240a23a1b49d6132e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69471302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0115b7e6179997944d5abffabfac54fccdef8a92587e427f5768a9c9de20880d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff0a5ddd9d781307de313da1795a608ac9ad369d6764056fbc13e7a64f89198b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72325963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec92a70eea4641cb7a6a60aa8a75b0981ffebfa175089e815dcff73ee1754808`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0083cf345719f184fe22aaf238217142b9c18b3a4aa7abceb916e0924b123281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69038130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da36f695074cd766511cc8a44b9629c55bd5e1999a49245479a39221b2fb53d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:92f9ed323d1b94f81fa714490e510187fdc47489e4e68c451511adb10f217626
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56413e6990944267231df1e0c2432576718f56e83808120185b375c50b89b503`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:754786485ef09e39e6946ba3605b887177a768e34aa803b1230314cab507d40e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68960835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81ec6160b5bfecebd05bc6c3b675a4a551c8a22dca8920e5e6902ce190090a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:302de6ccb1237785333412d7d70bdb64edad7f5c5c4bb80ee579b383d6f9319b
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
$ docker pull buildpack-deps@sha256:a46617c635cf7c885e2f741b3308f1e65c98a1e19515a0954959ef94081812d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125436932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9564ff86d3091c7760338926393f13187612898bbae224360fd36969581b1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b82a28618cd428cb303a3b3fed70c1fbaa15e2d7c0ec88a5213f7e5fb324f24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014ab67dc0681bc0aec86fe312177d276bf8643ab040b0b846c51bb075db4fe0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9dac4341f985ba6f6da87a345745251d4e1f1f88f5abbc11ff21dd613f0fbe1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115478050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd4d99544718ca88c6a40d99f13d278f6c4ab785d0fcac3d99148b6fe4aa000`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:50f9d48738e31a49e12cd8da39a4d5960ebea181dfc08c81fb3eed98f5ba53fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124165603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42ccb34be84e46eb9856d81064e642bfb16e932250605147287fc82f49f772a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9d2d1bbeb1a9c7d440ca0bbdce6e3b16fbcde367d9fa13057b28010dee90f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128253649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f814dcaa1597e9d66a274df2456808589086d74b54a14e03d9c850650bba5ee9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632a01713bf6f27a1de411f14f1e21b375412e471fa832f03dc7ea3c86a0a51`  
		Last Modified: Tue, 12 Mar 2024 07:55:07 GMT  
		Size: 55.9 MB (55927686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5fa1a7821881083e40ead9bf790cb63689f782905b96113519aa764c7b1636bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122348826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245a78fc3d28c1fba5c24a42c04a692d9b60f560c68e5aa3055dc5edfef73ba4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f183b6f40e96072119ab41213733a9079dd8d43cd4a7c36f9f7e3531dd614`  
		Last Modified: Tue, 12 Mar 2024 02:45:50 GMT  
		Size: 53.3 MB (53310696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ca5ed2831818a94c464ffdf78335acca49d1cd6e75f265e00fee6da1246bed8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71d28760fe78cfdc496496e01e97a5dba19414830d62e4ece7deb0bf643ad6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dff51578c019416cba8959947215e6ef4365bc531885e874fb8a3e4d552facc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123036566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200b30cd7082400a7d00f01fa2fff2d45ffcf3f75e979a708c121c5d07fc7ec1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:2c0c1638d1e037a1ab747f02c39b7e54fff548be0fe6f230a28c2b8301fbd20d
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
$ docker pull buildpack-deps@sha256:25f20fd3e3c8be1e9626c246986beb400ccfe19b0ab13d57127399927801d499
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3829553ca241eb6ec827e514210faab2db77d5f4a58764d0dd5a00f97f4a049`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4604b8d280097513158cce324d296dd8806f21056e09f659b28c7a0b236cc7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f5e6d0ea8c878fb6e49c35a11089dc2a50afecb3abe7942942297679e212bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cfb748d851e2e3cfdcbc1be1e1817fd84e8fff94498702a724beb1ed87b168ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126317289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2a90a637715c3c6bb9034dbf6c64f7ea86758a8c52109f24996208cf4d832d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd1553434a26aadad218bb6dacdecbc747db860969aaa45222d479b12c9fcdb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137164774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81cdaeb1cfb57a71b96eb9e0a8673ffde7936b504bd716ede73f435391fd8db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:651ed01e0f955ed10779074376f6fe0ecb8fe43cd832988c176b5c4fe3d8f4dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141453603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7e7c3092c37a6e5c2b8d528da777020e5b3d0cb69c67d216649c3d7c239f87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4ad06509257def2a4df2513623de0665e807666f3c0d942042e3228e12ab49d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136159650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d33af04fbcfe6b33eccfc1638aa0f25b79423288344805b88451266aa3eb56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9b03894e8f0ddcd1ee80a6112c6aab6e27a3532fbcae3e272cac191218353386
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148835718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f9a694cfc75a976c7f54142f0a5c4745f9d4f2a0ae27d4a673a3987c4888b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:793d4d8f8b9efc430bada65e9066cf9215dc96b03c605ae45dbaa4fb24ad830b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135086824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329d23986398ef8817d6d027b58b5b6edab632660cf8b81c3092f5ffe0a77816`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:0658bee092d2e837c5020aa7effee407a2c7b3bbc59cf1da6235c482ce4382a7
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
$ docker pull buildpack-deps@sha256:57ac383c326ff712bab6fd9b199d44510599a4e0281a3aaca37b8586d45a2223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.0 MB (387988231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43d2453de4fe2fb28496f33f2180811f598511875812a4066bea677fb343dd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:39:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da143e0f6d9787b0c89d6405a787ded9de6dcb65f3b9717f82da42f10ff997b6`  
		Last Modified: Sat, 30 Mar 2024 21:42:57 GMT  
		Size: 66.1 MB (66121672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c86b463be435223351150e682274c024736e2d18e8692edb2df9fdbbc0c419`  
		Last Modified: Sat, 30 Mar 2024 21:43:36 GMT  
		Size: 245.3 MB (245265582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:17bc4bd22190703d8768aeaa3ca6bcd2210fc641746d2454585be08ce56549bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349646719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614f6de95aa626bece07ebe03b846284624db6354ec954386925ca06485d0083`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb3d107ad7b8f22e25af7c2ea21540943257d714d5f5258c8275e541fd460cc`  
		Last Modified: Sat, 30 Mar 2024 21:20:04 GMT  
		Size: 63.8 MB (63848526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8556d6df8b94862fc63dfac7c0bcbae4ab10302c1f9ef0b871b8fafd147bd6`  
		Last Modified: Sat, 30 Mar 2024 21:20:42 GMT  
		Size: 213.2 MB (213207955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:871e0f29584780024f2204c980284b9c9391fec747286a83190d491d200a6814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332812461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee2aec038450d0cf24a4e37e4f23eda53bb149657b4ce73450749cff557bbe8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba4b082de66bbca9897c8dba7f31512bba321ddd2a661347d670d910b4ef36`  
		Last Modified: Sat, 30 Mar 2024 21:30:50 GMT  
		Size: 61.3 MB (61251721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9506c1ec3f4d514c50744f383e5d6be73cb1ec6ad9ff611f2f6c6044f529c896`  
		Last Modified: Sat, 30 Mar 2024 21:31:25 GMT  
		Size: 202.1 MB (202137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8fdce59c69a1449570ad7e28d7d6a3c93d6d22fa193133eeb50a19328c2ba05f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378477580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1747b554c7d67544ddafb675e6be262cebdf69160ca27b8626bdee79cab5a26f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:39:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544cbfb4f7236143d102b4ef349f35d3d31527535f242406bbfd2d42dbfe60ee`  
		Last Modified: Sat, 30 Mar 2024 21:43:05 GMT  
		Size: 66.3 MB (66331165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c307077e7d76abcb4bd4d45c8ace8d03bf5ecdf42e3cc300d9004aa74bbf1a`  
		Last Modified: Sat, 30 Mar 2024 21:43:36 GMT  
		Size: 235.9 MB (235940025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:54905ffedef969cc2e213a1e9a0fada1fc515acd5d1f63592aaf3178675e51bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387860877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fdfccb3460ac7002fa33cef8001a4588dbfc8aa65b902e39c6fb38fd8f1ecb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a15da4ef836ff60f9c28ef8b15ef8794d788a67c0a3d58b61d51a0e65213a7`  
		Last Modified: Sat, 30 Mar 2024 21:21:45 GMT  
		Size: 67.9 MB (67876237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51302bc05c4c173523b513edf1b3957871cd4387ae1b1a565c5bd4a3eddb7c6c`  
		Last Modified: Sat, 30 Mar 2024 21:22:41 GMT  
		Size: 241.4 MB (241417390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b5224f59c01c64b248e9f48214432ae69669ab3e3bbe2f36a4412b60b58e4fdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357495125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3615639b43b8508a560b974f0f2c8153011ac54069af729c882ebd1149beda34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec5d517bc6924cab27f5df1f01979046acdf9cdb844cd5281549ae70cffd261`  
		Last Modified: Sat, 30 Mar 2024 21:49:28 GMT  
		Size: 216.2 MB (216190767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ec624754a8b69473cb9b81413a4b282e6cb28ba8f672f0e5a99247b21d660ebd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401680790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb5830486e828fd2cec3b7fe5910b5925f3d26950aa5db6ee446be40af0f264`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95220faf903de5c246bc60d7f00054712c075484056449785d59c657e22436e`  
		Last Modified: Sat, 30 Mar 2024 21:45:39 GMT  
		Size: 71.7 MB (71689301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d202211364551a66c5bdc24a551df53c88b1d009232162339febb791ddf65fb7`  
		Last Modified: Sat, 30 Mar 2024 21:46:26 GMT  
		Size: 247.3 MB (247336595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b8c90681410c7a219fb7f7d04aa57e2cf52f01af353243fb0b0f43a1e8e4a827
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (420983437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2f4a3271f92c24c8642e98dae057607e7c994185921ee91f6a528279ae0b81`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:26:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259a8b8d1c2e3af16628db8608e828fa16ec2c3aadfd7660f4716db301738d6b`  
		Last Modified: Sat, 30 Mar 2024 21:28:40 GMT  
		Size: 65.6 MB (65606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0b2e0b74b3f4b89240082a552a105f36e18ee01936ae286a1f1b860dc7521`  
		Last Modified: Sat, 30 Mar 2024 21:33:41 GMT  
		Size: 280.9 MB (280894516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4bb0ce013670aae1801c1a36a4458da7b41a079951d7d46f758813926a26f386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369323131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92206efd704f5b1ef33db0289e2f80885e1e5e85e0ce41ca5c64eb7acc42547`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:45:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8b2bab401823952dea39f0a278dd656c849280f02e7b6f21ca4deddc0219d`  
		Last Modified: Sun, 31 Mar 2024 00:08:23 GMT  
		Size: 67.4 MB (67423448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1739ba0e83442ddf7c0d49fb3fe672de89ffe6650ed119a9a2c0737076f8c316`  
		Last Modified: Sun, 31 Mar 2024 00:08:56 GMT  
		Size: 224.7 MB (224700849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:802aca163686fc799fb1a83ec8695f1b45fb2d5b752a5a0584743c3be3b82a0d
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
$ docker pull buildpack-deps@sha256:caad2aca24ca403a1973910e2f4791f36b7b3e5fb425af6a7770bd22e9d221f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76600977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd25a8ea97d2b2f86521600ddb5e57db254046cacca05377c30858cfb434fb0b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cde303353e0557e4632fe6d4d3b1903636b16ed4c2f0dd2efdfde0c49154af97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72590238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099267525a60ae8269b784db17b8d89fc4883cbb22c185e879571bef8b17c008`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bb08393ddc9172f1653daee17542d08cfc7f31b1408c85caafcf52c575dacda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69422843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9ac916505f84bfb509eb3477762a21c71698e5f1db222611903011b9f4437d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13c28b84072c7e9d0bbb7ae510977c4d4e0747b52c234125f78d1b0aa91b20c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76206390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed51ceb4392ad24e0551894887ea30ccfd611cb6440074a774b34a4e8c6e1812`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cda0b4ed2c65d325d0edf15b4d5e8459bef2d4f5a27a1a8bd4d71cdf281e16b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78567250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13648a0fda94cb4145326f4037c8a9e7272bba5fe7754a9f298e9c2e5c1fadaa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:72e4be73652e8dc05458a7b54e9e9a1d8dcb15e658eda60002b5eb0a590beebd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76152427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b14909d446d42857d16c65a888f02ae7df059ba4b435fc88fa7069cd1fd2ef8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44b879235275c23ac4ea8f634435b73cdfbed488c37f0b59f1863bb04790b8c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82654894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ee2989f40b8bf1d782733ee67a4d51f809eacb777913582e8a8d508df5aa0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bec0eb25faa85054bdacab8da9d9d50138c42aaa16df08715df2110d680cf979
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74482043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f100f56d88dba8d99909f4819951fbde0a33ce797e908064862c52abc53caf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22fde5fa3d322988856886c94d2da0c1dac1261effb3d5190e99883ecb3cad86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77198834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c741e0d6341ca4ad452547e9ef78adcc34894e284d00885f03ddac549222022`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:3e3707db6ce77a6240faf371c5d47bdb0f29ac3945fcfae3d9e5b174f7e9f0a4
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
$ docker pull buildpack-deps@sha256:6d6ba19df7ac34deaee2837c9989349bb222d5d8cd772c2eb08090a05b0404f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142722649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ee1b47cac952c9c05aa200b7d527b77f84c37804e50850b0d411f7b6d7b228`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da143e0f6d9787b0c89d6405a787ded9de6dcb65f3b9717f82da42f10ff997b6`  
		Last Modified: Sat, 30 Mar 2024 21:42:57 GMT  
		Size: 66.1 MB (66121672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29601816820e241abcad249b8e1c5a56b3c72320d3b1a09eee2f799a79570a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136438764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b05cb0813a14a71549c9b53c6ba587e924600042dbe0f5f87e324681afbaa0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb3d107ad7b8f22e25af7c2ea21540943257d714d5f5258c8275e541fd460cc`  
		Last Modified: Sat, 30 Mar 2024 21:20:04 GMT  
		Size: 63.8 MB (63848526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bcf0e6e53f87bdf060fe92e1ff43af0edfdcecdc7bf80642f4326d6c365ec6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130674564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3603e38a05a3732f16f7345c6d4a212bca05335fd34aa151adf86be572361f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba4b082de66bbca9897c8dba7f31512bba321ddd2a661347d670d910b4ef36`  
		Last Modified: Sat, 30 Mar 2024 21:30:50 GMT  
		Size: 61.3 MB (61251721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:960984f241bafb16c55235d8db73ba936e37461f733feb0b34fc2404c582b330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142537555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9dd4442662661fd0376972d939bfb99b7a961420e5af377a404911e9f4a1735`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544cbfb4f7236143d102b4ef349f35d3d31527535f242406bbfd2d42dbfe60ee`  
		Last Modified: Sat, 30 Mar 2024 21:43:05 GMT  
		Size: 66.3 MB (66331165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d18fa777ebc7ea2e073e4bffda4c47de7132dd54b9fd9b1e58690f087de5d3a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146443487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b170d882dbbd60c1068d13fd4cadcf7e8399258e2290a48999a461dd9f1ca2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a15da4ef836ff60f9c28ef8b15ef8794d788a67c0a3d58b61d51a0e65213a7`  
		Last Modified: Sat, 30 Mar 2024 21:21:45 GMT  
		Size: 67.9 MB (67876237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6c77a5529a0384f610cc4238b7086ad705e14f1fc79c382bfafca81d6c957a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41ad8fc978f8d2925c94540c6b5928f5e0e55c43ab6d99a9e02b26e17a9b10b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f503a33191cf930c854f6db9bbbb4869ccbec7ff1c51ddc9f7c6a23aa26244a4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154344195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cad6e11ebc7819d06808e304fd24f559ffdd6df84c9f1b35094beb99311b6c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95220faf903de5c246bc60d7f00054712c075484056449785d59c657e22436e`  
		Last Modified: Sat, 30 Mar 2024 21:45:39 GMT  
		Size: 71.7 MB (71689301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3b84dd2e51c1d7bc38652a613a744353040ea2ab821b910ff694e3a1e13943c3
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140088921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9abff9aede153fe1ede007e697504da2ac4f742d4f9c5e8afd4ee1f6da6a91`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259a8b8d1c2e3af16628db8608e828fa16ec2c3aadfd7660f4716db301738d6b`  
		Last Modified: Sat, 30 Mar 2024 21:28:40 GMT  
		Size: 65.6 MB (65606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:58058792dbb38618b64512a4f523c0e2e7ea9bd12447bb2555e85a21fc99e831
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144622282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b467bd594b194ed628a97ca9f35ace2f08eff7d03179e6bb58a3f0701ebfee5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8b2bab401823952dea39f0a278dd656c849280f02e7b6f21ca4deddc0219d`  
		Last Modified: Sun, 31 Mar 2024 00:08:23 GMT  
		Size: 67.4 MB (67423448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:33fd523e6d918b2d066038992f814ff881eb6de323d3c70b7fea851ed1c36be0
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
$ docker pull buildpack-deps@sha256:db9fa21724f9ed2ea02b2b5ece7b9b33c539c1bc812e1f576c88854470db0c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348878735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a3793f3c6079a0170f05599f2735b64766d39d2c34374471d3bcc6ca540d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:54:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567db630df8d441ffe43e050ede26996c87e3b33c99f79d4fba0bf6b7ffa0213`  
		Last Modified: Tue, 12 Mar 2024 06:03:18 GMT  
		Size: 211.1 MB (211139445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:091d6742817a9012801ddba3c88d22130da8ec2a52a82fdab424cadb8c02672f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316009389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d577d2712bb80823634647f21b499b3b5950339ba80b463b1d5ec39552739bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:35:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9069b8edc3144ea7c7fba8c956dedcc448fc0ba006a12c9cfe4ac23f05569d`  
		Last Modified: Tue, 12 Mar 2024 01:44:12 GMT  
		Size: 184.5 MB (184456518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1919befcfca67d8372abe16832d32831608044d6022238cb362f0ad8296441a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301423265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c58b41f8b222deb6863d767951930f9431b526720e771a43ecb9c74e996cac2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:236f29b4631548c327b2d1d0590ef8011bff534a87f62bfa2a68a91f8d8c3c02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339703020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02567629c9e9c4dc92672656620fd7750ba05eb4c4fa2d86a63ac92419d2dbe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c418b37b4bcde3a68933365b172d45ae5f3b046050fde08b6eeca5d57994a08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351512027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f67448ff33c81527caf039ca97b379daa5a4deb989b5d2bba32c70ec9a07deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:41:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee485e7c553f7b1465ed88918f0904a411af3dbb0918703ec7b92192eda6417e`  
		Last Modified: Tue, 12 Mar 2024 07:54:34 GMT  
		Size: 210.1 MB (210058424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3e131fedd6c0a053f4d92db50d59e106405e5047e2b38db2db93bd1cbf4dc08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325858634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9827aaea1a13889e5939e08ab8f7c05be47b277bcb8f5da059cec0ab3b14c450`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02977c85a258d317066e5a1e6febc79a4caa2a830ee66f596c866db50d3361d7`  
		Last Modified: Tue, 12 Mar 2024 02:44:46 GMT  
		Size: 189.7 MB (189698984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d82d41cabf8e17cd142de9f607e0fa1c803e30fc7c1c11702fe2eff44af1d4c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363009215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6db4fb9bf6b421d4aadfcc2a56b963ee8771a5c2e2813078cc1e73b7a33733b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d9053a0f750316634df779ba70e4b32f8618c06678f58ba3e14bdbd7ec4d444
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0947a371e12fd46d0e731838049ffbbc92492031782ffcf22ec58497a4e57efd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6654b38164df76c1496278c128a09a6fc9ea1d703322ccb6eb98f578047b2b07`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 183.2 MB (183164991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:da13a0b5c77dc3e752cc9d9e185b9c09f2e2064d8e11218ffca5a57406a10bfc
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
$ docker pull buildpack-deps@sha256:cc05c08ca39e926630564a43219ac19163c7e528389960d2fe9e639025638618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c215ffce5e7490aba71d8dabf58ef741bced74521af2c5f27869e888e3d95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0240b8998a2b49677c6ca0a32e10689d5c0117ba74d967e8a6d98fe7a4ae3fa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70037013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca62b11afe7a8431a7e12380500c7c2eb46286dde03a2bf7cf121cb6e7d10708`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b872e7fd396a6833da36a5ef61e35ffddcffce622e76d99cd704ed9bc2bb9c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff330e85d6b2d9a434a86e0c5df03f2fc83d2d5fd31e47532edcdd9512873898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48cec1cd7e892dc51c4f2d7516b2ed8f391e116929b5460e3ae0c976ed050693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ea96e7d1339ff33f942f8cc1315e0731121520bcbfac53669df4bb05c253fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7bfebc01b0982fb9874fe5bc61cb62bf8dba226d5fa3477f593bdad7502621f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7410bad07bb558d5fe093b6a01893c3a2b26334e114a68a3644836299bf37f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b18588551c4d881828aa5f3317b0536cc51d3663c096fa4d1ff409b1a7837e4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a9c2db66277195f38df723d4eaf40817c0a38943d94badc968e39f17f98be7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9d2e59a230a9d4a04808ae004745f51e0e596953a2770503084886a3fb23f2e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79253819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5a24d3eb15d8f3b9ef6a936bb7a9d5b7a210c0779c7b2bbfc59ae6e0e14774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:95b1f86365edd875e362c6d47e79763e1f3b7504f29992ff6abf68cefbf731c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71960165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b776a30a72031edeaea3d61789f2250d8181bfb7503c9857a93cb931e569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:2c0c1638d1e037a1ab747f02c39b7e54fff548be0fe6f230a28c2b8301fbd20d
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
$ docker pull buildpack-deps@sha256:25f20fd3e3c8be1e9626c246986beb400ccfe19b0ab13d57127399927801d499
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3829553ca241eb6ec827e514210faab2db77d5f4a58764d0dd5a00f97f4a049`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4604b8d280097513158cce324d296dd8806f21056e09f659b28c7a0b236cc7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f5e6d0ea8c878fb6e49c35a11089dc2a50afecb3abe7942942297679e212bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cfb748d851e2e3cfdcbc1be1e1817fd84e8fff94498702a724beb1ed87b168ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126317289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2a90a637715c3c6bb9034dbf6c64f7ea86758a8c52109f24996208cf4d832d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd1553434a26aadad218bb6dacdecbc747db860969aaa45222d479b12c9fcdb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137164774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81cdaeb1cfb57a71b96eb9e0a8673ffde7936b504bd716ede73f435391fd8db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:651ed01e0f955ed10779074376f6fe0ecb8fe43cd832988c176b5c4fe3d8f4dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141453603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7e7c3092c37a6e5c2b8d528da777020e5b3d0cb69c67d216649c3d7c239f87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4ad06509257def2a4df2513623de0665e807666f3c0d942042e3228e12ab49d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136159650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d33af04fbcfe6b33eccfc1638aa0f25b79423288344805b88451266aa3eb56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9b03894e8f0ddcd1ee80a6112c6aab6e27a3532fbcae3e272cac191218353386
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148835718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f9a694cfc75a976c7f54142f0a5c4745f9d4f2a0ae27d4a673a3987c4888b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:793d4d8f8b9efc430bada65e9066cf9215dc96b03c605ae45dbaa4fb24ad830b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135086824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329d23986398ef8817d6d027b58b5b6edab632660cf8b81c3092f5ffe0a77816`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:df736553217d7d4565f1f68381efc814ad6fa6c7dd5db7305e4f8b61690d8fe2
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
$ docker pull buildpack-deps@sha256:9334e7f8e54002a8070c2fdee57e644722cef7732be2e6fc58deb05f18aa0a5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407197649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd6e9445ce815823bd61f82d8ccac60f8042376e7245a561d54e52d5d405da5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:41:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ed217077cbab3a8045ced4bde7cf8f18ce1f44772f12fd815426ba986a514`  
		Last Modified: Sat, 30 Mar 2024 21:44:05 GMT  
		Size: 66.5 MB (66494478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7eea01bdc93a861a285a81f2c756e9f3ccf57cb8b8ccd4798ec342ebcb9a62`  
		Last Modified: Sat, 30 Mar 2024 21:44:46 GMT  
		Size: 264.2 MB (264209773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7b71cbcc42810d84831d60bea49483cf40bbab2aff46e9cd943236ac4b8db310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.4 MB (370378903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6322db07d9c36437546abbf50de40d76d29b2d83fa4cb4e34c3790883f4e95`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b58fc48be57cf2d13ee9a032f9a12e78a89d4e920b01edfc3db1a2244d6fefc`  
		Last Modified: Sat, 30 Mar 2024 21:21:12 GMT  
		Size: 64.1 MB (64140486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445cd06d91c5d1a2a9f126d50bee6e679ebdb26057a5f28219241292718ee494`  
		Last Modified: Sat, 30 Mar 2024 21:21:54 GMT  
		Size: 233.8 MB (233774772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe328d3acf2b3a1a04177df6e3646804a9c723702f41246f2c2fa94c7e6b251f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348835489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e28be6a8566ffe770a5445f44f18fb23f396f27b864c9026e51f6e931967929`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9c6e3e6ce96fb41f02f466b843d37cc564ba933de9a8c733b54cc9095a60c0`  
		Last Modified: Sat, 30 Mar 2024 21:31:53 GMT  
		Size: 61.5 MB (61505430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0848461b9b4785f45b667a3db634a643e594beab111e48a523e8e61699cf6d4`  
		Last Modified: Sat, 30 Mar 2024 21:32:30 GMT  
		Size: 218.1 MB (218054484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:867aaa4ab22ba052d88db8b522b581ad4cd589b888306220e9c07e029e20dfa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 MB (395134887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356997e63ecd3ba0ab0879397732b031cb0cb914ef40f6fa2b36a648561ec3d6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63caa9a5413155875f8588f11232551811490c971f44ce81eb5af6b6772a02`  
		Last Modified: Sat, 30 Mar 2024 21:44:03 GMT  
		Size: 66.6 MB (66608728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c83fe45b997bce88c47d9729781159dd266d8ee3061ff664a1ea61ae7a99836`  
		Last Modified: Sat, 30 Mar 2024 21:44:35 GMT  
		Size: 252.5 MB (252453989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b2ad1b73972958501ce343e89c50cce82100bae16b76b6bc5ef5b1aff64a0b7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 MB (403686311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34d9f9875407c704830efd5253be522bdd79b77702e7fc776a1574f903e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313f7d227590d173c7c917355cd9f941004d00a942880bbeb46db2d83afb99a`  
		Last Modified: Sat, 30 Mar 2024 21:24:18 GMT  
		Size: 256.9 MB (256934564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f03e178c9abf4112b3462aca11b751002244d4290ceb7c13be55fc086d3cda06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374054854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375690a33878b671637de5260b41fbf3653065bc084c04483f0c1aa4b3304065`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:45:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6e7309cbb19498b04d6ce239394888a75868da207aba050aad04cb90d117d3`  
		Last Modified: Sat, 30 Mar 2024 21:53:10 GMT  
		Size: 232.7 MB (232721406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b6a4bafac2ba0b871a1f18bbb27dddfb9a0a953676d504d3fb63ebfe71fb018e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417935469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c74e473a6533b08cb81ca0078daf0be3d6bc8863752d6f85ce9fa2a46466c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28cc0d4e61b8cd8c7b7e7f0f32f02fdf18eeb78863a40518a35ae1fa157877`  
		Last Modified: Sat, 30 Mar 2024 21:46:59 GMT  
		Size: 72.0 MB (71999507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2009a081181198024762b32de41b803175d353b112711a89807dd88ce6533ffd`  
		Last Modified: Sat, 30 Mar 2024 21:47:47 GMT  
		Size: 263.4 MB (263430071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c8ce9d22b81b531b84fcd0053c1764223025ee0237517271d259d5cc0b334754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385391050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557450db20d19e4286d71e7df5a0cbcbcd96ed024ed60dbab7ec653d2c8d0bf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:50:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd869558e192852f59615a3c48ccbd98eb100935a473d9f83c786dfc340d8877`  
		Last Modified: Sun, 31 Mar 2024 00:09:19 GMT  
		Size: 67.6 MB (67586886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac5abf6bb25592cd6dcd1e039eb244572ed2262313de81026bd18e4ea9078e6`  
		Last Modified: Sun, 31 Mar 2024 00:09:54 GMT  
		Size: 240.7 MB (240745154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:78a5d03a75eeb1b23ac97399418913fef5d68518d331167ca35d3e304f9d95e0
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
$ docker pull buildpack-deps@sha256:002da05f9df97b31ef836b483a61ed01d3331ed704492ee4af14d639e70063bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76493398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94047d7f8b431825db72b9fb121c25b457aa8636d32cbe8294d878a5142ab1db`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7fbfa81d59aac0db3ce9fc149b2457cbad7de0c2a4b87c62b9a1322efc1316a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72463645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d657f7569f9296996cb49331191c85a53b0ff696831458f2abd425216f4ee64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e2e75a10eb04172119c721e9cfdb6c6dd68fcccaa2f72a7500e10ece8d5ef33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69275575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22849dd906c5988b8dbecb1128db23dcdb6bc204c546d5dfcc9c7f202c36720b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:316e1fa8a278128ad74632d6c2644dea76ab06f0478bbb6bc10e2b7da5bffee0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76072170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490610d0fdef66fd582ebd89efbdbfa1f998860955e5be3e5ea5ac9237ae53b1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ade99aca5a25a9ccd47b950d25bce57189ae06309fec207a419bd20d9204481e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78464402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7140bd1b11c3401b355ccc13586f05f2d2fb3e2ec6fbf6f177c608da01b21968`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:363c0c44809b184ca8136ce186fb7b835d52282b57b2a32140cf8abaadb7c521
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76035641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2592a789f614b82ffe8267610de4d3d39c0e9172725f22ab8e5a3624e774be9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9ef7db1d4a6348f18c0d9380d0ca7dfd813434858666fc4eb03ff5eceeb9042b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82505891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6eb67d19e8d3ea6600b0e12284439dcb5958712689cf4f73250cd97c1a2b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:19034a5338fd96d04bd7529abcf0f394bd8b800c890cd17a9d3ce98d0bee89d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a2b86de9c8bc1032b3d9b9215615dd8a09899205abedf77dc87438f77837db`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:92344e18bfedf4eb6883bd71608f576744493d0120e6b895a5fb19f148a79942
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
$ docker pull buildpack-deps@sha256:a74cdbcbd2e4fb8989e9f0659c3fe7c4693daddf5db31a4336d0a9fff7eba5e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142987876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129adc2f7a72789a1a148218ecde13379a552586ced05b0690a00e7c0044a5c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ed217077cbab3a8045ced4bde7cf8f18ce1f44772f12fd815426ba986a514`  
		Last Modified: Sat, 30 Mar 2024 21:44:05 GMT  
		Size: 66.5 MB (66494478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9b202e18370d0b5daf6bd65fdc74b44b9a2beb387dc604e7bf5821079d6ffec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136604131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8096fadd752766e37c0a8eb7436d3abe284d061067230813d29eef0c77c0e187`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b58fc48be57cf2d13ee9a032f9a12e78a89d4e920b01edfc3db1a2244d6fefc`  
		Last Modified: Sat, 30 Mar 2024 21:21:12 GMT  
		Size: 64.1 MB (64140486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:403c95b800e81f8ff214e7b174678a3118cf703b5e9387d66a18e6687dab8d0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130781005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b1d0a45b7c1d0c6284b797e4d6b8c1a10b952b1ee863865c90d0139903aab0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9c6e3e6ce96fb41f02f466b843d37cc564ba933de9a8c733b54cc9095a60c0`  
		Last Modified: Sat, 30 Mar 2024 21:31:53 GMT  
		Size: 61.5 MB (61505430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5a7ba798a132371c9edf1e2136941f258449624e822eb1f7786329a20188cdaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142680898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a220d37191ad7fda6b47cb01ba0b5fda60e218f8b4d53d61c2fb469851490427`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63caa9a5413155875f8588f11232551811490c971f44ce81eb5af6b6772a02`  
		Last Modified: Sat, 30 Mar 2024 21:44:03 GMT  
		Size: 66.6 MB (66608728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eed184f7c0a8d3c5614a63902094e8b29d82dbaea4e9710e2591b9c3cfad513d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146751747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e487430056e803e7f442fafda3fb9030b67eca8226babf68a2a3e8ca55ed5ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:073778b7037e665c7deb59a4f06a254c6be933587f8fb58d705794a27a93e25d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141333448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db4c0353943ea80b7ba5e735727b8a5c912807d88ac7d1804205b190897140`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7383cc117938cb6effde90e11e6a0d3577d03642e71279f2df4f6984eb702d9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154505398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fefcf5e1fd141eea29c1f426e1a805d63a2fb2ad983912acb4204dee42e05e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28cc0d4e61b8cd8c7b7e7f0f32f02fdf18eeb78863a40518a35ae1fa157877`  
		Last Modified: Sat, 30 Mar 2024 21:46:59 GMT  
		Size: 72.0 MB (71999507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8cda0d5b06506102f3bd891eb29b3e594fc31a87844b0f14e79e37a17ac456bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144645896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5dbaf2f60d35f24fc959bb3f226720c2d708c20e3b5636f955bab0408b240a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd869558e192852f59615a3c48ccbd98eb100935a473d9f83c786dfc340d8877`  
		Last Modified: Sun, 31 Mar 2024 00:09:19 GMT  
		Size: 67.6 MB (67586886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:df736553217d7d4565f1f68381efc814ad6fa6c7dd5db7305e4f8b61690d8fe2
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
$ docker pull buildpack-deps@sha256:9334e7f8e54002a8070c2fdee57e644722cef7732be2e6fc58deb05f18aa0a5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407197649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd6e9445ce815823bd61f82d8ccac60f8042376e7245a561d54e52d5d405da5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:41:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ed217077cbab3a8045ced4bde7cf8f18ce1f44772f12fd815426ba986a514`  
		Last Modified: Sat, 30 Mar 2024 21:44:05 GMT  
		Size: 66.5 MB (66494478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7eea01bdc93a861a285a81f2c756e9f3ccf57cb8b8ccd4798ec342ebcb9a62`  
		Last Modified: Sat, 30 Mar 2024 21:44:46 GMT  
		Size: 264.2 MB (264209773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7b71cbcc42810d84831d60bea49483cf40bbab2aff46e9cd943236ac4b8db310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.4 MB (370378903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6322db07d9c36437546abbf50de40d76d29b2d83fa4cb4e34c3790883f4e95`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b58fc48be57cf2d13ee9a032f9a12e78a89d4e920b01edfc3db1a2244d6fefc`  
		Last Modified: Sat, 30 Mar 2024 21:21:12 GMT  
		Size: 64.1 MB (64140486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445cd06d91c5d1a2a9f126d50bee6e679ebdb26057a5f28219241292718ee494`  
		Last Modified: Sat, 30 Mar 2024 21:21:54 GMT  
		Size: 233.8 MB (233774772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe328d3acf2b3a1a04177df6e3646804a9c723702f41246f2c2fa94c7e6b251f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348835489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e28be6a8566ffe770a5445f44f18fb23f396f27b864c9026e51f6e931967929`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9c6e3e6ce96fb41f02f466b843d37cc564ba933de9a8c733b54cc9095a60c0`  
		Last Modified: Sat, 30 Mar 2024 21:31:53 GMT  
		Size: 61.5 MB (61505430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0848461b9b4785f45b667a3db634a643e594beab111e48a523e8e61699cf6d4`  
		Last Modified: Sat, 30 Mar 2024 21:32:30 GMT  
		Size: 218.1 MB (218054484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:867aaa4ab22ba052d88db8b522b581ad4cd589b888306220e9c07e029e20dfa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 MB (395134887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356997e63ecd3ba0ab0879397732b031cb0cb914ef40f6fa2b36a648561ec3d6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63caa9a5413155875f8588f11232551811490c971f44ce81eb5af6b6772a02`  
		Last Modified: Sat, 30 Mar 2024 21:44:03 GMT  
		Size: 66.6 MB (66608728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c83fe45b997bce88c47d9729781159dd266d8ee3061ff664a1ea61ae7a99836`  
		Last Modified: Sat, 30 Mar 2024 21:44:35 GMT  
		Size: 252.5 MB (252453989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b2ad1b73972958501ce343e89c50cce82100bae16b76b6bc5ef5b1aff64a0b7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 MB (403686311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34d9f9875407c704830efd5253be522bdd79b77702e7fc776a1574f903e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313f7d227590d173c7c917355cd9f941004d00a942880bbeb46db2d83afb99a`  
		Last Modified: Sat, 30 Mar 2024 21:24:18 GMT  
		Size: 256.9 MB (256934564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f03e178c9abf4112b3462aca11b751002244d4290ceb7c13be55fc086d3cda06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374054854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375690a33878b671637de5260b41fbf3653065bc084c04483f0c1aa4b3304065`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:45:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6e7309cbb19498b04d6ce239394888a75868da207aba050aad04cb90d117d3`  
		Last Modified: Sat, 30 Mar 2024 21:53:10 GMT  
		Size: 232.7 MB (232721406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b6a4bafac2ba0b871a1f18bbb27dddfb9a0a953676d504d3fb63ebfe71fb018e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417935469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c74e473a6533b08cb81ca0078daf0be3d6bc8863752d6f85ce9fa2a46466c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28cc0d4e61b8cd8c7b7e7f0f32f02fdf18eeb78863a40518a35ae1fa157877`  
		Last Modified: Sat, 30 Mar 2024 21:46:59 GMT  
		Size: 72.0 MB (71999507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2009a081181198024762b32de41b803175d353b112711a89807dd88ce6533ffd`  
		Last Modified: Sat, 30 Mar 2024 21:47:47 GMT  
		Size: 263.4 MB (263430071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c8ce9d22b81b531b84fcd0053c1764223025ee0237517271d259d5cc0b334754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385391050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557450db20d19e4286d71e7df5a0cbcbcd96ed024ed60dbab7ec653d2c8d0bf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:50:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd869558e192852f59615a3c48ccbd98eb100935a473d9f83c786dfc340d8877`  
		Last Modified: Sun, 31 Mar 2024 00:09:19 GMT  
		Size: 67.6 MB (67586886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac5abf6bb25592cd6dcd1e039eb244572ed2262313de81026bd18e4ea9078e6`  
		Last Modified: Sun, 31 Mar 2024 00:09:54 GMT  
		Size: 240.7 MB (240745154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:78a5d03a75eeb1b23ac97399418913fef5d68518d331167ca35d3e304f9d95e0
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
$ docker pull buildpack-deps@sha256:002da05f9df97b31ef836b483a61ed01d3331ed704492ee4af14d639e70063bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76493398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94047d7f8b431825db72b9fb121c25b457aa8636d32cbe8294d878a5142ab1db`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7fbfa81d59aac0db3ce9fc149b2457cbad7de0c2a4b87c62b9a1322efc1316a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72463645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d657f7569f9296996cb49331191c85a53b0ff696831458f2abd425216f4ee64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e2e75a10eb04172119c721e9cfdb6c6dd68fcccaa2f72a7500e10ece8d5ef33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69275575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22849dd906c5988b8dbecb1128db23dcdb6bc204c546d5dfcc9c7f202c36720b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:316e1fa8a278128ad74632d6c2644dea76ab06f0478bbb6bc10e2b7da5bffee0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76072170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490610d0fdef66fd582ebd89efbdbfa1f998860955e5be3e5ea5ac9237ae53b1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ade99aca5a25a9ccd47b950d25bce57189ae06309fec207a419bd20d9204481e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78464402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7140bd1b11c3401b355ccc13586f05f2d2fb3e2ec6fbf6f177c608da01b21968`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:363c0c44809b184ca8136ce186fb7b835d52282b57b2a32140cf8abaadb7c521
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76035641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2592a789f614b82ffe8267610de4d3d39c0e9172725f22ab8e5a3624e774be9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9ef7db1d4a6348f18c0d9380d0ca7dfd813434858666fc4eb03ff5eceeb9042b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82505891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6eb67d19e8d3ea6600b0e12284439dcb5958712689cf4f73250cd97c1a2b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:19034a5338fd96d04bd7529abcf0f394bd8b800c890cd17a9d3ce98d0bee89d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a2b86de9c8bc1032b3d9b9215615dd8a09899205abedf77dc87438f77837db`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:92344e18bfedf4eb6883bd71608f576744493d0120e6b895a5fb19f148a79942
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
$ docker pull buildpack-deps@sha256:a74cdbcbd2e4fb8989e9f0659c3fe7c4693daddf5db31a4336d0a9fff7eba5e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142987876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129adc2f7a72789a1a148218ecde13379a552586ced05b0690a00e7c0044a5c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ed217077cbab3a8045ced4bde7cf8f18ce1f44772f12fd815426ba986a514`  
		Last Modified: Sat, 30 Mar 2024 21:44:05 GMT  
		Size: 66.5 MB (66494478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9b202e18370d0b5daf6bd65fdc74b44b9a2beb387dc604e7bf5821079d6ffec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136604131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8096fadd752766e37c0a8eb7436d3abe284d061067230813d29eef0c77c0e187`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b58fc48be57cf2d13ee9a032f9a12e78a89d4e920b01edfc3db1a2244d6fefc`  
		Last Modified: Sat, 30 Mar 2024 21:21:12 GMT  
		Size: 64.1 MB (64140486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:403c95b800e81f8ff214e7b174678a3118cf703b5e9387d66a18e6687dab8d0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130781005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b1d0a45b7c1d0c6284b797e4d6b8c1a10b952b1ee863865c90d0139903aab0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9c6e3e6ce96fb41f02f466b843d37cc564ba933de9a8c733b54cc9095a60c0`  
		Last Modified: Sat, 30 Mar 2024 21:31:53 GMT  
		Size: 61.5 MB (61505430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5a7ba798a132371c9edf1e2136941f258449624e822eb1f7786329a20188cdaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142680898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a220d37191ad7fda6b47cb01ba0b5fda60e218f8b4d53d61c2fb469851490427`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63caa9a5413155875f8588f11232551811490c971f44ce81eb5af6b6772a02`  
		Last Modified: Sat, 30 Mar 2024 21:44:03 GMT  
		Size: 66.6 MB (66608728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eed184f7c0a8d3c5614a63902094e8b29d82dbaea4e9710e2591b9c3cfad513d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146751747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e487430056e803e7f442fafda3fb9030b67eca8226babf68a2a3e8ca55ed5ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:073778b7037e665c7deb59a4f06a254c6be933587f8fb58d705794a27a93e25d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141333448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db4c0353943ea80b7ba5e735727b8a5c912807d88ac7d1804205b190897140`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7383cc117938cb6effde90e11e6a0d3577d03642e71279f2df4f6984eb702d9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154505398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fefcf5e1fd141eea29c1f426e1a805d63a2fb2ad983912acb4204dee42e05e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28cc0d4e61b8cd8c7b7e7f0f32f02fdf18eeb78863a40518a35ae1fa157877`  
		Last Modified: Sat, 30 Mar 2024 21:46:59 GMT  
		Size: 72.0 MB (71999507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8cda0d5b06506102f3bd891eb29b3e594fc31a87844b0f14e79e37a17ac456bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144645896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5dbaf2f60d35f24fc959bb3f226720c2d708c20e3b5636f955bab0408b240a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd869558e192852f59615a3c48ccbd98eb100935a473d9f83c786dfc340d8877`  
		Last Modified: Sun, 31 Mar 2024 00:09:19 GMT  
		Size: 67.6 MB (67586886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:0658bee092d2e837c5020aa7effee407a2c7b3bbc59cf1da6235c482ce4382a7
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
$ docker pull buildpack-deps@sha256:57ac383c326ff712bab6fd9b199d44510599a4e0281a3aaca37b8586d45a2223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.0 MB (387988231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43d2453de4fe2fb28496f33f2180811f598511875812a4066bea677fb343dd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:39:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da143e0f6d9787b0c89d6405a787ded9de6dcb65f3b9717f82da42f10ff997b6`  
		Last Modified: Sat, 30 Mar 2024 21:42:57 GMT  
		Size: 66.1 MB (66121672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c86b463be435223351150e682274c024736e2d18e8692edb2df9fdbbc0c419`  
		Last Modified: Sat, 30 Mar 2024 21:43:36 GMT  
		Size: 245.3 MB (245265582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:17bc4bd22190703d8768aeaa3ca6bcd2210fc641746d2454585be08ce56549bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349646719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614f6de95aa626bece07ebe03b846284624db6354ec954386925ca06485d0083`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb3d107ad7b8f22e25af7c2ea21540943257d714d5f5258c8275e541fd460cc`  
		Last Modified: Sat, 30 Mar 2024 21:20:04 GMT  
		Size: 63.8 MB (63848526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8556d6df8b94862fc63dfac7c0bcbae4ab10302c1f9ef0b871b8fafd147bd6`  
		Last Modified: Sat, 30 Mar 2024 21:20:42 GMT  
		Size: 213.2 MB (213207955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:871e0f29584780024f2204c980284b9c9391fec747286a83190d491d200a6814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332812461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee2aec038450d0cf24a4e37e4f23eda53bb149657b4ce73450749cff557bbe8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba4b082de66bbca9897c8dba7f31512bba321ddd2a661347d670d910b4ef36`  
		Last Modified: Sat, 30 Mar 2024 21:30:50 GMT  
		Size: 61.3 MB (61251721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9506c1ec3f4d514c50744f383e5d6be73cb1ec6ad9ff611f2f6c6044f529c896`  
		Last Modified: Sat, 30 Mar 2024 21:31:25 GMT  
		Size: 202.1 MB (202137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8fdce59c69a1449570ad7e28d7d6a3c93d6d22fa193133eeb50a19328c2ba05f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378477580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1747b554c7d67544ddafb675e6be262cebdf69160ca27b8626bdee79cab5a26f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:39:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544cbfb4f7236143d102b4ef349f35d3d31527535f242406bbfd2d42dbfe60ee`  
		Last Modified: Sat, 30 Mar 2024 21:43:05 GMT  
		Size: 66.3 MB (66331165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c307077e7d76abcb4bd4d45c8ace8d03bf5ecdf42e3cc300d9004aa74bbf1a`  
		Last Modified: Sat, 30 Mar 2024 21:43:36 GMT  
		Size: 235.9 MB (235940025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:54905ffedef969cc2e213a1e9a0fada1fc515acd5d1f63592aaf3178675e51bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387860877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fdfccb3460ac7002fa33cef8001a4588dbfc8aa65b902e39c6fb38fd8f1ecb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a15da4ef836ff60f9c28ef8b15ef8794d788a67c0a3d58b61d51a0e65213a7`  
		Last Modified: Sat, 30 Mar 2024 21:21:45 GMT  
		Size: 67.9 MB (67876237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51302bc05c4c173523b513edf1b3957871cd4387ae1b1a565c5bd4a3eddb7c6c`  
		Last Modified: Sat, 30 Mar 2024 21:22:41 GMT  
		Size: 241.4 MB (241417390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b5224f59c01c64b248e9f48214432ae69669ab3e3bbe2f36a4412b60b58e4fdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357495125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3615639b43b8508a560b974f0f2c8153011ac54069af729c882ebd1149beda34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec5d517bc6924cab27f5df1f01979046acdf9cdb844cd5281549ae70cffd261`  
		Last Modified: Sat, 30 Mar 2024 21:49:28 GMT  
		Size: 216.2 MB (216190767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ec624754a8b69473cb9b81413a4b282e6cb28ba8f672f0e5a99247b21d660ebd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401680790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb5830486e828fd2cec3b7fe5910b5925f3d26950aa5db6ee446be40af0f264`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95220faf903de5c246bc60d7f00054712c075484056449785d59c657e22436e`  
		Last Modified: Sat, 30 Mar 2024 21:45:39 GMT  
		Size: 71.7 MB (71689301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d202211364551a66c5bdc24a551df53c88b1d009232162339febb791ddf65fb7`  
		Last Modified: Sat, 30 Mar 2024 21:46:26 GMT  
		Size: 247.3 MB (247336595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b8c90681410c7a219fb7f7d04aa57e2cf52f01af353243fb0b0f43a1e8e4a827
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (420983437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2f4a3271f92c24c8642e98dae057607e7c994185921ee91f6a528279ae0b81`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:26:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259a8b8d1c2e3af16628db8608e828fa16ec2c3aadfd7660f4716db301738d6b`  
		Last Modified: Sat, 30 Mar 2024 21:28:40 GMT  
		Size: 65.6 MB (65606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0b2e0b74b3f4b89240082a552a105f36e18ee01936ae286a1f1b860dc7521`  
		Last Modified: Sat, 30 Mar 2024 21:33:41 GMT  
		Size: 280.9 MB (280894516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4bb0ce013670aae1801c1a36a4458da7b41a079951d7d46f758813926a26f386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369323131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92206efd704f5b1ef33db0289e2f80885e1e5e85e0ce41ca5c64eb7acc42547`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:45:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8b2bab401823952dea39f0a278dd656c849280f02e7b6f21ca4deddc0219d`  
		Last Modified: Sun, 31 Mar 2024 00:08:23 GMT  
		Size: 67.4 MB (67423448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1739ba0e83442ddf7c0d49fb3fe672de89ffe6650ed119a9a2c0737076f8c316`  
		Last Modified: Sun, 31 Mar 2024 00:08:56 GMT  
		Size: 224.7 MB (224700849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:802aca163686fc799fb1a83ec8695f1b45fb2d5b752a5a0584743c3be3b82a0d
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
$ docker pull buildpack-deps@sha256:caad2aca24ca403a1973910e2f4791f36b7b3e5fb425af6a7770bd22e9d221f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76600977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd25a8ea97d2b2f86521600ddb5e57db254046cacca05377c30858cfb434fb0b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cde303353e0557e4632fe6d4d3b1903636b16ed4c2f0dd2efdfde0c49154af97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72590238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099267525a60ae8269b784db17b8d89fc4883cbb22c185e879571bef8b17c008`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bb08393ddc9172f1653daee17542d08cfc7f31b1408c85caafcf52c575dacda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69422843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9ac916505f84bfb509eb3477762a21c71698e5f1db222611903011b9f4437d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13c28b84072c7e9d0bbb7ae510977c4d4e0747b52c234125f78d1b0aa91b20c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76206390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed51ceb4392ad24e0551894887ea30ccfd611cb6440074a774b34a4e8c6e1812`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cda0b4ed2c65d325d0edf15b4d5e8459bef2d4f5a27a1a8bd4d71cdf281e16b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78567250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13648a0fda94cb4145326f4037c8a9e7272bba5fe7754a9f298e9c2e5c1fadaa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:72e4be73652e8dc05458a7b54e9e9a1d8dcb15e658eda60002b5eb0a590beebd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76152427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b14909d446d42857d16c65a888f02ae7df059ba4b435fc88fa7069cd1fd2ef8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44b879235275c23ac4ea8f634435b73cdfbed488c37f0b59f1863bb04790b8c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82654894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ee2989f40b8bf1d782733ee67a4d51f809eacb777913582e8a8d508df5aa0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bec0eb25faa85054bdacab8da9d9d50138c42aaa16df08715df2110d680cf979
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74482043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f100f56d88dba8d99909f4819951fbde0a33ce797e908064862c52abc53caf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22fde5fa3d322988856886c94d2da0c1dac1261effb3d5190e99883ecb3cad86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77198834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c741e0d6341ca4ad452547e9ef78adcc34894e284d00885f03ddac549222022`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:3e3707db6ce77a6240faf371c5d47bdb0f29ac3945fcfae3d9e5b174f7e9f0a4
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
$ docker pull buildpack-deps@sha256:6d6ba19df7ac34deaee2837c9989349bb222d5d8cd772c2eb08090a05b0404f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142722649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ee1b47cac952c9c05aa200b7d527b77f84c37804e50850b0d411f7b6d7b228`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da143e0f6d9787b0c89d6405a787ded9de6dcb65f3b9717f82da42f10ff997b6`  
		Last Modified: Sat, 30 Mar 2024 21:42:57 GMT  
		Size: 66.1 MB (66121672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29601816820e241abcad249b8e1c5a56b3c72320d3b1a09eee2f799a79570a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136438764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b05cb0813a14a71549c9b53c6ba587e924600042dbe0f5f87e324681afbaa0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4adcb1bcec984aff86f15319a4ef9bf43bac660d2c31fb398102ad3cc6190d3`  
		Last Modified: Sat, 30 Mar 2024 21:19:45 GMT  
		Size: 23.9 MB (23906632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb3d107ad7b8f22e25af7c2ea21540943257d714d5f5258c8275e541fd460cc`  
		Last Modified: Sat, 30 Mar 2024 21:20:04 GMT  
		Size: 63.8 MB (63848526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bcf0e6e53f87bdf060fe92e1ff43af0edfdcecdc7bf80642f4326d6c365ec6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130674564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3603e38a05a3732f16f7345c6d4a212bca05335fd34aa151adf86be572361f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba4b082de66bbca9897c8dba7f31512bba321ddd2a661347d670d910b4ef36`  
		Last Modified: Sat, 30 Mar 2024 21:30:50 GMT  
		Size: 61.3 MB (61251721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:960984f241bafb16c55235d8db73ba936e37461f733feb0b34fc2404c582b330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142537555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9dd4442662661fd0376972d939bfb99b7a961420e5af377a404911e9f4a1735`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3484d93fd537ed2435acc265bea31f7a3701955afec657d7cc9501a506f91`  
		Last Modified: Sat, 30 Mar 2024 21:42:50 GMT  
		Size: 24.8 MB (24829178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544cbfb4f7236143d102b4ef349f35d3d31527535f242406bbfd2d42dbfe60ee`  
		Last Modified: Sat, 30 Mar 2024 21:43:05 GMT  
		Size: 66.3 MB (66331165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d18fa777ebc7ea2e073e4bffda4c47de7132dd54b9fd9b1e58690f087de5d3a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146443487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b170d882dbbd60c1068d13fd4cadcf7e8399258e2290a48999a461dd9f1ca2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a15da4ef836ff60f9c28ef8b15ef8794d788a67c0a3d58b61d51a0e65213a7`  
		Last Modified: Sat, 30 Mar 2024 21:21:45 GMT  
		Size: 67.9 MB (67876237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6c77a5529a0384f610cc4238b7086ad705e14f1fc79c382bfafca81d6c957a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41ad8fc978f8d2925c94540c6b5928f5e0e55c43ab6d99a9e02b26e17a9b10b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f503a33191cf930c854f6db9bbbb4869ccbec7ff1c51ddc9f7c6a23aa26244a4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154344195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cad6e11ebc7819d06808e304fd24f559ffdd6df84c9f1b35094beb99311b6c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95220faf903de5c246bc60d7f00054712c075484056449785d59c657e22436e`  
		Last Modified: Sat, 30 Mar 2024 21:45:39 GMT  
		Size: 71.7 MB (71689301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3b84dd2e51c1d7bc38652a613a744353040ea2ab821b910ff694e3a1e13943c3
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140088921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9abff9aede153fe1ede007e697504da2ac4f742d4f9c5e8afd4ee1f6da6a91`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fd4dbd9609ca7faf0abe9ea6267b25c79eed962f75cf26a985c129d246a50`  
		Last Modified: Sat, 30 Mar 2024 21:27:33 GMT  
		Size: 24.8 MB (24782159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259a8b8d1c2e3af16628db8608e828fa16ec2c3aadfd7660f4716db301738d6b`  
		Last Modified: Sat, 30 Mar 2024 21:28:40 GMT  
		Size: 65.6 MB (65606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:58058792dbb38618b64512a4f523c0e2e7ea9bd12447bb2555e85a21fc99e831
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144622282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b467bd594b194ed628a97ca9f35ace2f08eff7d03179e6bb58a3f0701ebfee5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8b2bab401823952dea39f0a278dd656c849280f02e7b6f21ca4deddc0219d`  
		Last Modified: Sun, 31 Mar 2024 00:08:23 GMT  
		Size: 67.4 MB (67423448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
