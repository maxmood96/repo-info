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
$ docker pull buildpack-deps@sha256:7c2d048c0a368c7aad2c9409c70138e8dcc6b1affb8b3589aca958a54e72ee33
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
$ docker pull buildpack-deps@sha256:095a3d73823c37efcda081308a64796e34e3f0ddc7d889a16827bcd104d2d093
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
$ docker pull buildpack-deps@sha256:ecb390accba7f56cd439adc0f4ed96c18b55f0c918be417c328a19a1ae4b9dd6
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
$ docker pull buildpack-deps@sha256:8ebd7911641e02a7e6ad7e13d4b7a5176c1173fb7f42b8f59239ef1a8307aff6
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
$ docker pull buildpack-deps@sha256:31d0c494bc7400de931ec94b364886de3c36282586c30d0678439d763265c806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250129065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16b9f75d1553b439ba0476ff2bad50b9f62b80e322cce6cfb99d336a0c6ad1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:33:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016818fa25ad1e637fdb0c16cc94be31803d9b4257ef9986069ee1cd0333f72`  
		Last Modified: Fri, 16 Feb 2024 03:39:12 GMT  
		Size: 7.1 MB (7124928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0dc8191d96fccf341944ad312c97ff9192cfc4178313222e32a74e25e06920`  
		Last Modified: Fri, 16 Feb 2024 03:39:27 GMT  
		Size: 39.5 MB (39450372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ac7edfb3876d598b1bc0ea20e8c53260c894c562669446dfb13bbe9d299597`  
		Last Modified: Fri, 16 Feb 2024 03:39:57 GMT  
		Size: 173.1 MB (173103688 bytes)  
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
$ docker pull buildpack-deps@sha256:20bf94c658cfc60d08c489a22bda57970a4d4a77cfc79f1d16bdbda220a53fa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223846269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ae1083012c07e5c3e4997ed82d46c1eb1dc35ffee8c7dc8f868d3532d5dcb1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:20:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f01f2f9c0917b40af1232466a37506afd3230ca589df53da4c2fc4798eb5be`  
		Last Modified: Fri, 16 Feb 2024 06:33:33 GMT  
		Size: 7.0 MB (7038889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45425a34e07af7429c7e38b94ce06396c13e8eac144323aeededbbd1d4e46800`  
		Last Modified: Fri, 16 Feb 2024 06:33:48 GMT  
		Size: 39.4 MB (39416370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd4b5a4f68bbda130f3e8654ca930ee1f73f269b1245dbe0b7837e9abe133d4`  
		Last Modified: Fri, 16 Feb 2024 06:34:11 GMT  
		Size: 148.8 MB (148752286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:0e99d246c074cca22987e19823b83f66f6d1911cac88ea462ec07d1265517bf4
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
$ docker pull buildpack-deps@sha256:14cd02d4a1a6c9273ff20c9ebef3732d896f32f588714f2f05cbc6ed90110d07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37575005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059d7272994c76e4fae67d1d521900eef143b6b72493644bc2966558b0de7452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016818fa25ad1e637fdb0c16cc94be31803d9b4257ef9986069ee1cd0333f72`  
		Last Modified: Fri, 16 Feb 2024 03:39:12 GMT  
		Size: 7.1 MB (7124928 bytes)  
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
$ docker pull buildpack-deps@sha256:9a43a1b7e7f5016b02cc5f118e08bed994779dd5d50c192eb54f2696c62d6300
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35677613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7d966198ec95b2d731371a6db40ecab7b4a1a4c554152c9fe46766402f4a43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f01f2f9c0917b40af1232466a37506afd3230ca589df53da4c2fc4798eb5be`  
		Last Modified: Fri, 16 Feb 2024 06:33:33 GMT  
		Size: 7.0 MB (7038889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:62a2098d1fa9a74148b55396f4b10a95c28eafefc50009d9351d2e4d96840008
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
$ docker pull buildpack-deps@sha256:bfced0deafc3f1b0b9e3bddae7e681d334a19d92254fb3ff4a721296af9badac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77025377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338cb1dfb6d392cda4c631595a6eff8fe159d10e1beee56a9a88f43b24469035`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016818fa25ad1e637fdb0c16cc94be31803d9b4257ef9986069ee1cd0333f72`  
		Last Modified: Fri, 16 Feb 2024 03:39:12 GMT  
		Size: 7.1 MB (7124928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0dc8191d96fccf341944ad312c97ff9192cfc4178313222e32a74e25e06920`  
		Last Modified: Fri, 16 Feb 2024 03:39:27 GMT  
		Size: 39.5 MB (39450372 bytes)  
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
$ docker pull buildpack-deps@sha256:c7417ec1e8c2de7a1e746f846b29c764439b080abc2aca690cd0ce43b5002f8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75093983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10471b49a755eaa640639b4dca0de6f3707d71440bf4d827e9be8b7f4edfb6de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f01f2f9c0917b40af1232466a37506afd3230ca589df53da4c2fc4798eb5be`  
		Last Modified: Fri, 16 Feb 2024 06:33:33 GMT  
		Size: 7.0 MB (7038889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45425a34e07af7429c7e38b94ce06396c13e8eac144323aeededbbd1d4e46800`  
		Last Modified: Fri, 16 Feb 2024 06:33:48 GMT  
		Size: 39.4 MB (39416370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10`

```console
$ docker pull buildpack-deps@sha256:0031234de53c9563e4a6cd17de2b38a94425e932e7e809dda8bfd7b1b515a89e
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
$ docker pull buildpack-deps@sha256:92c581e07d813b5737dd9125bce0570538cf9ecac06a238a8fc84b15fd9b67e6
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
$ docker pull buildpack-deps@sha256:02343f558154e61d7f95295a73be1e616bcdd08b33b11525d3106ac4df870112
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
$ docker pull buildpack-deps@sha256:fe0dca775415139a02c93607d92cd39daadd28a7b6330e250b194b2f99e5caff
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
$ docker pull buildpack-deps@sha256:333917f6aa55aaa103d0b78bbb3743bda393e7d317bbcd3b1deb0f8b72031234
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323857558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01879effe0ec199729157e81f7d45cd0a74546be873c66d59fa0a688098b10f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b23ce13f84812ac6df1bc6603b609b4098273dd0ead57baadb72855d6221e`  
		Last Modified: Fri, 16 Feb 2024 03:41:09 GMT  
		Size: 231.6 MB (231608416 bytes)  
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
$ docker pull buildpack-deps@sha256:a48c64715451231c8f1a80ea6141dfde0c6839f220820139adcf2f675682e3e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305732967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3930ec12b77f5751f083122cae0faeb0b275c7bfabf5243027c90c511404b2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:31:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404889b91c64925706ad61665db8c07a99ed919566a735134342d7542d1607f2`  
		Last Modified: Fri, 16 Feb 2024 06:34:34 GMT  
		Size: 50.0 MB (49965092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cab934ab958cb8b6e6182f8598bbb4129e6c25c3c8e15805979f7c2026fa6e`  
		Last Modified: Fri, 16 Feb 2024 06:35:04 GMT  
		Size: 210.5 MB (210466296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:bfa00030cfc04c0ded2261f9b3428472aebf524a2b1d1f907e2a7a854a10c0f3
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
$ docker pull buildpack-deps@sha256:56ffc00ae277d7d43a3616cb6d583a8106f024bf1c30b424ed226bad3b982ae6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44110493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e864e112b75cb0ac68713a0ba92005fa72fb0b6175327b838ca78a95ff2869`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
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
$ docker pull buildpack-deps@sha256:88249b29234b01748c7c32377108e130a7bdf18e23eeb9e4fa201e924e9f9419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62482c207e5972a36cfd7c128da5fb0f72f707546c8a49c0bc8864dd03615228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:ac91ed94b5d8f59731debd39b99358ea7ddaa4dea0209a11568d10e7ef634c33
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
$ docker pull buildpack-deps@sha256:fe5c79afc853edbd845ac127d00b186f7df5e3920803a2c5c81bbc469e42173e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92249142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b08e273d8129a14881605da6c8c29203a789693212c0cb0238cc100fc740fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
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
$ docker pull buildpack-deps@sha256:d6b9c2c0467950293584f6f5f629c50c9b3cbc2f92a09e9642c94a5e742bca72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95266671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10897081722df1674fa655ab9f9f4c99ec007dd87f1d4ae6286777eaddae0c9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404889b91c64925706ad61665db8c07a99ed919566a735134342d7542d1607f2`  
		Last Modified: Fri, 16 Feb 2024 06:34:34 GMT  
		Size: 50.0 MB (49965092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:04d1c08832e425c7b6b5744b458e227c35f4ebb7841a912986bfaaabbc66e233
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
$ docker pull buildpack-deps@sha256:c3da82fc7ac70863e9bd6b1aa8274d5f546353260ff179eefbe7a22bce53a080
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348859945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e45ce51c523eaaae83f90227eb57a7854e8abf45a7f3be498589144a9095a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558fac597f8ecbb7a66712e14912ce1d83b23a92ca8b6ff14eef209ab01aff2`  
		Last Modified: Tue, 13 Feb 2024 01:31:35 GMT  
		Size: 211.1 MB (211120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:498d0147a44368abb2b05b684507da3aafa924e25a134a0aae869a18da79795c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316000608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aedbd3ab00a80b41114e2e156b27b06868112f9c245079c90dd49a30425f716`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:42:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4f2c673dee7c01dead9d002b58f94f192dedcd8cb540af771a3e99076df2ae`  
		Last Modified: Tue, 13 Feb 2024 01:54:59 GMT  
		Size: 184.4 MB (184448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8803cfa9be0301a6ac179d42ead5df09ce099585a8d3af82bc135a83b403e21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301405885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cde88f627e35b00c835f4ed62193ce13c65c97c5002b7741e4ae356ec2b9cc0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80088b70c07ea4625157344410c74a9f5aee9d7c29474b2a4353496defbfb5b1`  
		Last Modified: Tue, 13 Feb 2024 04:28:07 GMT  
		Size: 175.1 MB (175089000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3a1f628c5b65d19591d47e510fd56c43e103eeebf6fbe891397da18a7678fead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339684343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701f356a402fb855158c9f507c5043f953d84e1cfe645fd952668f57715d3f5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:38:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcabfc6c415bdafce0fb78b78afe51a8be789b05c4c3f5ccf5f1046bb5d32776`  
		Last Modified: Tue, 13 Feb 2024 01:47:24 GMT  
		Size: 202.5 MB (202519692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:75cdf1e75b5c0d85a316d078a374cbc929383d2a3ffc26d655786dd914d77f73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351499924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cd01f4c9df72780c2cc807cb245471bb21efd12d115b1687af42a18eca6c56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa04ac89e98e423a77743b83b547bbfed238c3f5c7c341959541005af241df49`  
		Last Modified: Tue, 13 Feb 2024 01:30:38 GMT  
		Size: 210.0 MB (210046749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fdfdb9bd1f480b2822305a8e8fca8bd401518d791ec9dd63660e798fcb4f60e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325869531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a4752654751c7693f8ce3207cb68b23715c1a73bbb6204e33f332632fbceb0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:51:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cedb7a3137759e51142758f8b7029dc78e57a3033813443144502d7ef4c020`  
		Last Modified: Tue, 13 Feb 2024 04:23:34 GMT  
		Size: 189.7 MB (189709673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bea1e0798704828403d6c7cb6a3b339cf5eb3bb029ff172b5be61bf585fb4d5e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362985389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590365a4815d6e17cfd6a4aeadd5cb54292d100096bbb709490dadeb8bf06460`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:23:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766a6e0e49a985c19ff5bed265467d9f1f6eada575066cf5a142c50bd88a57d`  
		Last Modified: Tue, 13 Feb 2024 07:37:13 GMT  
		Size: 214.2 MB (214151358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b79ddaa3322a2a9c7ecbccc12fe877e96794af1e9c3c76cddfedd37f7c722cf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318255163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d705af29279bf4338c1cfa62569d434d9a8d5c8ce7db7e15b91513dc85abf671`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:25:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef3f1a97bd13632e244781ae7503da3241b898fd89a42df192c290447f2cf03`  
		Last Modified: Tue, 13 Feb 2024 02:58:47 GMT  
		Size: 183.2 MB (183169094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:b5e504d3918d633d7ed04fce4cdbed4cbae55148cdbc58ef202ec693c1d8f0b4
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
$ docker pull buildpack-deps@sha256:71f969271cdbd16274234876785c2e276d8294aeb5d977b42aa83631f7684d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73599182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0aa610bb0fc1805c8cb5f5eba5f72a1c87aed088ea5c979c5eda30852c4514`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8a9bdc1a52ecbddda26ae35a9cc92b169bf05f3a06bffbdfb11cfa6feee08a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70036722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841f7172b5da0937e2db88203954c4184af0ca3c047129fd56a215e741f6ec3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ea690c06329fb428b4c350e3a936fc776641dbd292dea95644792d6450917c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67103937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf3b255e43b998fcb76ebb890056d1d75d577f00cb104ef631a5a99ec09dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a8a36d0aea4aac326643676b0219281617b83843b91154869b645ea24f34f9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bd33bdb130671b693e432fcf05cdd12d8531ea7cdee41f7f09e32b00c5dfd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c1100581a915bcad3c65d416ffa5c59f9c6791b8f7ed13a0d6458a162d9e669
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed05ae5df9ff35b46cdbf27e308cc5c8f0619b60a27b9b624f3682a6db147b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1eb12b7f00bf43b25969027e6f12677dfc58dad280fb933f580de8bc078d756f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a625c69e8c8ce460c71c8f5f00ef77fc19244edfa02315becfb08079afa69a21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4731c06396fd41e5380f3ddca1a02f78b4ac8b0d8146a2cca70323ebdb2337b4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f731a23661023501913e0d11c4da05333ebc54017ef0a8d5fac88af683fc803a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:25d3921209863ac81e2c3a9f89e054dac21c9999dc0f06980fcae587fe8d3d85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71959726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d37131e25319321b9b0612704137b0358484e6505251139244771e35c8bb71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:cdf130621a2dabec25c871f2f7c0a2a6249eee0f4d47c1cbb54b5e945b4e775d
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
$ docker pull buildpack-deps@sha256:fb5e878ec1dce3866ba1790e847f1e2a26a20f5dc847bbf9104f1bef0da7fb16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20f587594e57a8a88d79cb1afe4f962666bdd06f7a9c0ba33636724d9aa819c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5e7019261254418035af77dd442aaded3bd50f4de1a96870d4afa2bcfba2eb7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ac0eadd06c312ef3a2c044f5b46f099e5566136eb82c7d23de6a69e7376cf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:95923f973cf2f9e97e02a4131aa863ce5c250653a75bd73890dea3a6078a7beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed0c51c51c4a5dc12c8411b93f2f51ce9061f611b023b20589d29e13e5bf065`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f3b8888591ff7c3c5013181b8c438db8a849cb8ef8c5056953463f90836a44f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137164651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfa309b7928ccbb9ab1532b231841ac35c02e9e543f9f40793811a3bfccdf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:388d8b1f1f326bdba21772291704c24c93af8cd4551eacdf280bb29a4992644c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141453175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238a8e12c3f0469e141a977996ce5dda849e2a66e901149b745be538c37e747`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:07624084e774b4fa966627ae1efdcc05a78299cc645390e0d02981f3b1c820d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136159858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589fcf617f646e03d231a9c75cd7b2b8935071c2161639f341eaf8aab55432cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:12d1a1f3c60d59350f022eae19bdd24c04e1ca5f6f1d4a59bb6191fd11113bc0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a1365520d6a870826c979d1ae41072e965b7ccdd710879321b448476caaba4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41912604708dfd5334f32d83e6df641ecac0cefccd26dc4c0c55e4aa3ff17e84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135086069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129d9dfc6bce48b04c322295e7be11dbcbd47a8d8e0f0d8bd592b8875885a3e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:9e584d2e74a44772a611db8c2b3d5c0bc1a57d2656745e5708f0688d5d625fa8
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
$ docker pull buildpack-deps@sha256:ec4364bdd315fdc472bab4d87a51d587fcb1813d0cc1d17c6d21d89df0eef61c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322411585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0043ced802eacce5728603ccbb62ac3190bd373bce9b582161f98da78f736b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:23:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0209a266bb24310efc230a2cedc8c753df202b1367d6b917b3a6febaaa225fd`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 197.0 MB (196974754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:525115c2edae697e4c45a3d1215c43510ae8c1148127942a70744e704bda5c5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295449294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c52a214d5740de25e8b42c22a6ffdb58eebe7620bcfacd56959215dfbe7074c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:43:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:45:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc02d7d7d38fe07956e4599b2b651fc55e5e2b28292d866c9380c4dfe44188b0`  
		Last Modified: Tue, 13 Feb 2024 01:55:36 GMT  
		Size: 52.3 MB (52329047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb168a1b4717ff082f25d1e77a5afa2bceccca40396bd897118ae6007b17d88`  
		Last Modified: Tue, 13 Feb 2024 01:56:21 GMT  
		Size: 175.2 MB (175158430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e90e892194199b70baf56d5e6566392aae642702703c600de598a9c2ef529ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282916053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb2823f37d008d4e9e94775f76b00e550bb5c83b4dd517174c2fc27d1509498`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:17:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbdd712885977c538429b59aa851dd5be6499412cb7b2ba0cb37a20b9186252`  
		Last Modified: Tue, 13 Feb 2024 04:29:25 GMT  
		Size: 167.4 MB (167437433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bead412cd7bc6f3a520541a7fcb1adb88e2bbb8af483a53f3c01fef18180aed9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314047938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59152146c18b5d37112420b29537de263545d00d6cf7bbafed34adb431df8bb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65abc8b7accd0e9bdc9cc49eb9156409ec3f7da3e3f756461cedc2eba2531331`  
		Last Modified: Tue, 13 Feb 2024 01:48:18 GMT  
		Size: 189.9 MB (189883632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:10d8d71dd7e96d009759d44e6f191565426f5b0eeff411d895663efceac249e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328125738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ec0cea638ff65c42e03b56e5ef2e8a7dde50f3780d21635974021e96a15b9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830822b5fe9fcce0a36786775e56d3ebba121abaf50d97e715d9bb63fb9b2291`  
		Last Modified: Tue, 13 Feb 2024 01:31:14 GMT  
		Size: 55.9 MB (55927728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebf2d43c0cb851da7dfab2d9ae6a682f338a112bb35e5720e1105ddc4e26dda`  
		Last Modified: Tue, 13 Feb 2024 01:32:00 GMT  
		Size: 199.9 MB (199872460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d8529243fd7801839562450905e1c0c2fc68b800ba1b6df39e9d2098906a6003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301442584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75109778b4ba96fbb68d8c45527702d31775f6aa26f858ea8c90c3a52176c5a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:00:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b01501f8952da39445ba5df82589cc4034f4701bb34fc660690e4a1841ed4c`  
		Last Modified: Tue, 13 Feb 2024 04:24:44 GMT  
		Size: 53.3 MB (53310605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b7e5ed5b619e2f3d0a778cafde0e1fc84ca5cced5b5458d11a7ee49229b375`  
		Last Modified: Tue, 13 Feb 2024 04:26:42 GMT  
		Size: 179.1 MB (179094416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:259b518b1d580d800b84e8f725cd90d741153f0bb9ccbf83bd9fb4a34e630514
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330917736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f9fbc850eb68e2f347d7d5b47580dda634c6e551119a5b7df0a55317f22b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:26:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c4f70ca0212997eb1b2c82b5f1feb6920ff2654089e68975cba4b400a4451`  
		Last Modified: Tue, 13 Feb 2024 07:37:46 GMT  
		Size: 58.9 MB (58872935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b71a4e8c3360ab2f0fc44790fa318623d9b5bf860bb3aff76bf5e481709053`  
		Last Modified: Tue, 13 Feb 2024 07:38:23 GMT  
		Size: 196.3 MB (196324754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:40399894f40c09293a6bd15481f4c6b0eededdf9dcc7113d693bc3b02882019a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296007300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c0f21901c1d25a9333c9bacf48584ea60b83bbca832888bd4bdd698e907121`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:30:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb188cda5ee038922dabb4ba5c3c81be9096f05e1d4d4cdeab23a983e578d77`  
		Last Modified: Tue, 13 Feb 2024 02:59:09 GMT  
		Size: 54.1 MB (54076017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3290768c093f8e148cae12eaffa30fa6cd78ef3fa1c9639c07459aa92948e70`  
		Last Modified: Tue, 13 Feb 2024 02:59:33 GMT  
		Size: 173.0 MB (172970685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:b962d15af115bec13744d18db887b70f1cd214ff349848aa65ed3669cd9bdf1e
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
$ docker pull buildpack-deps@sha256:33e2f726c178caacc3a3230f83bd503fe5d23202237256adf9e2b55af0ed86ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4230b3e4bcd298bd9ab076e5def770bacf8ca055d26bca243a35a3a4809d17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c06bc5e596da68e541d1945e2c738494bbc749fee351b2aa949aa71bad6612ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67961817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4a2ec3c57ecae85345a0bcf9597d695fbd108cb75be3ad5cda7475eec249a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dbae290c16d068690f41fa20ae4285f139c2706e0146ddf9af72f24ff472205b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b0ffc707ded7337ff84765b4690514940a640c78d9494ff8730cf14369c2ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:606a04dc618c5b285d40fb7ec84d5732923f38fae0d4c4b7489b942fe35e01a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69470627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a912445217af04d8625a1b0b0e6d8ea4c548702559d8141eb63e00584b001b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:181b00ca45a400f3506725903a0f1bb9204e4a008af41ed8f31db39ac32d89ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72325550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa4f0bf68a9df19c762bb7d1faf854d4ce88305489a3e298bfb9abc459b4edf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f612116154a8cf673eea8fda22e01dff265d307a3a45f34ee167d6ea414c9456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69037563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4039f57e6dd822bcbdbef762b1eda72b73357ad98ac20061d2c1977f09e876a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d5632fb64e53862ab98e0cd37ecdf97ea6505bbd64c61d9807de3d9fe6702782
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f7217f3da1a232378210aba1327917a2a8c1187ee3d61a00999e0a6c2dfac9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b00da3f11b464d553016a1ab9c3bd2f59a79bcc555c40465966cba535158248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68960598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46db613acfb3f425b19419a4cd8be40519a125cf1784908dad907d7dcea2b4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:19e2b4b3203734e2ecc37fb3f73cdf532a87b72a38831b1f2563f4afe5625334
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
$ docker pull buildpack-deps@sha256:8977e048a8480b99b97e0a1c80140cca7452a6df6ef06f74d54c0ff232214335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125436831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcf2432ac3988d5974f0477ef18db3b32bf4ffb1e2b567904a456a77d760689`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9c32ce4faff0e4012772eb562a61fdccd7dd7f3e6c97af67ca9cf46a1721e98d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4a15aa63ca69cbbd5763c1c4f96f54fad207e42774924d7eec57519bc5c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:43:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc02d7d7d38fe07956e4599b2b651fc55e5e2b28292d866c9380c4dfe44188b0`  
		Last Modified: Tue, 13 Feb 2024 01:55:36 GMT  
		Size: 52.3 MB (52329047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a2f27fbd7df6f921e307c6b3842e06c4796bad9342cea45853a3860153e4506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115478620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633294151eb53a62585edd655f5a820a1f4cddb14fdf4bf4c7ad02a52515958f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8fc45901ab0495c46d50a3dc8d54b7ed9a3579f2ea74374f92fd68b9ef2b76d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124164306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088233470845dd66fc408aa5dfb3b09a754554d875476cd1b2971e8570739fa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:590295db46a73c7a0ad510538e83fcccf7925efcad6bf03a1d7efd80eef35d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128253278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c368009634b3257a5b9ce249447bae7abd576f288c9cc4f9c947c252750064d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830822b5fe9fcce0a36786775e56d3ebba121abaf50d97e715d9bb63fb9b2291`  
		Last Modified: Tue, 13 Feb 2024 01:31:14 GMT  
		Size: 55.9 MB (55927728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4e6a59b25679dffe9e5e0089270bf9258705db9d0e99f71759ba4c0be395ada4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122348168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f7a1eb919c361c8be5086c8756c3c7433aa038407da21c1967c356579b29a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b01501f8952da39445ba5df82589cc4034f4701bb34fc660690e4a1841ed4c`  
		Last Modified: Tue, 13 Feb 2024 04:24:44 GMT  
		Size: 53.3 MB (53310605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0e879a29487160a43c23e4b686dca12bb6fab5f57497b045ca2dfef25d5927b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134592982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba44c60109fcaa42d5784f3b7a4999c6cef9314e2e3e7220d7df62c43d9a7bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c4f70ca0212997eb1b2c82b5f1feb6920ff2654089e68975cba4b400a4451`  
		Last Modified: Tue, 13 Feb 2024 07:37:46 GMT  
		Size: 58.9 MB (58872935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4ac73ed6cff66207ec84a3968d0b0f1a59976ccc22ef8d3fe998fc99286acaa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123036615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4df4682dbd28e07f204a4bd1458f21bbb5720acfb4f26513f487cb2d06b55`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb188cda5ee038922dabb4ba5c3c81be9096f05e1d4d4cdeab23a983e578d77`  
		Last Modified: Tue, 13 Feb 2024 02:59:09 GMT  
		Size: 54.1 MB (54076017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:770ec23affa7fbccf8aca328fc040493ebf55dcba0d335ff9693a3df37122f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b1c9e7ce6903fa94c2b3f03f567d11dfee701cbd609df063a9ad36ce0fa8e1fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311895886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9874dbaa4e5f660d75aed1b4dfcbd114fd994b57605c4beb2fc95d308f0408eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:25:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5506dab13b722a0a2167c56d87ab89be676de83954672d39ea7d159e992a169`  
		Last Modified: Tue, 13 Feb 2024 01:33:34 GMT  
		Size: 191.9 MB (191934438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d5ef94cc92355c1edebc2b881079a0c6efcbf23957733fdf5d29cb394320ea0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277727847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed61e48e8847c8227e9c5b89252371e61b56aa9ede9c738f3b1d4076ad359cf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540545321e809bdd3253dc3e501c07157ca494eeb57e88cfc5f7c5ee705676c6`  
		Last Modified: Tue, 13 Feb 2024 04:29:56 GMT  
		Size: 47.4 MB (47410097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508c05504c73b82e0130fe371cfb5de03fef9bf8a98195962243261db202e8fb`  
		Last Modified: Tue, 13 Feb 2024 04:30:34 GMT  
		Size: 168.1 MB (168133783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9f38cf1ebe38840c849ddafba681fe393cf8da950b5aed49506651d6a1134a20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302468489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b3003cfad833ea0c7a9b3bb86d89947b765409f335ffd734a72e82c0159ddb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:41:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c6bc7c3a0dfb86749a480f02c7de49c95ed599190a22c2b030956c209624b`  
		Last Modified: Tue, 13 Feb 2024 01:48:43 GMT  
		Size: 52.2 MB (52224578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db194eb11c11aaae27c605c4494c48ff5c6fed400c810b6c101bff8d0e875459`  
		Last Modified: Tue, 13 Feb 2024 01:49:07 GMT  
		Size: 183.5 MB (183499542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c599298d79066b772b81128b1a1620592b7f32ad6e4750cd4c1ca6372f362d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321315894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374e59245d31877d21714838a3bcd92de3c784fc49d659c13da5667752558d16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:23:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5394ce220a4fdfe5a7557da33b1d28ce42579dd6401bfcece4be46f785212cb5`  
		Last Modified: Tue, 13 Feb 2024 01:33:21 GMT  
		Size: 198.5 MB (198470106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:8880072921960c6b650bb648c1a33f0252a4c92680cbc79229b72809aad006b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6b25066b29961e7aa16ca8406ce5ea650e3f8855c33e35ccaa115907dbfdea9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85804feeac02c23fe4d8e2f956ae269dc0d6bdd4dff8a8f46ce34da5cd61d63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69b0fed758544430d952e88e8f871fcdc5057b35e1abc2cedf5c498a758907db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667d89ecf61a4e936428ebb80edd5bb995a24dd2d67a86c8af566593ce355285`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4f164ec5a25585f32edddf47dfab977b6f777c1087a23e5cce3b3d7389864500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66744369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6df5fb88d550a5298172a8ac8559d862d8dcab6dca910aaaaa3f9a6e07e4c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0de08e18f1a2929dfd26d35b29bf2023e93138007d277e2b8e4ff6b7631e771d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae42ca5d891331e40f0cc8a32f83ba0912ecde69a7d2e2fabba6f37844828771`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:27b52c34737af31f5550a876d81343b03f115fbd3723516a5faf2f49539a65ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:afb08259f1ac535fe88bee2b3ea208cf5e321631169945cfb0d00109ed848cb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119961448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c979f5a4a9e45af0df32e4796505a3108bb8a91bf411c99d5151ef267c8f2cf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b02878f5a5ed75a04961083ade3732cf626aeb57be793a1e22bc7a8d5643428
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109594064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c619989ba56696218720a33254018f4653594a3bfc70c0cf6e15f137b0a2b1a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540545321e809bdd3253dc3e501c07157ca494eeb57e88cfc5f7c5ee705676c6`  
		Last Modified: Tue, 13 Feb 2024 04:29:56 GMT  
		Size: 47.4 MB (47410097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39aab6618e942bfedf2bb38d19946ce54a60a0a9f12f57ccef3a1544738a2fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118968947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5383738d040fad2e19ce081951827835339766b7f8e2cfc59ae2ddd9af31369e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c6bc7c3a0dfb86749a480f02c7de49c95ed599190a22c2b030956c209624b`  
		Last Modified: Tue, 13 Feb 2024 01:48:43 GMT  
		Size: 52.2 MB (52224578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e77e8e4e30b24b55c8167c85c97b09013b5ff67ed076602f377d18d035b2ef98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122845788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4a9d785bc03f2e98c30ae7b86ec864c22b1f55134e641482adafe1b0883e72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:b5e504d3918d633d7ed04fce4cdbed4cbae55148cdbc58ef202ec693c1d8f0b4
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
$ docker pull buildpack-deps@sha256:71f969271cdbd16274234876785c2e276d8294aeb5d977b42aa83631f7684d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73599182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0aa610bb0fc1805c8cb5f5eba5f72a1c87aed088ea5c979c5eda30852c4514`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8a9bdc1a52ecbddda26ae35a9cc92b169bf05f3a06bffbdfb11cfa6feee08a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70036722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841f7172b5da0937e2db88203954c4184af0ca3c047129fd56a215e741f6ec3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ea690c06329fb428b4c350e3a936fc776641dbd292dea95644792d6450917c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67103937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf3b255e43b998fcb76ebb890056d1d75d577f00cb104ef631a5a99ec09dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a8a36d0aea4aac326643676b0219281617b83843b91154869b645ea24f34f9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bd33bdb130671b693e432fcf05cdd12d8531ea7cdee41f7f09e32b00c5dfd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c1100581a915bcad3c65d416ffa5c59f9c6791b8f7ed13a0d6458a162d9e669
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed05ae5df9ff35b46cdbf27e308cc5c8f0619b60a27b9b624f3682a6db147b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1eb12b7f00bf43b25969027e6f12677dfc58dad280fb933f580de8bc078d756f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a625c69e8c8ce460c71c8f5f00ef77fc19244edfa02315becfb08079afa69a21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4731c06396fd41e5380f3ddca1a02f78b4ac8b0d8146a2cca70323ebdb2337b4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f731a23661023501913e0d11c4da05333ebc54017ef0a8d5fac88af683fc803a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:25d3921209863ac81e2c3a9f89e054dac21c9999dc0f06980fcae587fe8d3d85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71959726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d37131e25319321b9b0612704137b0358484e6505251139244771e35c8bb71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:7c2d048c0a368c7aad2c9409c70138e8dcc6b1affb8b3589aca958a54e72ee33
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
$ docker pull buildpack-deps@sha256:095a3d73823c37efcda081308a64796e34e3f0ddc7d889a16827bcd104d2d093
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
$ docker pull buildpack-deps@sha256:ecb390accba7f56cd439adc0f4ed96c18b55f0c918be417c328a19a1ae4b9dd6
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
$ docker pull buildpack-deps@sha256:8ebd7911641e02a7e6ad7e13d4b7a5176c1173fb7f42b8f59239ef1a8307aff6
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
$ docker pull buildpack-deps@sha256:31d0c494bc7400de931ec94b364886de3c36282586c30d0678439d763265c806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250129065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16b9f75d1553b439ba0476ff2bad50b9f62b80e322cce6cfb99d336a0c6ad1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:33:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016818fa25ad1e637fdb0c16cc94be31803d9b4257ef9986069ee1cd0333f72`  
		Last Modified: Fri, 16 Feb 2024 03:39:12 GMT  
		Size: 7.1 MB (7124928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0dc8191d96fccf341944ad312c97ff9192cfc4178313222e32a74e25e06920`  
		Last Modified: Fri, 16 Feb 2024 03:39:27 GMT  
		Size: 39.5 MB (39450372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ac7edfb3876d598b1bc0ea20e8c53260c894c562669446dfb13bbe9d299597`  
		Last Modified: Fri, 16 Feb 2024 03:39:57 GMT  
		Size: 173.1 MB (173103688 bytes)  
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
$ docker pull buildpack-deps@sha256:20bf94c658cfc60d08c489a22bda57970a4d4a77cfc79f1d16bdbda220a53fa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223846269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ae1083012c07e5c3e4997ed82d46c1eb1dc35ffee8c7dc8f868d3532d5dcb1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:20:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f01f2f9c0917b40af1232466a37506afd3230ca589df53da4c2fc4798eb5be`  
		Last Modified: Fri, 16 Feb 2024 06:33:33 GMT  
		Size: 7.0 MB (7038889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45425a34e07af7429c7e38b94ce06396c13e8eac144323aeededbbd1d4e46800`  
		Last Modified: Fri, 16 Feb 2024 06:33:48 GMT  
		Size: 39.4 MB (39416370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd4b5a4f68bbda130f3e8654ca930ee1f73f269b1245dbe0b7837e9abe133d4`  
		Last Modified: Fri, 16 Feb 2024 06:34:11 GMT  
		Size: 148.8 MB (148752286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:0e99d246c074cca22987e19823b83f66f6d1911cac88ea462ec07d1265517bf4
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
$ docker pull buildpack-deps@sha256:14cd02d4a1a6c9273ff20c9ebef3732d896f32f588714f2f05cbc6ed90110d07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37575005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059d7272994c76e4fae67d1d521900eef143b6b72493644bc2966558b0de7452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016818fa25ad1e637fdb0c16cc94be31803d9b4257ef9986069ee1cd0333f72`  
		Last Modified: Fri, 16 Feb 2024 03:39:12 GMT  
		Size: 7.1 MB (7124928 bytes)  
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
$ docker pull buildpack-deps@sha256:9a43a1b7e7f5016b02cc5f118e08bed994779dd5d50c192eb54f2696c62d6300
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35677613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7d966198ec95b2d731371a6db40ecab7b4a1a4c554152c9fe46766402f4a43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f01f2f9c0917b40af1232466a37506afd3230ca589df53da4c2fc4798eb5be`  
		Last Modified: Fri, 16 Feb 2024 06:33:33 GMT  
		Size: 7.0 MB (7038889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:62a2098d1fa9a74148b55396f4b10a95c28eafefc50009d9351d2e4d96840008
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
$ docker pull buildpack-deps@sha256:bfced0deafc3f1b0b9e3bddae7e681d334a19d92254fb3ff4a721296af9badac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77025377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338cb1dfb6d392cda4c631595a6eff8fe159d10e1beee56a9a88f43b24469035`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016818fa25ad1e637fdb0c16cc94be31803d9b4257ef9986069ee1cd0333f72`  
		Last Modified: Fri, 16 Feb 2024 03:39:12 GMT  
		Size: 7.1 MB (7124928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0dc8191d96fccf341944ad312c97ff9192cfc4178313222e32a74e25e06920`  
		Last Modified: Fri, 16 Feb 2024 03:39:27 GMT  
		Size: 39.5 MB (39450372 bytes)  
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
$ docker pull buildpack-deps@sha256:c7417ec1e8c2de7a1e746f846b29c764439b080abc2aca690cd0ce43b5002f8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75093983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10471b49a755eaa640639b4dca0de6f3707d71440bf4d827e9be8b7f4edfb6de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f01f2f9c0917b40af1232466a37506afd3230ca589df53da4c2fc4798eb5be`  
		Last Modified: Fri, 16 Feb 2024 06:33:33 GMT  
		Size: 7.0 MB (7038889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45425a34e07af7429c7e38b94ce06396c13e8eac144323aeededbbd1d4e46800`  
		Last Modified: Fri, 16 Feb 2024 06:33:48 GMT  
		Size: 39.4 MB (39416370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:04d1c08832e425c7b6b5744b458e227c35f4ebb7841a912986bfaaabbc66e233
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
$ docker pull buildpack-deps@sha256:c3da82fc7ac70863e9bd6b1aa8274d5f546353260ff179eefbe7a22bce53a080
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348859945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e45ce51c523eaaae83f90227eb57a7854e8abf45a7f3be498589144a9095a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558fac597f8ecbb7a66712e14912ce1d83b23a92ca8b6ff14eef209ab01aff2`  
		Last Modified: Tue, 13 Feb 2024 01:31:35 GMT  
		Size: 211.1 MB (211120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:498d0147a44368abb2b05b684507da3aafa924e25a134a0aae869a18da79795c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316000608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aedbd3ab00a80b41114e2e156b27b06868112f9c245079c90dd49a30425f716`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:42:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4f2c673dee7c01dead9d002b58f94f192dedcd8cb540af771a3e99076df2ae`  
		Last Modified: Tue, 13 Feb 2024 01:54:59 GMT  
		Size: 184.4 MB (184448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8803cfa9be0301a6ac179d42ead5df09ce099585a8d3af82bc135a83b403e21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301405885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cde88f627e35b00c835f4ed62193ce13c65c97c5002b7741e4ae356ec2b9cc0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80088b70c07ea4625157344410c74a9f5aee9d7c29474b2a4353496defbfb5b1`  
		Last Modified: Tue, 13 Feb 2024 04:28:07 GMT  
		Size: 175.1 MB (175089000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3a1f628c5b65d19591d47e510fd56c43e103eeebf6fbe891397da18a7678fead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339684343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701f356a402fb855158c9f507c5043f953d84e1cfe645fd952668f57715d3f5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:38:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcabfc6c415bdafce0fb78b78afe51a8be789b05c4c3f5ccf5f1046bb5d32776`  
		Last Modified: Tue, 13 Feb 2024 01:47:24 GMT  
		Size: 202.5 MB (202519692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:75cdf1e75b5c0d85a316d078a374cbc929383d2a3ffc26d655786dd914d77f73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351499924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cd01f4c9df72780c2cc807cb245471bb21efd12d115b1687af42a18eca6c56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa04ac89e98e423a77743b83b547bbfed238c3f5c7c341959541005af241df49`  
		Last Modified: Tue, 13 Feb 2024 01:30:38 GMT  
		Size: 210.0 MB (210046749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fdfdb9bd1f480b2822305a8e8fca8bd401518d791ec9dd63660e798fcb4f60e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325869531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a4752654751c7693f8ce3207cb68b23715c1a73bbb6204e33f332632fbceb0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:51:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cedb7a3137759e51142758f8b7029dc78e57a3033813443144502d7ef4c020`  
		Last Modified: Tue, 13 Feb 2024 04:23:34 GMT  
		Size: 189.7 MB (189709673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bea1e0798704828403d6c7cb6a3b339cf5eb3bb029ff172b5be61bf585fb4d5e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362985389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590365a4815d6e17cfd6a4aeadd5cb54292d100096bbb709490dadeb8bf06460`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:23:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766a6e0e49a985c19ff5bed265467d9f1f6eada575066cf5a142c50bd88a57d`  
		Last Modified: Tue, 13 Feb 2024 07:37:13 GMT  
		Size: 214.2 MB (214151358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b79ddaa3322a2a9c7ecbccc12fe877e96794af1e9c3c76cddfedd37f7c722cf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318255163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d705af29279bf4338c1cfa62569d434d9a8d5c8ce7db7e15b91513dc85abf671`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:25:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef3f1a97bd13632e244781ae7503da3241b898fd89a42df192c290447f2cf03`  
		Last Modified: Tue, 13 Feb 2024 02:58:47 GMT  
		Size: 183.2 MB (183169094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:0031234de53c9563e4a6cd17de2b38a94425e932e7e809dda8bfd7b1b515a89e
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
$ docker pull buildpack-deps@sha256:92c581e07d813b5737dd9125bce0570538cf9ecac06a238a8fc84b15fd9b67e6
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
$ docker pull buildpack-deps@sha256:02343f558154e61d7f95295a73be1e616bcdd08b33b11525d3106ac4df870112
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
$ docker pull buildpack-deps@sha256:fe0dca775415139a02c93607d92cd39daadd28a7b6330e250b194b2f99e5caff
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
$ docker pull buildpack-deps@sha256:333917f6aa55aaa103d0b78bbb3743bda393e7d317bbcd3b1deb0f8b72031234
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323857558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01879effe0ec199729157e81f7d45cd0a74546be873c66d59fa0a688098b10f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b23ce13f84812ac6df1bc6603b609b4098273dd0ead57baadb72855d6221e`  
		Last Modified: Fri, 16 Feb 2024 03:41:09 GMT  
		Size: 231.6 MB (231608416 bytes)  
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
$ docker pull buildpack-deps@sha256:a48c64715451231c8f1a80ea6141dfde0c6839f220820139adcf2f675682e3e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305732967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3930ec12b77f5751f083122cae0faeb0b275c7bfabf5243027c90c511404b2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:31:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404889b91c64925706ad61665db8c07a99ed919566a735134342d7542d1607f2`  
		Last Modified: Fri, 16 Feb 2024 06:34:34 GMT  
		Size: 50.0 MB (49965092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cab934ab958cb8b6e6182f8598bbb4129e6c25c3c8e15805979f7c2026fa6e`  
		Last Modified: Fri, 16 Feb 2024 06:35:04 GMT  
		Size: 210.5 MB (210466296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:bfa00030cfc04c0ded2261f9b3428472aebf524a2b1d1f907e2a7a854a10c0f3
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
$ docker pull buildpack-deps@sha256:56ffc00ae277d7d43a3616cb6d583a8106f024bf1c30b424ed226bad3b982ae6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44110493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e864e112b75cb0ac68713a0ba92005fa72fb0b6175327b838ca78a95ff2869`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
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
$ docker pull buildpack-deps@sha256:88249b29234b01748c7c32377108e130a7bdf18e23eeb9e4fa201e924e9f9419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62482c207e5972a36cfd7c128da5fb0f72f707546c8a49c0bc8864dd03615228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:ac91ed94b5d8f59731debd39b99358ea7ddaa4dea0209a11568d10e7ef634c33
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
$ docker pull buildpack-deps@sha256:fe5c79afc853edbd845ac127d00b186f7df5e3920803a2c5c81bbc469e42173e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92249142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b08e273d8129a14881605da6c8c29203a789693212c0cb0238cc100fc740fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
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
$ docker pull buildpack-deps@sha256:d6b9c2c0467950293584f6f5f629c50c9b3cbc2f92a09e9642c94a5e742bca72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95266671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10897081722df1674fa655ab9f9f4c99ec007dd87f1d4ae6286777eaddae0c9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404889b91c64925706ad61665db8c07a99ed919566a735134342d7542d1607f2`  
		Last Modified: Fri, 16 Feb 2024 06:34:34 GMT  
		Size: 50.0 MB (49965092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:770ec23affa7fbccf8aca328fc040493ebf55dcba0d335ff9693a3df37122f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b1c9e7ce6903fa94c2b3f03f567d11dfee701cbd609df063a9ad36ce0fa8e1fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311895886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9874dbaa4e5f660d75aed1b4dfcbd114fd994b57605c4beb2fc95d308f0408eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:25:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5506dab13b722a0a2167c56d87ab89be676de83954672d39ea7d159e992a169`  
		Last Modified: Tue, 13 Feb 2024 01:33:34 GMT  
		Size: 191.9 MB (191934438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d5ef94cc92355c1edebc2b881079a0c6efcbf23957733fdf5d29cb394320ea0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277727847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed61e48e8847c8227e9c5b89252371e61b56aa9ede9c738f3b1d4076ad359cf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540545321e809bdd3253dc3e501c07157ca494eeb57e88cfc5f7c5ee705676c6`  
		Last Modified: Tue, 13 Feb 2024 04:29:56 GMT  
		Size: 47.4 MB (47410097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508c05504c73b82e0130fe371cfb5de03fef9bf8a98195962243261db202e8fb`  
		Last Modified: Tue, 13 Feb 2024 04:30:34 GMT  
		Size: 168.1 MB (168133783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9f38cf1ebe38840c849ddafba681fe393cf8da950b5aed49506651d6a1134a20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302468489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b3003cfad833ea0c7a9b3bb86d89947b765409f335ffd734a72e82c0159ddb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:41:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c6bc7c3a0dfb86749a480f02c7de49c95ed599190a22c2b030956c209624b`  
		Last Modified: Tue, 13 Feb 2024 01:48:43 GMT  
		Size: 52.2 MB (52224578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db194eb11c11aaae27c605c4494c48ff5c6fed400c810b6c101bff8d0e875459`  
		Last Modified: Tue, 13 Feb 2024 01:49:07 GMT  
		Size: 183.5 MB (183499542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c599298d79066b772b81128b1a1620592b7f32ad6e4750cd4c1ca6372f362d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321315894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374e59245d31877d21714838a3bcd92de3c784fc49d659c13da5667752558d16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:23:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5394ce220a4fdfe5a7557da33b1d28ce42579dd6401bfcece4be46f785212cb5`  
		Last Modified: Tue, 13 Feb 2024 01:33:21 GMT  
		Size: 198.5 MB (198470106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:8880072921960c6b650bb648c1a33f0252a4c92680cbc79229b72809aad006b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6b25066b29961e7aa16ca8406ce5ea650e3f8855c33e35ccaa115907dbfdea9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85804feeac02c23fe4d8e2f956ae269dc0d6bdd4dff8a8f46ce34da5cd61d63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69b0fed758544430d952e88e8f871fcdc5057b35e1abc2cedf5c498a758907db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667d89ecf61a4e936428ebb80edd5bb995a24dd2d67a86c8af566593ce355285`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4f164ec5a25585f32edddf47dfab977b6f777c1087a23e5cce3b3d7389864500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66744369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6df5fb88d550a5298172a8ac8559d862d8dcab6dca910aaaaa3f9a6e07e4c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0de08e18f1a2929dfd26d35b29bf2023e93138007d277e2b8e4ff6b7631e771d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae42ca5d891331e40f0cc8a32f83ba0912ecde69a7d2e2fabba6f37844828771`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:27b52c34737af31f5550a876d81343b03f115fbd3723516a5faf2f49539a65ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:afb08259f1ac535fe88bee2b3ea208cf5e321631169945cfb0d00109ed848cb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119961448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c979f5a4a9e45af0df32e4796505a3108bb8a91bf411c99d5151ef267c8f2cf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b02878f5a5ed75a04961083ade3732cf626aeb57be793a1e22bc7a8d5643428
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109594064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c619989ba56696218720a33254018f4653594a3bfc70c0cf6e15f137b0a2b1a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540545321e809bdd3253dc3e501c07157ca494eeb57e88cfc5f7c5ee705676c6`  
		Last Modified: Tue, 13 Feb 2024 04:29:56 GMT  
		Size: 47.4 MB (47410097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39aab6618e942bfedf2bb38d19946ce54a60a0a9f12f57ccef3a1544738a2fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118968947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5383738d040fad2e19ce081951827835339766b7f8e2cfc59ae2ddd9af31369e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c6bc7c3a0dfb86749a480f02c7de49c95ed599190a22c2b030956c209624b`  
		Last Modified: Tue, 13 Feb 2024 01:48:43 GMT  
		Size: 52.2 MB (52224578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e77e8e4e30b24b55c8167c85c97b09013b5ff67ed076602f377d18d035b2ef98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122845788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4a9d785bc03f2e98c30ae7b86ec864c22b1f55134e641482adafe1b0883e72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:9e584d2e74a44772a611db8c2b3d5c0bc1a57d2656745e5708f0688d5d625fa8
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
$ docker pull buildpack-deps@sha256:ec4364bdd315fdc472bab4d87a51d587fcb1813d0cc1d17c6d21d89df0eef61c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322411585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0043ced802eacce5728603ccbb62ac3190bd373bce9b582161f98da78f736b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:23:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0209a266bb24310efc230a2cedc8c753df202b1367d6b917b3a6febaaa225fd`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 197.0 MB (196974754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:525115c2edae697e4c45a3d1215c43510ae8c1148127942a70744e704bda5c5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295449294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c52a214d5740de25e8b42c22a6ffdb58eebe7620bcfacd56959215dfbe7074c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:43:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:45:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc02d7d7d38fe07956e4599b2b651fc55e5e2b28292d866c9380c4dfe44188b0`  
		Last Modified: Tue, 13 Feb 2024 01:55:36 GMT  
		Size: 52.3 MB (52329047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb168a1b4717ff082f25d1e77a5afa2bceccca40396bd897118ae6007b17d88`  
		Last Modified: Tue, 13 Feb 2024 01:56:21 GMT  
		Size: 175.2 MB (175158430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e90e892194199b70baf56d5e6566392aae642702703c600de598a9c2ef529ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282916053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb2823f37d008d4e9e94775f76b00e550bb5c83b4dd517174c2fc27d1509498`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:17:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbdd712885977c538429b59aa851dd5be6499412cb7b2ba0cb37a20b9186252`  
		Last Modified: Tue, 13 Feb 2024 04:29:25 GMT  
		Size: 167.4 MB (167437433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bead412cd7bc6f3a520541a7fcb1adb88e2bbb8af483a53f3c01fef18180aed9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314047938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59152146c18b5d37112420b29537de263545d00d6cf7bbafed34adb431df8bb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65abc8b7accd0e9bdc9cc49eb9156409ec3f7da3e3f756461cedc2eba2531331`  
		Last Modified: Tue, 13 Feb 2024 01:48:18 GMT  
		Size: 189.9 MB (189883632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:10d8d71dd7e96d009759d44e6f191565426f5b0eeff411d895663efceac249e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328125738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ec0cea638ff65c42e03b56e5ef2e8a7dde50f3780d21635974021e96a15b9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830822b5fe9fcce0a36786775e56d3ebba121abaf50d97e715d9bb63fb9b2291`  
		Last Modified: Tue, 13 Feb 2024 01:31:14 GMT  
		Size: 55.9 MB (55927728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebf2d43c0cb851da7dfab2d9ae6a682f338a112bb35e5720e1105ddc4e26dda`  
		Last Modified: Tue, 13 Feb 2024 01:32:00 GMT  
		Size: 199.9 MB (199872460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d8529243fd7801839562450905e1c0c2fc68b800ba1b6df39e9d2098906a6003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301442584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75109778b4ba96fbb68d8c45527702d31775f6aa26f858ea8c90c3a52176c5a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:00:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b01501f8952da39445ba5df82589cc4034f4701bb34fc660690e4a1841ed4c`  
		Last Modified: Tue, 13 Feb 2024 04:24:44 GMT  
		Size: 53.3 MB (53310605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b7e5ed5b619e2f3d0a778cafde0e1fc84ca5cced5b5458d11a7ee49229b375`  
		Last Modified: Tue, 13 Feb 2024 04:26:42 GMT  
		Size: 179.1 MB (179094416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:259b518b1d580d800b84e8f725cd90d741153f0bb9ccbf83bd9fb4a34e630514
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330917736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f9fbc850eb68e2f347d7d5b47580dda634c6e551119a5b7df0a55317f22b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:26:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c4f70ca0212997eb1b2c82b5f1feb6920ff2654089e68975cba4b400a4451`  
		Last Modified: Tue, 13 Feb 2024 07:37:46 GMT  
		Size: 58.9 MB (58872935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b71a4e8c3360ab2f0fc44790fa318623d9b5bf860bb3aff76bf5e481709053`  
		Last Modified: Tue, 13 Feb 2024 07:38:23 GMT  
		Size: 196.3 MB (196324754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:40399894f40c09293a6bd15481f4c6b0eededdf9dcc7113d693bc3b02882019a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296007300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c0f21901c1d25a9333c9bacf48584ea60b83bbca832888bd4bdd698e907121`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:30:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb188cda5ee038922dabb4ba5c3c81be9096f05e1d4d4cdeab23a983e578d77`  
		Last Modified: Tue, 13 Feb 2024 02:59:09 GMT  
		Size: 54.1 MB (54076017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3290768c093f8e148cae12eaffa30fa6cd78ef3fa1c9639c07459aa92948e70`  
		Last Modified: Tue, 13 Feb 2024 02:59:33 GMT  
		Size: 173.0 MB (172970685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:b962d15af115bec13744d18db887b70f1cd214ff349848aa65ed3669cd9bdf1e
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
$ docker pull buildpack-deps@sha256:33e2f726c178caacc3a3230f83bd503fe5d23202237256adf9e2b55af0ed86ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4230b3e4bcd298bd9ab076e5def770bacf8ca055d26bca243a35a3a4809d17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c06bc5e596da68e541d1945e2c738494bbc749fee351b2aa949aa71bad6612ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67961817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4a2ec3c57ecae85345a0bcf9597d695fbd108cb75be3ad5cda7475eec249a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dbae290c16d068690f41fa20ae4285f139c2706e0146ddf9af72f24ff472205b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b0ffc707ded7337ff84765b4690514940a640c78d9494ff8730cf14369c2ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:606a04dc618c5b285d40fb7ec84d5732923f38fae0d4c4b7489b942fe35e01a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69470627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a912445217af04d8625a1b0b0e6d8ea4c548702559d8141eb63e00584b001b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:181b00ca45a400f3506725903a0f1bb9204e4a008af41ed8f31db39ac32d89ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72325550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa4f0bf68a9df19c762bb7d1faf854d4ce88305489a3e298bfb9abc459b4edf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f612116154a8cf673eea8fda22e01dff265d307a3a45f34ee167d6ea414c9456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69037563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4039f57e6dd822bcbdbef762b1eda72b73357ad98ac20061d2c1977f09e876a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d5632fb64e53862ab98e0cd37ecdf97ea6505bbd64c61d9807de3d9fe6702782
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75720047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f7217f3da1a232378210aba1327917a2a8c1187ee3d61a00999e0a6c2dfac9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b00da3f11b464d553016a1ab9c3bd2f59a79bcc555c40465966cba535158248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68960598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46db613acfb3f425b19419a4cd8be40519a125cf1784908dad907d7dcea2b4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:19e2b4b3203734e2ecc37fb3f73cdf532a87b72a38831b1f2563f4afe5625334
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
$ docker pull buildpack-deps@sha256:8977e048a8480b99b97e0a1c80140cca7452a6df6ef06f74d54c0ff232214335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125436831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcf2432ac3988d5974f0477ef18db3b32bf4ffb1e2b567904a456a77d760689`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9c32ce4faff0e4012772eb562a61fdccd7dd7f3e6c97af67ca9cf46a1721e98d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4a15aa63ca69cbbd5763c1c4f96f54fad207e42774924d7eec57519bc5c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:43:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc02d7d7d38fe07956e4599b2b651fc55e5e2b28292d866c9380c4dfe44188b0`  
		Last Modified: Tue, 13 Feb 2024 01:55:36 GMT  
		Size: 52.3 MB (52329047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a2f27fbd7df6f921e307c6b3842e06c4796bad9342cea45853a3860153e4506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115478620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633294151eb53a62585edd655f5a820a1f4cddb14fdf4bf4c7ad02a52515958f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8fc45901ab0495c46d50a3dc8d54b7ed9a3579f2ea74374f92fd68b9ef2b76d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124164306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088233470845dd66fc408aa5dfb3b09a754554d875476cd1b2971e8570739fa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:590295db46a73c7a0ad510538e83fcccf7925efcad6bf03a1d7efd80eef35d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128253278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c368009634b3257a5b9ce249447bae7abd576f288c9cc4f9c947c252750064d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830822b5fe9fcce0a36786775e56d3ebba121abaf50d97e715d9bb63fb9b2291`  
		Last Modified: Tue, 13 Feb 2024 01:31:14 GMT  
		Size: 55.9 MB (55927728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4e6a59b25679dffe9e5e0089270bf9258705db9d0e99f71759ba4c0be395ada4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122348168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f7a1eb919c361c8be5086c8756c3c7433aa038407da21c1967c356579b29a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b01501f8952da39445ba5df82589cc4034f4701bb34fc660690e4a1841ed4c`  
		Last Modified: Tue, 13 Feb 2024 04:24:44 GMT  
		Size: 53.3 MB (53310605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0e879a29487160a43c23e4b686dca12bb6fab5f57497b045ca2dfef25d5927b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134592982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba44c60109fcaa42d5784f3b7a4999c6cef9314e2e3e7220d7df62c43d9a7bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c4f70ca0212997eb1b2c82b5f1feb6920ff2654089e68975cba4b400a4451`  
		Last Modified: Tue, 13 Feb 2024 07:37:46 GMT  
		Size: 58.9 MB (58872935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4ac73ed6cff66207ec84a3968d0b0f1a59976ccc22ef8d3fe998fc99286acaa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123036615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4df4682dbd28e07f204a4bd1458f21bbb5720acfb4f26513f487cb2d06b55`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb188cda5ee038922dabb4ba5c3c81be9096f05e1d4d4cdeab23a983e578d77`  
		Last Modified: Tue, 13 Feb 2024 02:59:09 GMT  
		Size: 54.1 MB (54076017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:cdf130621a2dabec25c871f2f7c0a2a6249eee0f4d47c1cbb54b5e945b4e775d
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
$ docker pull buildpack-deps@sha256:fb5e878ec1dce3866ba1790e847f1e2a26a20f5dc847bbf9104f1bef0da7fb16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20f587594e57a8a88d79cb1afe4f962666bdd06f7a9c0ba33636724d9aa819c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5e7019261254418035af77dd442aaded3bd50f4de1a96870d4afa2bcfba2eb7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ac0eadd06c312ef3a2c044f5b46f099e5566136eb82c7d23de6a69e7376cf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:95923f973cf2f9e97e02a4131aa863ce5c250653a75bd73890dea3a6078a7beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed0c51c51c4a5dc12c8411b93f2f51ce9061f611b023b20589d29e13e5bf065`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f3b8888591ff7c3c5013181b8c438db8a849cb8ef8c5056953463f90836a44f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137164651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfa309b7928ccbb9ab1532b231841ac35c02e9e543f9f40793811a3bfccdf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:388d8b1f1f326bdba21772291704c24c93af8cd4551eacdf280bb29a4992644c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141453175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238a8e12c3f0469e141a977996ce5dda849e2a66e901149b745be538c37e747`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:07624084e774b4fa966627ae1efdcc05a78299cc645390e0d02981f3b1c820d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136159858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589fcf617f646e03d231a9c75cd7b2b8935071c2161639f341eaf8aab55432cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:12d1a1f3c60d59350f022eae19bdd24c04e1ca5f6f1d4a59bb6191fd11113bc0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a1365520d6a870826c979d1ae41072e965b7ccdd710879321b448476caaba4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41912604708dfd5334f32d83e6df641ecac0cefccd26dc4c0c55e4aa3ff17e84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135086069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129d9dfc6bce48b04c322295e7be11dbcbd47a8d8e0f0d8bd592b8875885a3e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:9ca794c4139f1f2fd668ad43db2b4ff778a1030a17c3a40e022e93e06394e9af
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
$ docker pull buildpack-deps@sha256:c5f624e22f63eab74ad44c949c411907e08323fd94f954dc217eabeb8a1086b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 MB (407116189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d209584b062cf0549b2080529ebf79610669da99af4644b934a2841095e3e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94778b4f8d542570a58f18b952aac258e2970cab96fd361b214bfa16118b00`  
		Last Modified: Tue, 13 Feb 2024 01:34:04 GMT  
		Size: 66.5 MB (66468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80def60bd73e3a9a5705eaecdbe842048e3d84a1c605e6fae357e8be7cf6e617`  
		Last Modified: Tue, 13 Feb 2024 01:34:45 GMT  
		Size: 264.1 MB (264140563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bcf7327d7f12ffc8a2a41a1f361e1cf6533d82877429896f0da0f01ae3fdc5bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370331989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41519ced967b01b112d200b16c18a1a11bc1f34d907ed1811981430e1eb64146`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:50:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7541155b76422a64edf910ec2131b609a880f2b83ac01ac06abd5cb73d5ee`  
		Last Modified: Tue, 13 Feb 2024 01:57:51 GMT  
		Size: 233.7 MB (233747841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8a188b1ac61aeeaf35024c340f52f63a0132ba4657889d2e9437aca5527433b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348778060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ad35eb2f1a3a5e5732ca672c9f3ce8c926a53741aa176c8e2fd0870378fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:22:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496516de4f431d258aba363886cad002ce4f57baeffcdf4e252ed7edd24c0f9`  
		Last Modified: Tue, 13 Feb 2024 04:31:58 GMT  
		Size: 218.0 MB (218020845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fa0f545d4430defd649acd3e14a5d481038bd7bcb00a39eca14e998bb2040b88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395048369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd48be5b1aae01f7999d77c7503552362d2ad656276c58aa8043f9387888794`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:42:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:43:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313a023dd2178b52531ace278aad9cfe2b7b237ef6b56c93424eefb6724d585`  
		Last Modified: Tue, 13 Feb 2024 01:49:39 GMT  
		Size: 66.6 MB (66566375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10eefeb9a7dd28dee992ba5b7e16f5b64a8d5549fb74ba8d4d7cf0c53c4dfe`  
		Last Modified: Tue, 13 Feb 2024 01:50:12 GMT  
		Size: 252.4 MB (252400519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:251fddb93de647e92e5db9520b50e234245592088d0ea64935cc2fc9cc92550f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403617689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e0fb16df1b72057c3fe1def6cc1a9b8c83fe2c54bd9320847a6a63ffc2d62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef40ea4fb0aaa505ca0fc627a4b7f559f54d7f3a06a621779b84c00fb13dc3d`  
		Last Modified: Tue, 13 Feb 2024 01:35:03 GMT  
		Size: 256.9 MB (256910908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b492a050d8bee6734d4e7fddf2b7dfc78e633a132a169b1e1700ee0a9229feb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (374000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35abde10cd1ddc508f26b152e3ed074e3faab5ae5a9689f6d148e8967c4806b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:10:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6328e06fb256ea30715aa4016628a9149817a5fd5af519caa1fc97eed490e251`  
		Last Modified: Tue, 13 Feb 2024 04:28:01 GMT  
		Size: 65.3 MB (65264661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0279072739c3e1a41c7935740d8cbb0cebb904baa4052f248b0c7367bbdcc76`  
		Last Modified: Tue, 13 Feb 2024 04:30:38 GMT  
		Size: 232.7 MB (232696791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cb959a6bb47eee2998308c197d3c0ca38ecc6b48e80abec53dd7ecb715a5c226
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417863444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbe3e9b6748ebc3010b3c56484c4abd26ff4e2995d92e0c772c765eda4038c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:31:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a5c8875e799e5e279fbdd05c6f1210fc9492749ce7709449def06189f5a739`  
		Last Modified: Tue, 13 Feb 2024 07:38:56 GMT  
		Size: 72.0 MB (71962170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa143fea443b5fbf9767fb081bf4a51c014002c74db280206fed9c76c7a2e6`  
		Last Modified: Tue, 13 Feb 2024 07:39:45 GMT  
		Size: 263.4 MB (263404095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:57831dfaf93e60466e60bb0361b71f5bef513395b770321bf8395f2126f28eac
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.7 MB (435678773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7161e3929956969d644f37455c71a73d206a7eb668a1eb5898c7287c8ee4e6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:40:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759b918e35db2dd593162c00a042bb80cc9bea4f8643a193ebb8f688356fa5d4`  
		Last Modified: Tue, 13 Feb 2024 01:42:44 GMT  
		Size: 65.7 MB (65714562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1c45ab68df68f5378f8164324aa1dad55295edf91785eebdc4ab678e13fa3`  
		Last Modified: Tue, 13 Feb 2024 01:48:38 GMT  
		Size: 295.6 MB (295606402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cbcf2b8c203819dcee64abf3e7c40fe72103115355dc0546c993a533fc14fe44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385275888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91997c3e812b362628e372aa2d09a9a6cf7ff77aa137b4fcba2a62a8754bf29f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d71e89930040fcd5c9bab43bc590b577afe0564c16033af772417a01da471`  
		Last Modified: Tue, 13 Feb 2024 02:59:57 GMT  
		Size: 67.6 MB (67555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4950bfd2260fcacae5cb79b071be191ad22b275987a43ed9ab875aea6929a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:36 GMT  
		Size: 240.7 MB (240670966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:8c74f4bb17335392329320c3e636203e880e20ad49656d32bdac0933452198bd
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
$ docker pull buildpack-deps@sha256:d1c743af9b2f43730e2f8d2a90966952e1c05d7eba867f064b254d425e63f787
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76507372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7e3baed9409d7c78f0e08ccd5994257277c2e71b13f26b332343359456f03a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b839041109743d570e5b781207c8b6dd0d83f7a02c1312c39b3abb5859206ead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72475557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0f7d477c9f33dfcd2679ea280f5c1a52efe266dd8936b0206e4796fc5b1727`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6b8be762fd7b820a830a3321642176df58972875bda564d8ab9992399b21a19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69289468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847f66994b4f16318f221a7a1e0bfc18624e296073c3f43d158ff2b83d9c8b0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:471947f5197058ebfb95666bd4796655232ffb21a10bbe66bfbf513c998d6c5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ed0f568e4e46400479da1e5ad8a697b7df7d49591b78efc93ef2fd2b0e9091`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5a308728d3b203f524e96e1e51691b47168168b7318136b03ff137e66eb6ee7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78457588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b0696be583a4588b82ce28f76fa3e2241256e439d3cf9a96e63c5314f54a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a4a8db675393ee92fe409ef196cc95ae2101616b16dcd567cbee927d7adacb37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eca413a639eeb7f89bb3aba1e73462639a1e199d4687fb37ade8e121335cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8ca8a63e9f98ec918b00dbfa0cbfb9e821cec7c7b9a7262e2ebfb57dbf86c5bb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82497179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add37801d447fd77e633588185ca27ec48e8f097c48c4bfc36b48bec7ba57b3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:05da3f23abd0d4fdbfd32e5862e58f132da411fbe7b4892ceb60ffcfc563174f
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74357809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb3bebb24086f8a3702016ae8531035dfdc9bbc785d2b5466db4bcd57ca1d2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3d8adea1bb07411818beb7059fe1c1f46540e6069549a17757b87bacba9eb7c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73e082015284c35b32815c0f3361322c3f497023955778b8843b6cde5ef827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:634a3e8d91bc4a5cb62bac2a3ab857376d21fce1f5815381c616682b28aa2807
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
$ docker pull buildpack-deps@sha256:0bb071c1266f203b2041ca93497a739fe9d4349b7c7853cff4887a81e059f022
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142975626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdde92020438ebe73f96a17fc7307a7b413d194374d50b71e68efb8a6944608b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94778b4f8d542570a58f18b952aac258e2970cab96fd361b214bfa16118b00`  
		Last Modified: Tue, 13 Feb 2024 01:34:04 GMT  
		Size: 66.5 MB (66468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1cec2114b9fbc4843b5cf0b9c8fbaa74c4b4b83edaefe5346dfc5a2325eb6d89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136584148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9fdbbebeb90640507c0fe9c9c7f94c49092e2b2457779acf670d041930ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:779fa01b9f5918a69716dbdf3d599dd12913476ec65cd9c5bc05a41183678baa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130757215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d298e5bd648d71e4c86864a1c66f3452d3e31f41781f27ee8a9c9d9a15fd7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4c705bda8f8f91e639cf3638fc33c9feb0ee0193c9dde109b78bbe6a45204325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142647850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd40f6dc2d9a57c3494b8c18be9c992dbdee27bbb8e85d2653ee05954ba2f66c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:42:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313a023dd2178b52531ace278aad9cfe2b7b237ef6b56c93424eefb6724d585`  
		Last Modified: Tue, 13 Feb 2024 01:49:39 GMT  
		Size: 66.6 MB (66566375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5c9106633d47775077bc4f62164c7fa00a7ee8d404348145e6f41c9cac5a2886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146706781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c92dfca00a5b2fbf2cb1672a258505f21b5cf25b37447b3e807b9f6c27863d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:351c91be38a50c74c25edc544bd502d4f74e3b6de4654e5aad3ea980b4281238
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141303459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e68e0576b452fb51c345c98058dda8777da05598f125487b7fa516a3863973`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6328e06fb256ea30715aa4016628a9149817a5fd5af519caa1fc97eed490e251`  
		Last Modified: Tue, 13 Feb 2024 04:28:01 GMT  
		Size: 65.3 MB (65264661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a6262101470d5f902e746a0fd115dc08a5bffd3790d17e56b29e2d14069a3ef
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154459349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abb73597e516d0a2f1196348483cff4c2caa8d87ebf42ad3cfea2b1ce78864a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a5c8875e799e5e279fbdd05c6f1210fc9492749ce7709449def06189f5a739`  
		Last Modified: Tue, 13 Feb 2024 07:38:56 GMT  
		Size: 72.0 MB (71962170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8cddfb384ed7eda6cf63effa0216f3b88205274484e895ec8d600f7a47555ec5
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140072371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af13fdd86228575c0423c9cc3a2a23c756cf4d2d71c5b4f8d912ea669bf54afe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759b918e35db2dd593162c00a042bb80cc9bea4f8643a193ebb8f688356fa5d4`  
		Last Modified: Tue, 13 Feb 2024 01:42:44 GMT  
		Size: 65.7 MB (65714562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cdcb147cf298be69685f44453fc0886d5b00156f2a176a5ebd4c3af96ee77356
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144604922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc10f37875adb45d677b6de292e99fb4740b93d3444cb3b8c0f9450701015d0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d71e89930040fcd5c9bab43bc590b577afe0564c16033af772417a01da471`  
		Last Modified: Tue, 13 Feb 2024 02:59:57 GMT  
		Size: 67.6 MB (67555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:04d1c08832e425c7b6b5744b458e227c35f4ebb7841a912986bfaaabbc66e233
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
$ docker pull buildpack-deps@sha256:c3da82fc7ac70863e9bd6b1aa8274d5f546353260ff179eefbe7a22bce53a080
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348859945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e45ce51c523eaaae83f90227eb57a7854e8abf45a7f3be498589144a9095a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558fac597f8ecbb7a66712e14912ce1d83b23a92ca8b6ff14eef209ab01aff2`  
		Last Modified: Tue, 13 Feb 2024 01:31:35 GMT  
		Size: 211.1 MB (211120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:498d0147a44368abb2b05b684507da3aafa924e25a134a0aae869a18da79795c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316000608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aedbd3ab00a80b41114e2e156b27b06868112f9c245079c90dd49a30425f716`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:42:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4f2c673dee7c01dead9d002b58f94f192dedcd8cb540af771a3e99076df2ae`  
		Last Modified: Tue, 13 Feb 2024 01:54:59 GMT  
		Size: 184.4 MB (184448080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8803cfa9be0301a6ac179d42ead5df09ce099585a8d3af82bc135a83b403e21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301405885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cde88f627e35b00c835f4ed62193ce13c65c97c5002b7741e4ae356ec2b9cc0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80088b70c07ea4625157344410c74a9f5aee9d7c29474b2a4353496defbfb5b1`  
		Last Modified: Tue, 13 Feb 2024 04:28:07 GMT  
		Size: 175.1 MB (175089000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3a1f628c5b65d19591d47e510fd56c43e103eeebf6fbe891397da18a7678fead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339684343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701f356a402fb855158c9f507c5043f953d84e1cfe645fd952668f57715d3f5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:38:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcabfc6c415bdafce0fb78b78afe51a8be789b05c4c3f5ccf5f1046bb5d32776`  
		Last Modified: Tue, 13 Feb 2024 01:47:24 GMT  
		Size: 202.5 MB (202519692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:75cdf1e75b5c0d85a316d078a374cbc929383d2a3ffc26d655786dd914d77f73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351499924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cd01f4c9df72780c2cc807cb245471bb21efd12d115b1687af42a18eca6c56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:19:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa04ac89e98e423a77743b83b547bbfed238c3f5c7c341959541005af241df49`  
		Last Modified: Tue, 13 Feb 2024 01:30:38 GMT  
		Size: 210.0 MB (210046749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fdfdb9bd1f480b2822305a8e8fca8bd401518d791ec9dd63660e798fcb4f60e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325869531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a4752654751c7693f8ce3207cb68b23715c1a73bbb6204e33f332632fbceb0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:51:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cedb7a3137759e51142758f8b7029dc78e57a3033813443144502d7ef4c020`  
		Last Modified: Tue, 13 Feb 2024 04:23:34 GMT  
		Size: 189.7 MB (189709673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bea1e0798704828403d6c7cb6a3b339cf5eb3bb029ff172b5be61bf585fb4d5e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362985389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590365a4815d6e17cfd6a4aeadd5cb54292d100096bbb709490dadeb8bf06460`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:23:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766a6e0e49a985c19ff5bed265467d9f1f6eada575066cf5a142c50bd88a57d`  
		Last Modified: Tue, 13 Feb 2024 07:37:13 GMT  
		Size: 214.2 MB (214151358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b79ddaa3322a2a9c7ecbccc12fe877e96794af1e9c3c76cddfedd37f7c722cf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318255163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d705af29279bf4338c1cfa62569d434d9a8d5c8ce7db7e15b91513dc85abf671`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:25:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef3f1a97bd13632e244781ae7503da3241b898fd89a42df192c290447f2cf03`  
		Last Modified: Tue, 13 Feb 2024 02:58:47 GMT  
		Size: 183.2 MB (183169094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:b5e504d3918d633d7ed04fce4cdbed4cbae55148cdbc58ef202ec693c1d8f0b4
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
$ docker pull buildpack-deps@sha256:71f969271cdbd16274234876785c2e276d8294aeb5d977b42aa83631f7684d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73599182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0aa610bb0fc1805c8cb5f5eba5f72a1c87aed088ea5c979c5eda30852c4514`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8a9bdc1a52ecbddda26ae35a9cc92b169bf05f3a06bffbdfb11cfa6feee08a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70036722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841f7172b5da0937e2db88203954c4184af0ca3c047129fd56a215e741f6ec3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ea690c06329fb428b4c350e3a936fc776641dbd292dea95644792d6450917c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67103937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf3b255e43b998fcb76ebb890056d1d75d577f00cb104ef631a5a99ec09dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a8a36d0aea4aac326643676b0219281617b83843b91154869b645ea24f34f9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bd33bdb130671b693e432fcf05cdd12d8531ea7cdee41f7f09e32b00c5dfd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c1100581a915bcad3c65d416ffa5c59f9c6791b8f7ed13a0d6458a162d9e669
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed05ae5df9ff35b46cdbf27e308cc5c8f0619b60a27b9b624f3682a6db147b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1eb12b7f00bf43b25969027e6f12677dfc58dad280fb933f580de8bc078d756f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a625c69e8c8ce460c71c8f5f00ef77fc19244edfa02315becfb08079afa69a21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4731c06396fd41e5380f3ddca1a02f78b4ac8b0d8146a2cca70323ebdb2337b4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f731a23661023501913e0d11c4da05333ebc54017ef0a8d5fac88af683fc803a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:25d3921209863ac81e2c3a9f89e054dac21c9999dc0f06980fcae587fe8d3d85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71959726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d37131e25319321b9b0612704137b0358484e6505251139244771e35c8bb71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:cdf130621a2dabec25c871f2f7c0a2a6249eee0f4d47c1cbb54b5e945b4e775d
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
$ docker pull buildpack-deps@sha256:fb5e878ec1dce3866ba1790e847f1e2a26a20f5dc847bbf9104f1bef0da7fb16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20f587594e57a8a88d79cb1afe4f962666bdd06f7a9c0ba33636724d9aa819c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5e7019261254418035af77dd442aaded3bd50f4de1a96870d4afa2bcfba2eb7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ac0eadd06c312ef3a2c044f5b46f099e5566136eb82c7d23de6a69e7376cf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:95923f973cf2f9e97e02a4131aa863ce5c250653a75bd73890dea3a6078a7beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed0c51c51c4a5dc12c8411b93f2f51ce9061f611b023b20589d29e13e5bf065`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f3b8888591ff7c3c5013181b8c438db8a849cb8ef8c5056953463f90836a44f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137164651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfa309b7928ccbb9ab1532b231841ac35c02e9e543f9f40793811a3bfccdf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:388d8b1f1f326bdba21772291704c24c93af8cd4551eacdf280bb29a4992644c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141453175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238a8e12c3f0469e141a977996ce5dda849e2a66e901149b745be538c37e747`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:07624084e774b4fa966627ae1efdcc05a78299cc645390e0d02981f3b1c820d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136159858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589fcf617f646e03d231a9c75cd7b2b8935071c2161639f341eaf8aab55432cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:12d1a1f3c60d59350f022eae19bdd24c04e1ca5f6f1d4a59bb6191fd11113bc0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a1365520d6a870826c979d1ae41072e965b7ccdd710879321b448476caaba4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41912604708dfd5334f32d83e6df641ecac0cefccd26dc4c0c55e4aa3ff17e84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135086069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129d9dfc6bce48b04c322295e7be11dbcbd47a8d8e0f0d8bd592b8875885a3e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:2b9d7ee09f795a9beb0434d09f93ec6683a6d25373c2f781e02406b20a75f84f
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
$ docker pull buildpack-deps@sha256:2ccf6b25b8566453f5f526fbd4c3831aa06a4bcbebd9493e84e09e3b4570117e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 MB (409750740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca6651cb595f48fdb562484fab92a2371fd14450365d10b7516be35283aa314`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:29:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e96ba6a4df5f9a034d0f042c6ba596296abfca3f619a6c6625bec56ca08f02`  
		Last Modified: Tue, 13 Feb 2024 01:35:16 GMT  
		Size: 66.5 MB (66454282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6861838beebbc0b557a6de8a7fb09bbccaf7158cf0c2b59348823b05fdd0d3`  
		Last Modified: Tue, 13 Feb 2024 01:35:58 GMT  
		Size: 264.1 MB (264114976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8c0cc9887ce02ed395a536f49065fe63711009cee94e2d79abca0ff517ce3ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 MB (373029590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c2092ce016bdf4f1cc7ccdd8be6788c7bc03de1cf3a39edf63ff83df0cbc97`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:52:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283ca3166ffd80ea83ab111c2390bc95b099bd6fd3a16ebb965559ad02fb483f`  
		Last Modified: Tue, 13 Feb 2024 01:58:33 GMT  
		Size: 64.1 MB (64096976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d901a84a069b82728e01139c65e037a1f75e08bcc5f823a2d09e12c1eac80f8`  
		Last Modified: Tue, 13 Feb 2024 01:59:25 GMT  
		Size: 234.3 MB (234271252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:50c56853720265f8e2acd24a2ff92edfa61464b24c24fbabf21e4ea355f57a3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350795607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701bc906a4b78e2b953eda9825c63a4b1714d5d65288578da74ab395410647e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:25:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8b8f779f6f6934c8df0f23fb560ca92edd571c516e89d73b9eb684de34c1c`  
		Last Modified: Tue, 13 Feb 2024 04:32:36 GMT  
		Size: 61.5 MB (61458710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e89653202d76bb2d2634ea10b87a6fd514cf8ff4b054a5c0dd35be5cdb217`  
		Last Modified: Tue, 13 Feb 2024 04:33:25 GMT  
		Size: 218.0 MB (218000349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b50632c5c3c1da541f198af067944b978fc3e86d09d6e5faf31f7cd7bec9f0dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397477302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb739bca9cfb606e2e4198c8b388fd60e62d0ba4c857851a82f722e1fc6b0d8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:45:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbc13be4438f9f8d894060aed3c33f0d7346f4270baeb1a88d2666d594e5e6`  
		Last Modified: Tue, 13 Feb 2024 01:50:38 GMT  
		Size: 66.6 MB (66561866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2f96767199297b5c9b62bfca3bf8dbe64f2140a3971075286c296b044f2327`  
		Last Modified: Tue, 13 Feb 2024 01:51:12 GMT  
		Size: 252.4 MB (252353725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6bea73c06e3551fc523afbb46a8a36107fb11a2b34ef71401204332062512d23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406188638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ce9d00a5d17f92dea63d4f7a5cc99f96b4ba99f43b734292e757b4c9618f48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e75a2a2fbea7b1fbd9bb0b804cd9b38871606c13ab1171e0718bc6b1bc3c64`  
		Last Modified: Tue, 13 Feb 2024 01:36:42 GMT  
		Size: 256.9 MB (256891738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c22bcdd2a316c671d589a3fe07524d1744d7ade31af60299293cbf3a5c8bae4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.0 MB (375990697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d59a8849bed4e04ab4c47dbe072e0ceed36418b0c03df31554d8c26da99371`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af89200b4b870fed00cbeab38968248af7ce012b97890ac09be125e872ee1`  
		Last Modified: Tue, 13 Feb 2024 04:31:59 GMT  
		Size: 65.3 MB (65254297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d879d1c67f3b1e5353b850642efde0180be4e1e5692e1198898cf9db2281efc9`  
		Last Modified: Tue, 13 Feb 2024 04:34:33 GMT  
		Size: 232.7 MB (232669218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8b34a14b0c2ae1541471d6a13d71985a6eab797c46a7e174e4223161dfdb6131
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420632790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90eb58e9c47c30ece9739b27b11b70332b25717bf0a3704a059b1167755ad37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:34:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb6585507457cd34ebcb56c4a04a3a14027e38412e2f405ef1023d35c26241b`  
		Last Modified: Tue, 13 Feb 2024 07:40:19 GMT  
		Size: 72.0 MB (71960573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd44839e24d4a0018783b0ea8b4c1b977cd0f28595e199fc923d26666c81cb1`  
		Last Modified: Tue, 13 Feb 2024 07:41:09 GMT  
		Size: 263.4 MB (263389958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c310e82d82b61bec72517f6521c1516a5f0e9af4a73795236c6b8da34f02e690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.6 MB (387584017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adccf6519ee2b291e9647181e80778e73c8b1e060050457922decfad33a075`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:40:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1bb14fde65edf4d3cc63eb384e2aad7fa969df7a3d75e3b18a18e361903aef`  
		Last Modified: Tue, 13 Feb 2024 03:01:01 GMT  
		Size: 67.6 MB (67554101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d349cd9c4812463a9aba9a6976074c9069725e39974b26a3ac27c6ea804c53`  
		Last Modified: Tue, 13 Feb 2024 03:01:35 GMT  
		Size: 240.6 MB (240633816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:6cc93f7d8e22296cef5afc6efe31a8e8aca20b6aced5522a38f75ec8348d2094
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
$ docker pull buildpack-deps@sha256:b5a2216ded3dfabaa523075f3d093e49651e32b4c676be578ce1d198001b5c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79181482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5f0ef64f6edce5c0b648e714f12badae93d6c4ff5495129213ff569d07e79d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cb5fe38f4490b648db7bf158240daf6d9d40487b626b23797b59fa5b4d5d0bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74661362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbc0c243b4960056c99e073bf90d93941e3aa0aba6beab2db3a5bfc0075e437`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bd0fef0c15b6b22976187497f5fc8e60c1cb6fe6ad8dd9a9826aff2ecc2a69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71336548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cca5fd674f71a9a0e4010da408509d4d06da6a66ee88cb1749dedb163009ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8edfed0a59efe2746108fe993e3841a05a2dba25b04ce5d0afaff3bd214cccbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78561711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabffe4ac529f15902cb12d90f74078b7b21696e1e32995ff069818041c1c63b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd0f8780a9e3a1427be04b729b628a6210f19daa6c147b10d71dd85511a17e52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cb4f729aa8bf435ec461964e478b611b67a629029a4e260fa8900bb4a8b6a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b384349ee873c845d6846cc9daf33f3b3862a129b50d3cca6417f92d632223cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78067182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f22cc52942ab8af399e083497fc46481bb88c01eb1c1a256f15e9bf165bd043`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:462a72ba0fb0509281ec48005feee8849237e75e97b4f9473c101c91c8b2b032
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85282259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40249fefed1d217df6b9b8c2575dbf6cdaf6e89168f22c2c96d4701e47c4e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff0d1a140bae51964725cb9471d5a971ecf74e35f74d3c64234763ef4b503fee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79396100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883211e70ad6032fefbbac2065bff44d3cc98bef3a1c14cfcf6c1d800e8a1f07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:1d5940636c1200f777940db4303fc1a16ea4c06befdeec7f4cd5fa5cf9296be2
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
$ docker pull buildpack-deps@sha256:a3fcacb276a237f179f61690e5dcf33fcae1cd25c9d66e28b5c273bba37c9737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145635764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1c0ac84dc2701c68aa9b881afc91e9a799e4038b2d8e2b53539ea03dd105c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e96ba6a4df5f9a034d0f042c6ba596296abfca3f619a6c6625bec56ca08f02`  
		Last Modified: Tue, 13 Feb 2024 01:35:16 GMT  
		Size: 66.5 MB (66454282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b838c3dc66a1a215063f98adf3d8e14768aa083ecda160e1a56919533aac4201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138758338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152fbe5a782479f6d405e1df9c69ab00418bcf8eef4beb82731fd5c35dcc575d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283ca3166ffd80ea83ab111c2390bc95b099bd6fd3a16ebb965559ad02fb483f`  
		Last Modified: Tue, 13 Feb 2024 01:58:33 GMT  
		Size: 64.1 MB (64096976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9916b4e4d28beb0ccf7c8da3e9126dc3f7cdb6be859659f29de26f717d285171
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132795258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcc0c57c5387e8ee87f425a5b5c418ee5b74927d02b6035d0f6ed30083107f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8b8f779f6f6934c8df0f23fb560ca92edd571c516e89d73b9eb684de34c1c`  
		Last Modified: Tue, 13 Feb 2024 04:32:36 GMT  
		Size: 61.5 MB (61458710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:72860f7e24a59e3a5327ffdda80ee0b9118a53789dbb50a2f53ccc6a0492e44a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145123577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac7ec8b348e610c9910071f8e26c3de4db6e8c345b8bbdc78c81547992faa4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbc13be4438f9f8d894060aed3c33f0d7346f4270baeb1a88d2666d594e5e6`  
		Last Modified: Tue, 13 Feb 2024 01:50:38 GMT  
		Size: 66.6 MB (66561866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ca387afdf0e91d05db41030b363b68a3df8bf459fa80447c8aaa0e92d6748c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149296900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01436b9ac474e17d8a06155260b7b95b4b6bcc35a0ad139578ccd2d36a12d94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8bc4f8dc524d8284e66aa0912fdab04075f18ca180a4cceca14b9cb16237f183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143321479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35309638f06a7ca72ae389aca8f405bf09710253cb995f985d34e77ea6a76921`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af89200b4b870fed00cbeab38968248af7ce012b97890ac09be125e872ee1`  
		Last Modified: Tue, 13 Feb 2024 04:31:59 GMT  
		Size: 65.3 MB (65254297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1bac2e40d971824d215b57156d6fe15725283aaa9d46c9bb806a202b733bc96b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157242832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a11a2db4798215fbbc73a947c8f61a0bf27b55429e6dc11f78a6370e3dedf07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb6585507457cd34ebcb56c4a04a3a14027e38412e2f405ef1023d35c26241b`  
		Last Modified: Tue, 13 Feb 2024 07:40:19 GMT  
		Size: 72.0 MB (71960573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4b88686067389882715870e2ba53aef7d41489aeecf6f097e49daae466bfbedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146950201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09ced20dd0f1590d7b05d51dd14a6d1ebf2fc4a502255d2e7080781bacb2c54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1bb14fde65edf4d3cc63eb384e2aad7fa969df7a3d75e3b18a18e361903aef`  
		Last Modified: Tue, 13 Feb 2024 03:01:01 GMT  
		Size: 67.6 MB (67554101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:2b9d7ee09f795a9beb0434d09f93ec6683a6d25373c2f781e02406b20a75f84f
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
$ docker pull buildpack-deps@sha256:2ccf6b25b8566453f5f526fbd4c3831aa06a4bcbebd9493e84e09e3b4570117e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 MB (409750740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca6651cb595f48fdb562484fab92a2371fd14450365d10b7516be35283aa314`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:29:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e96ba6a4df5f9a034d0f042c6ba596296abfca3f619a6c6625bec56ca08f02`  
		Last Modified: Tue, 13 Feb 2024 01:35:16 GMT  
		Size: 66.5 MB (66454282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6861838beebbc0b557a6de8a7fb09bbccaf7158cf0c2b59348823b05fdd0d3`  
		Last Modified: Tue, 13 Feb 2024 01:35:58 GMT  
		Size: 264.1 MB (264114976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8c0cc9887ce02ed395a536f49065fe63711009cee94e2d79abca0ff517ce3ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 MB (373029590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c2092ce016bdf4f1cc7ccdd8be6788c7bc03de1cf3a39edf63ff83df0cbc97`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:52:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283ca3166ffd80ea83ab111c2390bc95b099bd6fd3a16ebb965559ad02fb483f`  
		Last Modified: Tue, 13 Feb 2024 01:58:33 GMT  
		Size: 64.1 MB (64096976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d901a84a069b82728e01139c65e037a1f75e08bcc5f823a2d09e12c1eac80f8`  
		Last Modified: Tue, 13 Feb 2024 01:59:25 GMT  
		Size: 234.3 MB (234271252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:50c56853720265f8e2acd24a2ff92edfa61464b24c24fbabf21e4ea355f57a3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350795607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701bc906a4b78e2b953eda9825c63a4b1714d5d65288578da74ab395410647e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:25:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8b8f779f6f6934c8df0f23fb560ca92edd571c516e89d73b9eb684de34c1c`  
		Last Modified: Tue, 13 Feb 2024 04:32:36 GMT  
		Size: 61.5 MB (61458710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e89653202d76bb2d2634ea10b87a6fd514cf8ff4b054a5c0dd35be5cdb217`  
		Last Modified: Tue, 13 Feb 2024 04:33:25 GMT  
		Size: 218.0 MB (218000349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b50632c5c3c1da541f198af067944b978fc3e86d09d6e5faf31f7cd7bec9f0dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397477302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb739bca9cfb606e2e4198c8b388fd60e62d0ba4c857851a82f722e1fc6b0d8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:45:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbc13be4438f9f8d894060aed3c33f0d7346f4270baeb1a88d2666d594e5e6`  
		Last Modified: Tue, 13 Feb 2024 01:50:38 GMT  
		Size: 66.6 MB (66561866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2f96767199297b5c9b62bfca3bf8dbe64f2140a3971075286c296b044f2327`  
		Last Modified: Tue, 13 Feb 2024 01:51:12 GMT  
		Size: 252.4 MB (252353725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6bea73c06e3551fc523afbb46a8a36107fb11a2b34ef71401204332062512d23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406188638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ce9d00a5d17f92dea63d4f7a5cc99f96b4ba99f43b734292e757b4c9618f48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e75a2a2fbea7b1fbd9bb0b804cd9b38871606c13ab1171e0718bc6b1bc3c64`  
		Last Modified: Tue, 13 Feb 2024 01:36:42 GMT  
		Size: 256.9 MB (256891738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c22bcdd2a316c671d589a3fe07524d1744d7ade31af60299293cbf3a5c8bae4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.0 MB (375990697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d59a8849bed4e04ab4c47dbe072e0ceed36418b0c03df31554d8c26da99371`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af89200b4b870fed00cbeab38968248af7ce012b97890ac09be125e872ee1`  
		Last Modified: Tue, 13 Feb 2024 04:31:59 GMT  
		Size: 65.3 MB (65254297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d879d1c67f3b1e5353b850642efde0180be4e1e5692e1198898cf9db2281efc9`  
		Last Modified: Tue, 13 Feb 2024 04:34:33 GMT  
		Size: 232.7 MB (232669218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8b34a14b0c2ae1541471d6a13d71985a6eab797c46a7e174e4223161dfdb6131
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420632790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90eb58e9c47c30ece9739b27b11b70332b25717bf0a3704a059b1167755ad37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:34:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb6585507457cd34ebcb56c4a04a3a14027e38412e2f405ef1023d35c26241b`  
		Last Modified: Tue, 13 Feb 2024 07:40:19 GMT  
		Size: 72.0 MB (71960573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd44839e24d4a0018783b0ea8b4c1b977cd0f28595e199fc923d26666c81cb1`  
		Last Modified: Tue, 13 Feb 2024 07:41:09 GMT  
		Size: 263.4 MB (263389958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c310e82d82b61bec72517f6521c1516a5f0e9af4a73795236c6b8da34f02e690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.6 MB (387584017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adccf6519ee2b291e9647181e80778e73c8b1e060050457922decfad33a075`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:40:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1bb14fde65edf4d3cc63eb384e2aad7fa969df7a3d75e3b18a18e361903aef`  
		Last Modified: Tue, 13 Feb 2024 03:01:01 GMT  
		Size: 67.6 MB (67554101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d349cd9c4812463a9aba9a6976074c9069725e39974b26a3ac27c6ea804c53`  
		Last Modified: Tue, 13 Feb 2024 03:01:35 GMT  
		Size: 240.6 MB (240633816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:6cc93f7d8e22296cef5afc6efe31a8e8aca20b6aced5522a38f75ec8348d2094
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
$ docker pull buildpack-deps@sha256:b5a2216ded3dfabaa523075f3d093e49651e32b4c676be578ce1d198001b5c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79181482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5f0ef64f6edce5c0b648e714f12badae93d6c4ff5495129213ff569d07e79d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cb5fe38f4490b648db7bf158240daf6d9d40487b626b23797b59fa5b4d5d0bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74661362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbc0c243b4960056c99e073bf90d93941e3aa0aba6beab2db3a5bfc0075e437`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bd0fef0c15b6b22976187497f5fc8e60c1cb6fe6ad8dd9a9826aff2ecc2a69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71336548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cca5fd674f71a9a0e4010da408509d4d06da6a66ee88cb1749dedb163009ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8edfed0a59efe2746108fe993e3841a05a2dba25b04ce5d0afaff3bd214cccbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78561711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabffe4ac529f15902cb12d90f74078b7b21696e1e32995ff069818041c1c63b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd0f8780a9e3a1427be04b729b628a6210f19daa6c147b10d71dd85511a17e52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cb4f729aa8bf435ec461964e478b611b67a629029a4e260fa8900bb4a8b6a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b384349ee873c845d6846cc9daf33f3b3862a129b50d3cca6417f92d632223cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78067182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f22cc52942ab8af399e083497fc46481bb88c01eb1c1a256f15e9bf165bd043`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:462a72ba0fb0509281ec48005feee8849237e75e97b4f9473c101c91c8b2b032
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85282259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40249fefed1d217df6b9b8c2575dbf6cdaf6e89168f22c2c96d4701e47c4e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff0d1a140bae51964725cb9471d5a971ecf74e35f74d3c64234763ef4b503fee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79396100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883211e70ad6032fefbbac2065bff44d3cc98bef3a1c14cfcf6c1d800e8a1f07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:1d5940636c1200f777940db4303fc1a16ea4c06befdeec7f4cd5fa5cf9296be2
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
$ docker pull buildpack-deps@sha256:a3fcacb276a237f179f61690e5dcf33fcae1cd25c9d66e28b5c273bba37c9737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145635764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1c0ac84dc2701c68aa9b881afc91e9a799e4038b2d8e2b53539ea03dd105c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e96ba6a4df5f9a034d0f042c6ba596296abfca3f619a6c6625bec56ca08f02`  
		Last Modified: Tue, 13 Feb 2024 01:35:16 GMT  
		Size: 66.5 MB (66454282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b838c3dc66a1a215063f98adf3d8e14768aa083ecda160e1a56919533aac4201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138758338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152fbe5a782479f6d405e1df9c69ab00418bcf8eef4beb82731fd5c35dcc575d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283ca3166ffd80ea83ab111c2390bc95b099bd6fd3a16ebb965559ad02fb483f`  
		Last Modified: Tue, 13 Feb 2024 01:58:33 GMT  
		Size: 64.1 MB (64096976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9916b4e4d28beb0ccf7c8da3e9126dc3f7cdb6be859659f29de26f717d285171
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132795258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcc0c57c5387e8ee87f425a5b5c418ee5b74927d02b6035d0f6ed30083107f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8b8f779f6f6934c8df0f23fb560ca92edd571c516e89d73b9eb684de34c1c`  
		Last Modified: Tue, 13 Feb 2024 04:32:36 GMT  
		Size: 61.5 MB (61458710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:72860f7e24a59e3a5327ffdda80ee0b9118a53789dbb50a2f53ccc6a0492e44a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145123577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac7ec8b348e610c9910071f8e26c3de4db6e8c345b8bbdc78c81547992faa4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbc13be4438f9f8d894060aed3c33f0d7346f4270baeb1a88d2666d594e5e6`  
		Last Modified: Tue, 13 Feb 2024 01:50:38 GMT  
		Size: 66.6 MB (66561866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ca387afdf0e91d05db41030b363b68a3df8bf459fa80447c8aaa0e92d6748c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149296900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01436b9ac474e17d8a06155260b7b95b4b6bcc35a0ad139578ccd2d36a12d94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8bc4f8dc524d8284e66aa0912fdab04075f18ca180a4cceca14b9cb16237f183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143321479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35309638f06a7ca72ae389aca8f405bf09710253cb995f985d34e77ea6a76921`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af89200b4b870fed00cbeab38968248af7ce012b97890ac09be125e872ee1`  
		Last Modified: Tue, 13 Feb 2024 04:31:59 GMT  
		Size: 65.3 MB (65254297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1bac2e40d971824d215b57156d6fe15725283aaa9d46c9bb806a202b733bc96b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157242832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a11a2db4798215fbbc73a947c8f61a0bf27b55429e6dc11f78a6370e3dedf07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb6585507457cd34ebcb56c4a04a3a14027e38412e2f405ef1023d35c26241b`  
		Last Modified: Tue, 13 Feb 2024 07:40:19 GMT  
		Size: 72.0 MB (71960573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4b88686067389882715870e2ba53aef7d41489aeecf6f097e49daae466bfbedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146950201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09ced20dd0f1590d7b05d51dd14a6d1ebf2fc4a502255d2e7080781bacb2c54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1bb14fde65edf4d3cc63eb384e2aad7fa969df7a3d75e3b18a18e361903aef`  
		Last Modified: Tue, 13 Feb 2024 03:01:01 GMT  
		Size: 67.6 MB (67554101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:9ca794c4139f1f2fd668ad43db2b4ff778a1030a17c3a40e022e93e06394e9af
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
$ docker pull buildpack-deps@sha256:c5f624e22f63eab74ad44c949c411907e08323fd94f954dc217eabeb8a1086b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 MB (407116189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d209584b062cf0549b2080529ebf79610669da99af4644b934a2841095e3e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94778b4f8d542570a58f18b952aac258e2970cab96fd361b214bfa16118b00`  
		Last Modified: Tue, 13 Feb 2024 01:34:04 GMT  
		Size: 66.5 MB (66468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80def60bd73e3a9a5705eaecdbe842048e3d84a1c605e6fae357e8be7cf6e617`  
		Last Modified: Tue, 13 Feb 2024 01:34:45 GMT  
		Size: 264.1 MB (264140563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bcf7327d7f12ffc8a2a41a1f361e1cf6533d82877429896f0da0f01ae3fdc5bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370331989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41519ced967b01b112d200b16c18a1a11bc1f34d907ed1811981430e1eb64146`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:50:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7541155b76422a64edf910ec2131b609a880f2b83ac01ac06abd5cb73d5ee`  
		Last Modified: Tue, 13 Feb 2024 01:57:51 GMT  
		Size: 233.7 MB (233747841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8a188b1ac61aeeaf35024c340f52f63a0132ba4657889d2e9437aca5527433b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348778060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ad35eb2f1a3a5e5732ca672c9f3ce8c926a53741aa176c8e2fd0870378fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:22:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496516de4f431d258aba363886cad002ce4f57baeffcdf4e252ed7edd24c0f9`  
		Last Modified: Tue, 13 Feb 2024 04:31:58 GMT  
		Size: 218.0 MB (218020845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fa0f545d4430defd649acd3e14a5d481038bd7bcb00a39eca14e998bb2040b88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395048369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd48be5b1aae01f7999d77c7503552362d2ad656276c58aa8043f9387888794`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:42:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:43:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313a023dd2178b52531ace278aad9cfe2b7b237ef6b56c93424eefb6724d585`  
		Last Modified: Tue, 13 Feb 2024 01:49:39 GMT  
		Size: 66.6 MB (66566375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10eefeb9a7dd28dee992ba5b7e16f5b64a8d5549fb74ba8d4d7cf0c53c4dfe`  
		Last Modified: Tue, 13 Feb 2024 01:50:12 GMT  
		Size: 252.4 MB (252400519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:251fddb93de647e92e5db9520b50e234245592088d0ea64935cc2fc9cc92550f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403617689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e0fb16df1b72057c3fe1def6cc1a9b8c83fe2c54bd9320847a6a63ffc2d62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef40ea4fb0aaa505ca0fc627a4b7f559f54d7f3a06a621779b84c00fb13dc3d`  
		Last Modified: Tue, 13 Feb 2024 01:35:03 GMT  
		Size: 256.9 MB (256910908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b492a050d8bee6734d4e7fddf2b7dfc78e633a132a169b1e1700ee0a9229feb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (374000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35abde10cd1ddc508f26b152e3ed074e3faab5ae5a9689f6d148e8967c4806b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:10:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6328e06fb256ea30715aa4016628a9149817a5fd5af519caa1fc97eed490e251`  
		Last Modified: Tue, 13 Feb 2024 04:28:01 GMT  
		Size: 65.3 MB (65264661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0279072739c3e1a41c7935740d8cbb0cebb904baa4052f248b0c7367bbdcc76`  
		Last Modified: Tue, 13 Feb 2024 04:30:38 GMT  
		Size: 232.7 MB (232696791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cb959a6bb47eee2998308c197d3c0ca38ecc6b48e80abec53dd7ecb715a5c226
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417863444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbe3e9b6748ebc3010b3c56484c4abd26ff4e2995d92e0c772c765eda4038c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:31:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a5c8875e799e5e279fbdd05c6f1210fc9492749ce7709449def06189f5a739`  
		Last Modified: Tue, 13 Feb 2024 07:38:56 GMT  
		Size: 72.0 MB (71962170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa143fea443b5fbf9767fb081bf4a51c014002c74db280206fed9c76c7a2e6`  
		Last Modified: Tue, 13 Feb 2024 07:39:45 GMT  
		Size: 263.4 MB (263404095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:57831dfaf93e60466e60bb0361b71f5bef513395b770321bf8395f2126f28eac
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.7 MB (435678773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7161e3929956969d644f37455c71a73d206a7eb668a1eb5898c7287c8ee4e6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:40:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759b918e35db2dd593162c00a042bb80cc9bea4f8643a193ebb8f688356fa5d4`  
		Last Modified: Tue, 13 Feb 2024 01:42:44 GMT  
		Size: 65.7 MB (65714562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1c45ab68df68f5378f8164324aa1dad55295edf91785eebdc4ab678e13fa3`  
		Last Modified: Tue, 13 Feb 2024 01:48:38 GMT  
		Size: 295.6 MB (295606402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cbcf2b8c203819dcee64abf3e7c40fe72103115355dc0546c993a533fc14fe44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385275888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91997c3e812b362628e372aa2d09a9a6cf7ff77aa137b4fcba2a62a8754bf29f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d71e89930040fcd5c9bab43bc590b577afe0564c16033af772417a01da471`  
		Last Modified: Tue, 13 Feb 2024 02:59:57 GMT  
		Size: 67.6 MB (67555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4950bfd2260fcacae5cb79b071be191ad22b275987a43ed9ab875aea6929a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:36 GMT  
		Size: 240.7 MB (240670966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:8c74f4bb17335392329320c3e636203e880e20ad49656d32bdac0933452198bd
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
$ docker pull buildpack-deps@sha256:d1c743af9b2f43730e2f8d2a90966952e1c05d7eba867f064b254d425e63f787
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76507372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7e3baed9409d7c78f0e08ccd5994257277c2e71b13f26b332343359456f03a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b839041109743d570e5b781207c8b6dd0d83f7a02c1312c39b3abb5859206ead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72475557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0f7d477c9f33dfcd2679ea280f5c1a52efe266dd8936b0206e4796fc5b1727`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6b8be762fd7b820a830a3321642176df58972875bda564d8ab9992399b21a19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69289468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847f66994b4f16318f221a7a1e0bfc18624e296073c3f43d158ff2b83d9c8b0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:471947f5197058ebfb95666bd4796655232ffb21a10bbe66bfbf513c998d6c5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ed0f568e4e46400479da1e5ad8a697b7df7d49591b78efc93ef2fd2b0e9091`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5a308728d3b203f524e96e1e51691b47168168b7318136b03ff137e66eb6ee7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78457588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b0696be583a4588b82ce28f76fa3e2241256e439d3cf9a96e63c5314f54a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a4a8db675393ee92fe409ef196cc95ae2101616b16dcd567cbee927d7adacb37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eca413a639eeb7f89bb3aba1e73462639a1e199d4687fb37ade8e121335cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8ca8a63e9f98ec918b00dbfa0cbfb9e821cec7c7b9a7262e2ebfb57dbf86c5bb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82497179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add37801d447fd77e633588185ca27ec48e8f097c48c4bfc36b48bec7ba57b3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:05da3f23abd0d4fdbfd32e5862e58f132da411fbe7b4892ceb60ffcfc563174f
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74357809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb3bebb24086f8a3702016ae8531035dfdc9bbc785d2b5466db4bcd57ca1d2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3d8adea1bb07411818beb7059fe1c1f46540e6069549a17757b87bacba9eb7c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73e082015284c35b32815c0f3361322c3f497023955778b8843b6cde5ef827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:634a3e8d91bc4a5cb62bac2a3ab857376d21fce1f5815381c616682b28aa2807
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
$ docker pull buildpack-deps@sha256:0bb071c1266f203b2041ca93497a739fe9d4349b7c7853cff4887a81e059f022
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142975626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdde92020438ebe73f96a17fc7307a7b413d194374d50b71e68efb8a6944608b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94778b4f8d542570a58f18b952aac258e2970cab96fd361b214bfa16118b00`  
		Last Modified: Tue, 13 Feb 2024 01:34:04 GMT  
		Size: 66.5 MB (66468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1cec2114b9fbc4843b5cf0b9c8fbaa74c4b4b83edaefe5346dfc5a2325eb6d89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136584148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9fdbbebeb90640507c0fe9c9c7f94c49092e2b2457779acf670d041930ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:779fa01b9f5918a69716dbdf3d599dd12913476ec65cd9c5bc05a41183678baa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130757215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d298e5bd648d71e4c86864a1c66f3452d3e31f41781f27ee8a9c9d9a15fd7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4c705bda8f8f91e639cf3638fc33c9feb0ee0193c9dde109b78bbe6a45204325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142647850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd40f6dc2d9a57c3494b8c18be9c992dbdee27bbb8e85d2653ee05954ba2f66c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:42:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313a023dd2178b52531ace278aad9cfe2b7b237ef6b56c93424eefb6724d585`  
		Last Modified: Tue, 13 Feb 2024 01:49:39 GMT  
		Size: 66.6 MB (66566375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5c9106633d47775077bc4f62164c7fa00a7ee8d404348145e6f41c9cac5a2886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146706781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c92dfca00a5b2fbf2cb1672a258505f21b5cf25b37447b3e807b9f6c27863d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:351c91be38a50c74c25edc544bd502d4f74e3b6de4654e5aad3ea980b4281238
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141303459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e68e0576b452fb51c345c98058dda8777da05598f125487b7fa516a3863973`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6328e06fb256ea30715aa4016628a9149817a5fd5af519caa1fc97eed490e251`  
		Last Modified: Tue, 13 Feb 2024 04:28:01 GMT  
		Size: 65.3 MB (65264661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a6262101470d5f902e746a0fd115dc08a5bffd3790d17e56b29e2d14069a3ef
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154459349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abb73597e516d0a2f1196348483cff4c2caa8d87ebf42ad3cfea2b1ce78864a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a5c8875e799e5e279fbdd05c6f1210fc9492749ce7709449def06189f5a739`  
		Last Modified: Tue, 13 Feb 2024 07:38:56 GMT  
		Size: 72.0 MB (71962170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8cddfb384ed7eda6cf63effa0216f3b88205274484e895ec8d600f7a47555ec5
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140072371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af13fdd86228575c0423c9cc3a2a23c756cf4d2d71c5b4f8d912ea669bf54afe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759b918e35db2dd593162c00a042bb80cc9bea4f8643a193ebb8f688356fa5d4`  
		Last Modified: Tue, 13 Feb 2024 01:42:44 GMT  
		Size: 65.7 MB (65714562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cdcb147cf298be69685f44453fc0886d5b00156f2a176a5ebd4c3af96ee77356
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144604922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc10f37875adb45d677b6de292e99fb4740b93d3444cb3b8c0f9450701015d0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d71e89930040fcd5c9bab43bc590b577afe0564c16033af772417a01da471`  
		Last Modified: Tue, 13 Feb 2024 02:59:57 GMT  
		Size: 67.6 MB (67555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
