<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `buildpack-deps`

-	[`buildpack-deps:20.04`](#buildpack-deps2004)
-	[`buildpack-deps:20.04-curl`](#buildpack-deps2004-curl)
-	[`buildpack-deps:20.04-scm`](#buildpack-deps2004-scm)
-	[`buildpack-deps:22.04`](#buildpack-deps2204)
-	[`buildpack-deps:22.04-curl`](#buildpack-deps2204-curl)
-	[`buildpack-deps:22.04-scm`](#buildpack-deps2204-scm)
-	[`buildpack-deps:23.04`](#buildpack-deps2304)
-	[`buildpack-deps:23.04-curl`](#buildpack-deps2304-curl)
-	[`buildpack-deps:23.04-scm`](#buildpack-deps2304-scm)
-	[`buildpack-deps:23.10`](#buildpack-deps2310)
-	[`buildpack-deps:23.10-curl`](#buildpack-deps2310-curl)
-	[`buildpack-deps:23.10-scm`](#buildpack-deps2310-scm)
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
-	[`buildpack-deps:lunar`](#buildpack-depslunar)
-	[`buildpack-deps:lunar-curl`](#buildpack-depslunar-curl)
-	[`buildpack-deps:lunar-scm`](#buildpack-depslunar-scm)
-	[`buildpack-deps:mantic`](#buildpack-depsmantic)
-	[`buildpack-deps:mantic-curl`](#buildpack-depsmantic-curl)
-	[`buildpack-deps:mantic-scm`](#buildpack-depsmantic-scm)
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
$ docker pull buildpack-deps@sha256:2d2731a5b40d1d21c76fcb5c4b00f9e9bb32b01987b5fcc9082e694f43e9db02
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
$ docker pull buildpack-deps@sha256:49f0fe4b976ac043f12a62f04bfd8adae2a952319778afc169f86509c107cf54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245752201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bc6d1de5710d03053e857c3a5eacd2b279784a069ecd156b0bd9341560518d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:15:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c20b8fe2791b6e15ca0e0c8fea173a474ac8b32c473ecd8fa0dad8254c1e0a2`  
		Last Modified: Sat, 16 Dec 2023 11:19:27 GMT  
		Size: 60.9 MB (60905474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b523f8830fca8275613fc3047b1e22961f1a7a6c7587e0bb64efed53078c94f`  
		Last Modified: Sat, 16 Dec 2023 11:19:55 GMT  
		Size: 145.1 MB (145133108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ead267650cca2661fd3975f2167362411203145a6e0caaf11c64557ac9209966
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211975825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb9bc4d2d36893e22cbb00d98af36e0ae0eb65642ef2e2b049e0a438719d401`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:18:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:22:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c119a8724608a6685fa0b34a61b0823649b200614b0f28f8e95663a4767fa`  
		Last Modified: Sat, 16 Dec 2023 09:27:47 GMT  
		Size: 9.6 MB (9599966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8358ab0bcee36d3539fb9f170efecfa9df4f1e74fa2251adc49ac10ac74952`  
		Last Modified: Sat, 16 Dec 2023 09:28:08 GMT  
		Size: 55.8 MB (55826952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f013a6bc4ca4d255a23c1e63d1fdfb28fa00386a7ff938cb51c8be1534176f`  
		Last Modified: Sat, 16 Dec 2023 09:28:34 GMT  
		Size: 121.9 MB (121947935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5b69f8f962cd85a7ce6e1bc45af306a1b8f4a78f009745a3ba34dc3252b920d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235995417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d417a10a146a055d70ef31ad8691921cacc065dd0580ce1a37f90316339e5d82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:43:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:46:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380c4384112ff5756a21a782cb3e56349b2d988fff912c2e300f7b05d457489`  
		Last Modified: Sat, 16 Dec 2023 09:52:17 GMT  
		Size: 11.0 MB (10982154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0746ab73b10a8a0e12014132cb3aa809cd3d140bfd04313883a205e6865f3`  
		Last Modified: Sat, 16 Dec 2023 09:52:34 GMT  
		Size: 61.0 MB (61012651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b011d880a900a17a3579d4920a78e1db60f769ea5c1320c9d4c0d5ba13063133`  
		Last Modified: Sat, 16 Dec 2023 09:52:55 GMT  
		Size: 136.8 MB (136797468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9482ce99fa3db42f7a580b25fc815210a3e9c376af14fa20d1034a5aa905afd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269520442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff837df70e1e592c3481bafa0e7a896d708a20c3083fcd534544afa0c050c102`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24901584c9da8423a19466ec4f3fb08b243d7102f5729a448869330a71ddc72`  
		Last Modified: Sat, 16 Dec 2023 10:34:01 GMT  
		Size: 12.9 MB (12937872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa67c542474baed45a0213236f852bc5d88639a093406a5b6231182f0058379`  
		Last Modified: Sat, 16 Dec 2023 10:34:27 GMT  
		Size: 69.6 MB (69647829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da84586fa63993f70fe6085c9b15c047c6ab3f4972037446c59141b9f844da1`  
		Last Modified: Sat, 16 Dec 2023 10:35:01 GMT  
		Size: 153.6 MB (153620421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:26660628f08bf320b00ae56a23204adabd214fb2422d14c3e98266ee173376ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226566330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774b65bf1694731af3655d129bcde92acd24f67498241b439e97dcd041f8e42e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:36:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbf59c6d3812f9f521b9fdfa2e6419c4ca08ffe8c5b6274489f04617d3e472`  
		Last Modified: Sat, 16 Dec 2023 07:41:54 GMT  
		Size: 10.7 MB (10689243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedb8b7c21d705ae2098924b2fe7951f410607de309a9159dcdea4656aa56f2`  
		Last Modified: Sat, 16 Dec 2023 07:42:11 GMT  
		Size: 60.3 MB (60310872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068074ec6695840845bf59a1dd16020f9db21b42ba9fb2e6149fce2ba86301`  
		Last Modified: Sat, 16 Dec 2023 07:42:33 GMT  
		Size: 128.6 MB (128550581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:7673b9d081573366ee82451aeec4b93a51e984ff765a8ea4ba791e0ca1024ead
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
$ docker pull buildpack-deps@sha256:199296415be961c4de236bfaaedc28a5b636890f193be30a9d4f977fa2ac44e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39713619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4528a57e0a1e9bb08fb9517e7aaf0675082cc77c9ea4ccb2fd55e4f856a24f6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f9a69781583e135fb2aa2e2b0302ffa4ae705e49027921fec90d7288a3b8b2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34200938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00ceec0d98579d19143ec7f0196882bcc060b9db40c6202e7a5a69b5da37d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c119a8724608a6685fa0b34a61b0823649b200614b0f28f8e95663a4767fa`  
		Last Modified: Sat, 16 Dec 2023 09:27:47 GMT  
		Size: 9.6 MB (9599966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6efec07dc3a777004a46c0a8b2ed890cf7033f33429d330252bed280c0c97805
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38185298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc297c299b325e22a1633441633105ca79bf1298f61b9423a98cdacc7784a5c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380c4384112ff5756a21a782cb3e56349b2d988fff912c2e300f7b05d457489`  
		Last Modified: Sat, 16 Dec 2023 09:52:17 GMT  
		Size: 11.0 MB (10982154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ac8f8dd96bde4f8f4852b9a4fb8b175b5984523cda0c4d3338c4c0528e7d3ce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46252192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f822c88396dabb70cd5d79d2159d3af9403964f9d5f44bc0418880a7a80a2eb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24901584c9da8423a19466ec4f3fb08b243d7102f5729a448869330a71ddc72`  
		Last Modified: Sat, 16 Dec 2023 10:34:01 GMT  
		Size: 12.9 MB (12937872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c992346b2af6d0020b193b7ccab7200cf7f698304a8adcea18790b7943a598e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37704877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656c410fdb9477c3bfc25768bd1c0aeb364911339ae1a706cee91c71db42aaf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbf59c6d3812f9f521b9fdfa2e6419c4ca08ffe8c5b6274489f04617d3e472`  
		Last Modified: Sat, 16 Dec 2023 07:41:54 GMT  
		Size: 10.7 MB (10689243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:48abb2c0ef13a4b8fdbae1025ba09a1a35b2c42a94c3b56b916f01e124c9afcc
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
$ docker pull buildpack-deps@sha256:2f9f349caffb0f2ade36f793a86536457b2d1e90ecf0eae5a47e328cdd0209f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100619093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7eb0e22f5cdbc37401c41319e3d76937da1e13fea7145cd2f5b058e06101383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c20b8fe2791b6e15ca0e0c8fea173a474ac8b32c473ecd8fa0dad8254c1e0a2`  
		Last Modified: Sat, 16 Dec 2023 11:19:27 GMT  
		Size: 60.9 MB (60905474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c83bfb6ddd50d498ff2f8c5369ea9af0534c7efa1fb4e5f63ea82c6a485ca553
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90027890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec1117d1a21421464a86195d1999ee114972d08f566cbea3682acbec840b2bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:18:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c119a8724608a6685fa0b34a61b0823649b200614b0f28f8e95663a4767fa`  
		Last Modified: Sat, 16 Dec 2023 09:27:47 GMT  
		Size: 9.6 MB (9599966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8358ab0bcee36d3539fb9f170efecfa9df4f1e74fa2251adc49ac10ac74952`  
		Last Modified: Sat, 16 Dec 2023 09:28:08 GMT  
		Size: 55.8 MB (55826952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:21230d6ec8667eba155677ad4f989b2e8d3b048bc345195f2e02f3c08628676a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572ab89760ba6e8291b6220d9c957d164f60e4891e38efe948c041932b04048`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:43:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380c4384112ff5756a21a782cb3e56349b2d988fff912c2e300f7b05d457489`  
		Last Modified: Sat, 16 Dec 2023 09:52:17 GMT  
		Size: 11.0 MB (10982154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0746ab73b10a8a0e12014132cb3aa809cd3d140bfd04313883a205e6865f3`  
		Last Modified: Sat, 16 Dec 2023 09:52:34 GMT  
		Size: 61.0 MB (61012651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c01c302d76283ec69bb5f663be6eacfebecfab55ac8900ac24381c8356f4784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115900021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efaea0fdf20b37cf12e6ede5f231fb98a2f8ecfa4ce7d052adaae0fdf5d3b5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24901584c9da8423a19466ec4f3fb08b243d7102f5729a448869330a71ddc72`  
		Last Modified: Sat, 16 Dec 2023 10:34:01 GMT  
		Size: 12.9 MB (12937872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa67c542474baed45a0213236f852bc5d88639a093406a5b6231182f0058379`  
		Last Modified: Sat, 16 Dec 2023 10:34:27 GMT  
		Size: 69.6 MB (69647829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:45bd2d6a723b69f1b5725e152eb9c9408820ee88b83aebfeda2dbc762625a608
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98015749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91729fbd0e1d0d3131931af841fafbf382392b3ff7ed33224ccc7121923f8a65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbf59c6d3812f9f521b9fdfa2e6419c4ca08ffe8c5b6274489f04617d3e472`  
		Last Modified: Sat, 16 Dec 2023 07:41:54 GMT  
		Size: 10.7 MB (10689243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedb8b7c21d705ae2098924b2fe7951f410607de309a9159dcdea4656aa56f2`  
		Last Modified: Sat, 16 Dec 2023 07:42:11 GMT  
		Size: 60.3 MB (60310872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:49b793d37e8a36dc753be343944245ace0ecbbeea19e92f2e74f53667c980960
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
$ docker pull buildpack-deps@sha256:4e9ec861c92dd67153dc1df1bd320fa25fd939e3edbc1627f636519b2d851b3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250058059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc43e4dd19cacc4018557e4f8c1d8ba55c56fc8c97c81b0720e740798dfa60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:18:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f8a7d572599c1debd48a9a5385f70cedee3efa5a035ac4fadc034948979add`  
		Last Modified: Sat, 16 Dec 2023 11:20:04 GMT  
		Size: 7.1 MB (7120117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c652b51acaba2f62dbf9b6e6932913b693eedd3e57ff251e5faf8080d3c720`  
		Last Modified: Sat, 16 Dec 2023 11:20:17 GMT  
		Size: 39.4 MB (39449471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b478d7d46710e8853d12306efe80ce48c807b3231fdfc4f17520ff18c63a443`  
		Last Modified: Sat, 16 Dec 2023 11:20:47 GMT  
		Size: 173.0 MB (173041894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dbbe13206b85834b453ce8234781872bc06448ce9a0face06c2ff2e273e872da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217311039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c826fee543bf4eb2ba7846a7f1fadcca269ca35896fe5d84a95a2f385baba78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:23:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:26:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f504dab242e1422942a773ffdc9f64b32c4ad2f2f933ae11318503879f2a6ed`  
		Last Modified: Sat, 16 Dec 2023 09:29:01 GMT  
		Size: 42.2 MB (42242672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cf30da1b3ef01b4af8dd61ab5eb311b8e4be8efa96b653e046fd005abe5d76`  
		Last Modified: Sat, 16 Dec 2023 09:29:28 GMT  
		Size: 140.5 MB (140523941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6c844a32a7bd2bc6b3d66ab135dfd74a85950ec0be28ed880d876ee5c7be1d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241349528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79943c4510fbd7c8b1e9b5967046a394984f59a12f6322c98583c10f7c58c32c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:47:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:51:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc1bb4922c3e6d6889ba7d474f6494f842ea5c58240c316f57c7f5477fd654`  
		Last Modified: Sat, 16 Dec 2023 09:53:05 GMT  
		Size: 7.1 MB (7066930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeeca1d35896d142baf29e201ff724b2629edcdd13eb39f8626bf934688bfc5`  
		Last Modified: Sat, 16 Dec 2023 09:53:19 GMT  
		Size: 39.4 MB (39361768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a34d39413fa289767cabec02f0b6fc9c0307332135b7cff694bdb09f6792062`  
		Last Modified: Sat, 16 Dec 2023 09:53:43 GMT  
		Size: 166.5 MB (166520548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:63f7f73318401ff45d60e23d4abb79e81d894f0005640972adbfa81997e1cdf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271363680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b3cb0ea7d30ad6375a0b20a6ae1011fbdd767aef03c672cc9111e9a122fc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:32:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de72efc09d1753caaf8c6b7fe2a5c73ace22d3acbe741d516b394a3ea5da0e7`  
		Last Modified: Sat, 16 Dec 2023 10:35:11 GMT  
		Size: 8.3 MB (8251190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c62be8e399ad2464e4d6d9e85d6f386366fabde00e1827a575829ecdd9e0820`  
		Last Modified: Sat, 16 Dec 2023 10:35:34 GMT  
		Size: 43.8 MB (43757200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3944fbddc2f4c3d092e69c6d382062dbde8f011a9d284ad77536b555cb4f0d`  
		Last Modified: Sat, 16 Dec 2023 10:36:11 GMT  
		Size: 183.7 MB (183700003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e48724d5ab7c15d9b2ab747b567a8771ef0b1ccd2f847c686f702670f4a6cadc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223840565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7c392df462a791435348bbbecc0b095f301dad5056219b1757ba03f0c77614`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:40:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4f2f1a144ba324fd3d8f8de5743652dff50c6a1029fe9d13bde04a34e5203`  
		Last Modified: Sat, 16 Dec 2023 07:42:53 GMT  
		Size: 39.4 MB (39415933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f499214031851861cc142460636b031c9cf19c11f6bbfccd95d813ad58191cc`  
		Last Modified: Sat, 16 Dec 2023 07:43:16 GMT  
		Size: 148.7 MB (148735867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:a98b0fe24b763e73fdac95caae22fbbce42b08dc238f98f0ceecce9465202a53
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
$ docker pull buildpack-deps@sha256:52bcaf8ff7d06ef5401f07f8e0afbcae02869216a7267a1b3827653c9336a857
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37566694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94de21796f573d9a3a6af2d14b1689335758184c456a2919a7677b8da0bdfead`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f8a7d572599c1debd48a9a5385f70cedee3efa5a035ac4fadc034948979add`  
		Last Modified: Sat, 16 Dec 2023 11:20:04 GMT  
		Size: 7.1 MB (7120117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:794d4a7c2505b118312f0b87dbd096ed01125d71c276c00f626a6cb087563773
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34544426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caac03054dbe2534c96a94c560c11d194ad26437fd6aaea6527656ee740a454`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4bd34233799cf9e09842419611c3700369e4b6abf1dbc4e6dee20f7b3f626e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35467212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e091a057505270dabc7203764307dfa8202a1d26da917fc3ee31feb8f5af3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc1bb4922c3e6d6889ba7d474f6494f842ea5c58240c316f57c7f5477fd654`  
		Last Modified: Sat, 16 Dec 2023 09:53:05 GMT  
		Size: 7.1 MB (7066930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:27aab4c3f2c3715203f459b788bc649aa9a2cede8e02b6c8a222629c7832eda1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43906477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee396606e247688cf49ca59b3c75f1e703757667ffee897e0da10e561d078ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de72efc09d1753caaf8c6b7fe2a5c73ace22d3acbe741d516b394a3ea5da0e7`  
		Last Modified: Sat, 16 Dec 2023 10:35:11 GMT  
		Size: 8.3 MB (8251190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8e5c93e0a2b6f080ce22e8634f9458ba487d22ad6511a50cd58cd77e00ff3d6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35688765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259643b7037de2f7883fb2369c666a716b2e13ee6afa3a6966e9e1929de6425c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:55b10c49fb8ef41cfca4c4bf74883ebfb8d8cf1444ce5d7ad495ee2e496c28cd
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
$ docker pull buildpack-deps@sha256:8a371d947edabb4c20886bec14e4533511e36494d1fc5b85259d65ea91a3e2ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77016165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a6a6919eee790ae031bdc496c2497f76c71998df2103a2e2840912740f44e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f8a7d572599c1debd48a9a5385f70cedee3efa5a035ac4fadc034948979add`  
		Last Modified: Sat, 16 Dec 2023 11:20:04 GMT  
		Size: 7.1 MB (7120117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c652b51acaba2f62dbf9b6e6932913b693eedd3e57ff251e5faf8080d3c720`  
		Last Modified: Sat, 16 Dec 2023 11:20:17 GMT  
		Size: 39.4 MB (39449471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:38a1ff60aa9570a38f695a8307b23b02025fa13de8e57ccc02735bac9b13684b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76787098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06986ac37ff65f3803f0ea5173f1874910b9aecc18a4d81f09df321a75d0145d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:23:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f504dab242e1422942a773ffdc9f64b32c4ad2f2f933ae11318503879f2a6ed`  
		Last Modified: Sat, 16 Dec 2023 09:29:01 GMT  
		Size: 42.2 MB (42242672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4254c1144719e2605489be9bac32321d4ef182cfdcbc05c323a8316252b5ee57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74828980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadc8f4b91f9c77cd5b48b837983355c6ecd357d1e7c07eff67e3b2fbd176780`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:47:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc1bb4922c3e6d6889ba7d474f6494f842ea5c58240c316f57c7f5477fd654`  
		Last Modified: Sat, 16 Dec 2023 09:53:05 GMT  
		Size: 7.1 MB (7066930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeeca1d35896d142baf29e201ff724b2629edcdd13eb39f8626bf934688bfc5`  
		Last Modified: Sat, 16 Dec 2023 09:53:19 GMT  
		Size: 39.4 MB (39361768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b4387cc3c5f1d662269be84b7d4e1fb9e7b85add31e40adecd2e3b73ab6cb801
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87663677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98515b2ab08c9a83f764288ed55907398534d81830acddc1efc9cd925b37acbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de72efc09d1753caaf8c6b7fe2a5c73ace22d3acbe741d516b394a3ea5da0e7`  
		Last Modified: Sat, 16 Dec 2023 10:35:11 GMT  
		Size: 8.3 MB (8251190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c62be8e399ad2464e4d6d9e85d6f386366fabde00e1827a575829ecdd9e0820`  
		Last Modified: Sat, 16 Dec 2023 10:35:34 GMT  
		Size: 43.8 MB (43757200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0e42e21c35bb4b3bd4d859cb9b7dee5da8b81cf3405e2aa761e0a56468a5bc28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75104698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85ebc1388dfe0e77d7f13fe90e51ea5e5fe960c81fee08d7d956876cea8559c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4f2f1a144ba324fd3d8f8de5743652dff50c6a1029fe9d13bde04a34e5203`  
		Last Modified: Sat, 16 Dec 2023 07:42:53 GMT  
		Size: 39.4 MB (39415933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.04`

```console
$ docker pull buildpack-deps@sha256:c7d7d6c28531bd9639b523bf679ccbc5d9bfd0034f4873b793a9141e1b3eb28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7b21e65f1f87a4d40c1e08ece63cdcf6d5bbb8a4ce86d1be098f46806b6c0638
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268668481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf78db3ee5ca832b01afa6e1fea9e19e28684224ec976d52b0ebec060e81872`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:14:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:19:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cee0249186900006ed579d35166f58e4d6a442a4e9b66ccb46a0243e7373da`  
		Last Modified: Sat, 02 Dec 2023 04:29:21 GMT  
		Size: 44.4 MB (44397170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8603ddc2ff7a137d2e15fbd2cea7e7e2b50e6f759511ea19bab5bf68d63a0d56`  
		Last Modified: Sat, 02 Dec 2023 04:29:52 GMT  
		Size: 182.9 MB (182858840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9306d55146ab27ef6646d3fb352cbaf44b376a52f1ee3336fb7f892393a187e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232495724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cae9150824b11c935ce2ddb3ee4e9dbfcd621a84b9dd613e2bc722a65395994`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:42:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f87a80e6c43b6548cd5b0e643f892f2fc0720cc0e1d1ca6af5004e41a46d0`  
		Last Modified: Sat, 02 Dec 2023 06:50:46 GMT  
		Size: 48.7 MB (48676390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92698ff8c25dbec9fb4ed937cd5666cea12ebe98e9d3e017cee2bb065c4911a`  
		Last Modified: Sat, 02 Dec 2023 06:51:14 GMT  
		Size: 145.7 MB (145708660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:385cb697dad3e2ba56c6a20b1afc6c56667b65f5cbfed930582d38fb13e74da5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258195944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be66fd44876dc484b4d741834e27903c02c33084a21c89ef0d518a54facc3395`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:21:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6fb536587f5b74e79c018e8e0ebffe9a2c75df578ac81ccc61a03df3accf1b`  
		Last Modified: Sat, 02 Dec 2023 05:28:44 GMT  
		Size: 44.2 MB (44238010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4868cd226407813b998f896a42c2220e514a98c0eefaeb601337750598dbe8e`  
		Last Modified: Sat, 02 Dec 2023 05:29:10 GMT  
		Size: 173.6 MB (173596864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28b94bcee4a8cb055fed2423c4a5f5eed3bddb44d642562ed919eaa94d1f61be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293032704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1edb88229280a5ee9a9bfda500be2f459fbd94de6047b1582af4c3337d92f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:39:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42ca5f151bb20d6c7b51d59876dbd19d36051f90cb24bcc0222c799a32797e9`  
		Last Modified: Sat, 02 Dec 2023 04:50:37 GMT  
		Size: 49.1 MB (49095383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bebcb056e42972476a4e6cafb3b1846641913ba2688e69054d94d3fb54cc81`  
		Last Modified: Sat, 02 Dec 2023 04:51:15 GMT  
		Size: 196.2 MB (196192278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b483a2f9d145d2d9002f37a70f79889cfd1a416c07d602971819654dff2abde5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240238066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94723dc8eb8f69ded807e3081249547013b685b7ea457bfe13797ded1fa219db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:06:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:08:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81554de0a0b21fe0679e6e99ecca0110eb2f9aa31f580f3d3e5d1b613737bbfc`  
		Last Modified: Sat, 02 Dec 2023 06:15:07 GMT  
		Size: 44.3 MB (44269164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21b029899d618b899a5bcf09c8f047e53df0420b01963eed2629239c9c37fbb`  
		Last Modified: Sat, 02 Dec 2023 06:15:33 GMT  
		Size: 155.7 MB (155723369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.04-curl`

```console
$ docker pull buildpack-deps@sha256:529bef561ae8a198f9a0dc1f909a993a5f9cf3c8f3380dde7b7e780724c9419b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:35625ee9cb8bdb3736140d7bed8927c84ff7864fe22ad4e3862ad13f73183b2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41412471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3709cf8f8ea250fe64cda5451abaaabf8deed4ed356c5486b539a22bd49a4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0c960bf8fe85e3de325c6286655e0f0e4843462352d762744571ca4413cb3a74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38110674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dfc5354e2f27ef3aeec4e772fbddb68c3548ed79058e2e8b458663a165c1b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:850b5d8601434b851402a02d2ca745d1f54c092dcfda8c4b477eae3f11eb6a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40361070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682085e559812c18bf38779ad53974fa00af4526a3687b71c8c0f918f510072b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a0e775a0e8aefa89fe4a614f5e4160606ac9169daa9fe6420cd24e234be3ca00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24f363699741030eaad8a4735f5035cbd186d20ce147a91e10b12379dd19b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dc7b59511df9c0e21dea14d09d9b12caae9b68fe771f5946d0433776a6d453cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40245533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b48c45599caba4ecb590cab8765de0bc6cede721952ab762c574728a32180a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.04-scm`

```console
$ docker pull buildpack-deps@sha256:8ff52549b29abd6fe2a6875d9cdfdc0a36434d45dfd420eee2d8cebd3338ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a4db1988a45960358fe344b3dd1706eb1378473e437187704aa4f0a9cc1f8ddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85809641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22511557ee0335085870fa236d32414b23f74e17bcc90dea2f56437d43f05672`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:14:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cee0249186900006ed579d35166f58e4d6a442a4e9b66ccb46a0243e7373da`  
		Last Modified: Sat, 02 Dec 2023 04:29:21 GMT  
		Size: 44.4 MB (44397170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fd63f5636aa03062899bc9a817b28b3646e702d5786120addf1052dd4d43a8cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86787064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5834b475edf594d4f57be97e2ea1e8cdbcd6a332194968f8ef09cd2469fbd1c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f87a80e6c43b6548cd5b0e643f892f2fc0720cc0e1d1ca6af5004e41a46d0`  
		Last Modified: Sat, 02 Dec 2023 06:50:46 GMT  
		Size: 48.7 MB (48676390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5208247a6a4aff72f60895a92f041d9afa3e52b280d94fd41b6c1ae182a8949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84599080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf32e027c36186e2f14c18da71be0e0aac6a2da16c77e591bdcacd8114441be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6fb536587f5b74e79c018e8e0ebffe9a2c75df578ac81ccc61a03df3accf1b`  
		Last Modified: Sat, 02 Dec 2023 05:28:44 GMT  
		Size: 44.2 MB (44238010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3f8d2d702a8d32d5ded0aee43f819fee8cc4afccdff55176e33865aec97dd462
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96840426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c692f5d3fc7325f389b2f39efd3b9c3c80dfda067e432769ba157cf4baf60ead`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42ca5f151bb20d6c7b51d59876dbd19d36051f90cb24bcc0222c799a32797e9`  
		Last Modified: Sat, 02 Dec 2023 04:50:37 GMT  
		Size: 49.1 MB (49095383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f62a41cb0e8eb2aaad22d208540d4fe09c2baf81142123136a786d7ee963770b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84514697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee9e70705122eba45793e0a1f619cc0570e8a5520d6dd5664eafd45cda6a870`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:06:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81554de0a0b21fe0679e6e99ecca0110eb2f9aa31f580f3d3e5d1b613737bbfc`  
		Last Modified: Sat, 02 Dec 2023 06:15:07 GMT  
		Size: 44.3 MB (44269164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10`

```console
$ docker pull buildpack-deps@sha256:bda82b5ce4abbfcca5aa613c7b4eefa7244fdaa78274a1257ce3fed7c7b468aa
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
$ docker pull buildpack-deps@sha256:e1640709591c9d9e0038347965dec617f717cceec03895d42666cfbaea33545c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279758764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfef5d2082eaa961e2d3cefef8e67a7d13c9269c329297040dd1ca2d2360b92f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:26:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760243c1a983844f069a293b501cd9301cbd819c4fb9551cc389ff6e1e7cb238`  
		Last Modified: Sat, 02 Dec 2023 04:30:20 GMT  
		Size: 44.8 MB (44753276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938a8634af1b782bcdc4d1714f961d7e4beb6bf923b888e9ff9db9a53165adf`  
		Last Modified: Sat, 02 Dec 2023 04:30:54 GMT  
		Size: 197.0 MB (197026602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b6a8197e03c16a5e5c64bfe05fb54494947096f94b9d8aac266320b571278e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246704690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb114e88bdc70517c782d36daab42fa65b90488add07631546f47e8c48d2b46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:46:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3624564a762546bdc52895b1c66bc1408260d1efaa2e2b2b765adadd9c8f8`  
		Last Modified: Sat, 02 Dec 2023 06:51:41 GMT  
		Size: 48.9 MB (48942472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aeb74102316977bd7618d2394b9a9b8f7871ce0db4fa7f72ff72287befbde4`  
		Last Modified: Sat, 02 Dec 2023 06:52:11 GMT  
		Size: 162.6 MB (162594872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d62de9add5227d3e50479035c3a5c90546bf4eb61de363dc77bbf7c5630518a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271776124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6002b7cadfd93e9864d95610be91fd2b4e31e9530491ec54797bf44df2f7a49f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:23:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:25:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3c268c4f8b402b3f9907fba74a035e04caa79bd82292e937192630e4a7e64e`  
		Last Modified: Sat, 02 Dec 2023 05:29:35 GMT  
		Size: 44.7 MB (44665066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282eba19e4b5f40a7947b90ee497e8544dd23f1b54758d9068e3352ce8847e32`  
		Last Modified: Sat, 02 Dec 2023 05:30:03 GMT  
		Size: 190.1 MB (190109195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4d837a54ed79c3697e81fe74410d427abcc9ebfde406fe98a1aed32710212ac1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293583524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbf6c27960d11c3cacd25fa84f3c4a28ccd7e42d8b3b888bdbff7212085aed7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:41:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:46:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c14fb2f649d6e1f2a6ecdb5517e059449e766f72791aa8c47aa868b20d52f1`  
		Last Modified: Sat, 02 Dec 2023 04:51:47 GMT  
		Size: 49.5 MB (49544508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7b8396201f82cfdb61aa43db57c73838c2ee3354bbba5efa522ec63f8a82ed`  
		Last Modified: Sat, 02 Dec 2023 04:52:25 GMT  
		Size: 200.1 MB (200126675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eabf406ea7248077acda817b048130604c4d31ca60b0de1626699a3e2eb097cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257648877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6ba5eec539c6ac927968b4411466cd495be79e29749d9cdb335895cc3fcab7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:09:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:12:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5727db7a5897b08af6f62472ddfb225235a5740723521606d98d708b40b5b5c`  
		Last Modified: Sat, 02 Dec 2023 06:15:55 GMT  
		Size: 45.2 MB (45237357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924da814eb1bd8f1adf34e963bb6011fa2589858be016a1a9960442bf68fcc2f`  
		Last Modified: Sat, 02 Dec 2023 06:16:22 GMT  
		Size: 175.1 MB (175070849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-curl`

```console
$ docker pull buildpack-deps@sha256:da38651b553d6f5be98ccc7c042b76d9065954276b7ae53d9d8e22ea79b5333e
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
$ docker pull buildpack-deps@sha256:c6f602b7643df9f295b45b95bfb4be8dfa85b98b94dd4e280809748a07d3dc36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37978886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c449b2867d49805ee4b096b0a3444aafcb711d7e3543e906c551acfb15076`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3541766b77a9d7cddffe0f683ba3de91d803ac8d96ba7997383ea11960f2645f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35167346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cf56efa7a77d4c21597de504086e09392aa92b2c6580e1188183c766fb4102`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f6f179f365fa65e5ffd520b13c82e630a1096364c6d85ff06d1d8444e51d8531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37001863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e4dd9aa8816d78892e82986f2cd6bf118375327fea8790e2fd05ae9d46879d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:04a3cc193a0eceb4125d729128dd4d0f0bb1b8a47085e1e23edf8f7d56da9b0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43912341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8991fd5c6982603f7891b53566d2c7e1439126fa3cdf93b211adbff3f17bc315`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0345da18bdf37949faa61a968b9bba8f243aff91193d4a73935b406a9330bb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37340671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e272dd5d4ca4e107463f2bcc1f447f7c851b09a44fe6729d35ae0140f60f90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.10-scm`

```console
$ docker pull buildpack-deps@sha256:9c75924264f5ce4613ed1c74d6a1357e26212f4fb7d0bee3c7cd3dcde041e181
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
$ docker pull buildpack-deps@sha256:c7e495a12a1464b2f7a02eda48b5aaaafe94d24645bb7352d2d86eb107bac600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3da1fd7d5dc4e9975002d36007814c5c3077c22612c43346ed3266b6f55ad2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760243c1a983844f069a293b501cd9301cbd819c4fb9551cc389ff6e1e7cb238`  
		Last Modified: Sat, 02 Dec 2023 04:30:20 GMT  
		Size: 44.8 MB (44753276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0302aaedd3bab6cff8ac153d9ee30bb8b87df3a1aa0768d28cf2b67929653a76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84109818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b260ff917b448a207bc835791aafc586e4f773f48b4238d9e927ada3c5ad598`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3624564a762546bdc52895b1c66bc1408260d1efaa2e2b2b765adadd9c8f8`  
		Last Modified: Sat, 02 Dec 2023 06:51:41 GMT  
		Size: 48.9 MB (48942472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:343eb645cde6e6956c8b7164ed9d042a1e49174872fb13a4ba23d2c8c6b41235
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81666929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d83d40fc9df2bc35558833212c0763dfb4db7db07263e0ddf7cd02316790ced`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:23:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3c268c4f8b402b3f9907fba74a035e04caa79bd82292e937192630e4a7e64e`  
		Last Modified: Sat, 02 Dec 2023 05:29:35 GMT  
		Size: 44.7 MB (44665066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e3dc8db0d9983ef98c6265650ef17b378e2e0fb0dc4df96cd6e6e6e23d2fa73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93456849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975a408a5e5596adcff48d38f73cf3ecffd1da203fe40d0444a14a5270af9278`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:41:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c14fb2f649d6e1f2a6ecdb5517e059449e766f72791aa8c47aa868b20d52f1`  
		Last Modified: Sat, 02 Dec 2023 04:51:47 GMT  
		Size: 49.5 MB (49544508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:186933f2e2cc721e6fff568a413d0303f4a87bcd36cc143b64adeb1ba51f73bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82578028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3d6fb80611ed2c14a1f255df327a9462516576473e64c3024844b15eccd4ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:09:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5727db7a5897b08af6f62472ddfb225235a5740723521606d98d708b40b5b5c`  
		Last Modified: Sat, 02 Dec 2023 06:15:55 GMT  
		Size: 45.2 MB (45237357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:06ecaa5b0816973ff3754ed13b53143817b5c0496aa31c2abeb1d93bee9bd92d
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
$ docker pull buildpack-deps@sha256:cab48bf340039495180cbca35d871f443db57ec9d532cfe3e3a8ab6639d53cc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348837034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d791bc1cb1f6c7c46712226d0be47fb831eaad91261f02e43658860c5ddd14a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43bd898d5fbe0e1606380820047fd1e8b421722c9e69ac12757474305bd6702`  
		Last Modified: Tue, 19 Dec 2023 04:42:04 GMT  
		Size: 211.1 MB (211097790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a8cc47c1663b1b036c8bf86e0ff4c0b53743221e050d8adb5d7f5cebc6dd1925
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315969673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f57754b027a778fc62c44ad7ae37f75c346b214449818bac406b2e887d60fd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:23:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5ddaed1389aec60f80faad6640540555cb8a57f3acbc1566f210c60f5773d9`  
		Last Modified: Tue, 19 Dec 2023 05:32:27 GMT  
		Size: 184.4 MB (184416924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a815ad278fe7dc89833dd6a7b684532b6057cac1767b962afa4983575aa1f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301446383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b5e278b9d73862aec6702c3e56e8b857bf8a19cb6e66bcde7eeb68d5063df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85053a74f42624bfc14f242a6031c07b0852c368395192d70b48f596e4d153c`  
		Last Modified: Tue, 21 Nov 2023 14:14:16 GMT  
		Size: 59.3 MB (59266480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb946cf4e2606f2c7964d891cd5bd5f657448a82b430e9b2cf898f85bebd20c`  
		Last Modified: Tue, 21 Nov 2023 14:14:53 GMT  
		Size: 175.0 MB (175047915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf8885d05e431485082a33c2677686253af6bcf2dcbdc0eb3b3c83d373b3151f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339641326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ca1f96b92da15e8cb6b0264f9e7d9b036c94064f8dd766058fd40e112908a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:58:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95089c600b361807380090316c250b0b8eaf4fa2175b11ac8f49bb7581c61125`  
		Last Modified: Tue, 21 Nov 2023 08:06:50 GMT  
		Size: 202.4 MB (202449525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:41348688de89e48544adfc8884c24a7641235850d399948843d4ee5a548a8a13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351472342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2401a98522a5b225355bc86da6eb9157f7e0da556a31222d528e53437f47ccc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:26:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0d6b307a56e19161f69c60eb7c94378540e6b20f49d8b1039becdeb53cdde5`  
		Last Modified: Tue, 19 Dec 2023 03:37:24 GMT  
		Size: 210.0 MB (210025484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:09903ccf65ed5d5f71dadb8d8326f7fd50d5ef3c4bbef73440f0ee7d81b1bbc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325827014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f31fea6bf40650e456044ad189ce02c1a40169cce4e7b84e3ec9445d3fb39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:57:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d627909a3ff9de03889850fa5e83ecd71d896b3c313a14fb5c6e9915cc9b62e6`  
		Last Modified: Tue, 19 Dec 2023 03:21:51 GMT  
		Size: 189.7 MB (189684223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff34a667d81db5798aaf33085e09a789e13a45e7b48e804c87809631102b0ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362952942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b6ecc5afbeef5b86b674ec0993915e6bb01b89f9c44f901050856f10a1bf0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a54ea75827017eaea7b7055d8fca97c313c72d7a237502105b83ab018bd5ad`  
		Last Modified: Tue, 21 Nov 2023 07:07:08 GMT  
		Size: 69.6 MB (69584187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e986f224599c525ac40be9636489d408b4daff891bb3567a7986f6ae5c817cc1`  
		Last Modified: Tue, 21 Nov 2023 07:07:49 GMT  
		Size: 214.1 MB (214094151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d1822d31d3c58472a93084eaa39396b37585eb538479e3ca57d5e2e50d7470c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.2 MB (318217378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dcda8469adc1e80e5b8779671680724ff22c47c0c87e7d0658d100902caa19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c99a00cc05c2b6ae13b5a9c1b8997b9915ab687454a9fcd00d485bbb2d9a5d`  
		Last Modified: Tue, 21 Nov 2023 06:16:33 GMT  
		Size: 63.1 MB (63132875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cf7e37f4b53af6dfd3bdea89a2078a221738e8eeade3f46428f3def3e4c97c`  
		Last Modified: Tue, 21 Nov 2023 06:17:01 GMT  
		Size: 183.1 MB (183096415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:920f9226523d7a3ff92b78096f94f13c418345e1102e2e4f24d144aac6906531
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
$ docker pull buildpack-deps@sha256:cda8ec97c57294a6ceea1ae08c6af7dde37538d69753575aab2f1176d7bbd014
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73607702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87bac02476a0657252b47c4e4d6e60f121745c8c0c7e48a0101e4a2c1b85333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:390f50a032923f246d5a5df336203e186a8e7172b92d0aa8eae7b7929a7dd369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70043879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8fc90fd2b8868771734a3c47d342dda49fa8df68657aa64e0482b50cdd3b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ec7e94e60582861838948e4ca3f4913d5cea61af7cc8c9f1d6686387082a6a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67131988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357880f61f3530c27c69c6693c30200854440034160cb3835bb44ee35c62bc51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:889ca82473cf4a98c425f8c9039a68b8b94e14b5cfd091ca5a3d13744bb3d23f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd0a05de4ae3c58150f70b4783f7e41beb77eb181ee286d4cee9d931fb037b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af799b89d3e04d76c2b38183417363b6e95e8237850de2493bb01dec150a2667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75465937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bafaf5619993ee37dd6ffbfb62531b24a142a5c802cf6c744d3592d037aecc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6ff6fba6f20b86b8b0e8c20fb83dec2fdf5d16f69ce9d27fe7adc2a32f4ae8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bd8ac63c464f8fbe3346a160c6616fbb3d38c75666d3af63234ae420b5ce4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:784282fea3a27c11b3c8668acf83fdf5fa1f805e2c648264766bd6bedda9f057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79274604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927ae87f00aa3f0f3b5f1fccbc2848eda2dec7b3d1754259fdd0af08c5485cf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:56dea1f8a449f195ffdd426569472adfdcbb657344ea182789923be11c8b79f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3cde7adf1be7b7277ab9b2cd62cc5ea051cb781184b34e1645be1f946290f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:1cbc77f04c5facaecfeda50d61d2636f35f49161e26f7e89ab0d177e964a96f2
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
$ docker pull buildpack-deps@sha256:a3fba8caf6509c5246a424e170457c0fa67a654b8cf3b9adb7ebdb32d6e55dd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74c65587a9edbcf9a75606c9753bbc489d003c39838e299fa593e655bd31766`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fe46ac679ff949d5099a4d5e3c4846bf93801df8852f569d4b98acd702804616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2830d417ae6fd93ea6f902e7c515936f50e33ddd54431596e33dbad425026`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0531a6dee1ec00ac6c4467943728d8df874a0db45976e6717b6f6bb7d625c3f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126398468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e6f0f26595e7d2f41e4027ddcb1a44e10b203994b8a19e47b7c02bb2905c48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85053a74f42624bfc14f242a6031c07b0852c368395192d70b48f596e4d153c`  
		Last Modified: Tue, 21 Nov 2023 14:14:16 GMT  
		Size: 59.3 MB (59266480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce0af9ba6e5a5840c7fbbe85a3ac5d2f028a84167b274095b85e353c37996b56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137191801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6117910a955cc657572894f9d7fcfe8b0e051e427abaa349776e641b089c6b4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:07139c0b1ab111539ee39037d7176130c6e8c7bd2f8a0c0c25d5eb0841358089
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141446858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ddd0f8763eba9ac84fc03f15e7e4ed7b7555c3f1b2617c15c0ef31fb6d1451`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f6bc94392d10b737484515c04dcc61b2c129c94735217591ea4ad865b35098ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136142791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa001887bc8f8fc436a8584002635ae26f975a75d402283a48799fc0a478e53d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad518e13047a2bffa7358d6ed80141ee89918b12549d94563fe33dfe97693f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148858791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1afccc4310e63668ea2fa68e7ed2114f91aa1c4023a673f0dbd3cb0d533ddd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a54ea75827017eaea7b7055d8fca97c313c72d7a237502105b83ab018bd5ad`  
		Last Modified: Tue, 21 Nov 2023 07:07:08 GMT  
		Size: 69.6 MB (69584187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a1788f5a7099541c5a0691f88050070dd6e2d5f4b0c97777b19ed32f799c64e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135120963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2372afa7eb1de18c0332fe8e706503fe4a85393e04c4f9b30e3689e074ea3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c99a00cc05c2b6ae13b5a9c1b8997b9915ab687454a9fcd00d485bbb2d9a5d`  
		Last Modified: Tue, 21 Nov 2023 06:16:33 GMT  
		Size: 63.1 MB (63132875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:379b7a278c2c0bd77484f30e960362980bb739a2d40325f8c5380a9d5678e79f
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
$ docker pull buildpack-deps@sha256:b81ac95e1cbe6774145a8c46c70798f3abada991aed19e74c711a667d06c313b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322298176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693a3b0e9f0beeb137d71fd998420f2ed5e4a873f1a925b166fd73d9d8c67d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:34:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e04794082b8082ce8c158a02cb11d1d737d6c0cd1542062514b3e2a93f6c70`  
		Last Modified: Tue, 19 Dec 2023 04:43:04 GMT  
		Size: 196.9 MB (196880584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a1ebfbfcc336a9f01d4cff2524309fd8b64f24d077436c9cad5856b4ddc8bc0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295368190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e3414d217203458c81aff1b8ea98e2b097fdf45f0356f282ec5876d5f2815`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:24:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:25:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d33e8d4b6c3b1604296a932879e7916cac6072efd2b9383ab5b5cad23e3a50f`  
		Last Modified: Tue, 19 Dec 2023 05:32:57 GMT  
		Size: 52.3 MB (52331706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4500a3ccfba84ad29d6a187a1df58375b465c6b72d771c80b4ba92087ef6a90`  
		Last Modified: Tue, 19 Dec 2023 05:33:31 GMT  
		Size: 175.1 MB (175098185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:281c2e7852166ddfeddf3eeb4e89583bbae350d41b7e8343ff9e31371aa3122b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282799881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e319e2640284bad2c1d9d24bd03f403a9619d08ff70efbb26f940147ba97a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:06:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eecaf32e1cec433a3782e292748fa035da5e777baaf4ac1861fa6524865c86`  
		Last Modified: Tue, 21 Nov 2023 14:15:27 GMT  
		Size: 50.4 MB (50353119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7849827a6023dc0eb89664b4bbcb1022abfed00e52a6656cf5c7d397bf3fc7`  
		Last Modified: Tue, 21 Nov 2023 14:15:57 GMT  
		Size: 167.4 MB (167351454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf1e855f9c67ff4a7db063750a11952d01ed274933c1f6ed704bf85a3f2c4b19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313958448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180f08699a0077d6aef1bbb77ab77e3696234930f168750b984377131dac7299`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe2c38c6b934d9d3107cc7ce50d9e852c8ccef92d5cbc324a6f083b5aef0d1`  
		Last Modified: Tue, 21 Nov 2023 08:07:42 GMT  
		Size: 189.8 MB (189800334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d2daaa23b6589fe5fa4ad0819ac5ff9897ea02be04e946b5de89bb38ff76d577
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328049320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8d2042afa39d811a9b7f8c7987284473a9820285c3cf850a40238dfc0b2f9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:28:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a344c33a496f0c80e861246ac1b15db106b888d28c7bb89d17b87d06a5f1abc`  
		Last Modified: Tue, 19 Dec 2023 03:37:57 GMT  
		Size: 55.9 MB (55937182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb89bdf92d460c8b83c3effc827149c832709e4d9e4e2262456e267a2e4decf`  
		Last Modified: Tue, 19 Dec 2023 03:38:42 GMT  
		Size: 199.8 MB (199796881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:88c6ced740de3f92bf92cd928e088b729645b104ba5e65063725a14562b603ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747475f2af1327aa65d7b48d20a89889bc44a4f8c346713a0840d4167cc9fb4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:59:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:05:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e24f65044fa0f3a3c6a2bf5c15dd5d639173537bdcd52919cfc676d1bbd685`  
		Last Modified: Tue, 19 Dec 2023 03:22:58 GMT  
		Size: 53.3 MB (53302689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b629433016e1325add5a9e6adac29d769012947b8e2ffaccf1a6796cf6312892`  
		Last Modified: Tue, 19 Dec 2023 03:24:56 GMT  
		Size: 179.0 MB (179003314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7733751255f51040ad326e2d497c3d6aabe11a8ed24f783c9636ab12482f2ea1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330807464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9fbbaaeb6eea31291adf92f760e668048a0a46665f6b4aea3f842b280bc4d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:58:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaf6761a16c321d5d91b3da652f34fb1b7bde7c3cd21ef5adab0f5622b5abf6`  
		Last Modified: Tue, 21 Nov 2023 07:08:22 GMT  
		Size: 58.9 MB (58866450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071a148a4e40b127789a1fa17ce9bddefefb7832718f122f278a3521df2a87d8`  
		Last Modified: Tue, 21 Nov 2023 07:08:59 GMT  
		Size: 196.2 MB (196245923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d21eb43ffae9bddb2833bb2cc089a45a2657ceb129fbc1efe82596c29ef7a606
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295896976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4523cd15fcda2a1659bf2e046932979faa9852aae1b3abfb45dc8067736010`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:08:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:09:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818038e8ab94615d4f37c021912371b8c12b7678bedbb8ec6d6ab7f1831fae84`  
		Last Modified: Tue, 21 Nov 2023 06:17:26 GMT  
		Size: 54.1 MB (54065995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e80e3f19dd08ea1b9709c3e94f513a117ed8eecd4e17bbd3c4c34659f2fdda0`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 172.9 MB (172894483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:2de8a157ca69bd523133578bcee92946162393c8ea7f04d71b17238a1c0dca6c
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
$ docker pull buildpack-deps@sha256:37be48bc80197588b2d2feccf03120a53ec9aabd184144da7f2dcfa2f6641ac8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70822152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17abab90e5d47b5cad8673b9daaa37fcc26a4fdc5ffb4582e9872be12317034a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a03bad59148d9bf40f8166f217b6dda704928fb16505f2d21a0b9192b083b381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67938299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a29583da0e595c9442acc92ae579e0cf9edad17a16a1766486d022284270f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ad86b6a5c10024d3a342add15039ffb3ec622b8489665819e6526d6c20888992
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65095308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d2362666a519f1f8c5b6aa3419b0fa2db7e0e46f3aacf502ae06a7488ca50a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a66d27332240bff4f704ed98e6b0f9c76bcdb3f404159083b2146dbf53f1102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69457985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5417794b6f151c095aabdcfd742fd5c0c9d5ac6ddac5d0f5904fe51f6f65b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e4b2172754daa7430e6b100b2d40337984129de33ad4b6a6a064583df70fdbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72315257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83b0ae55d018c7a1f72e40e264e6908ab764cffe472766f5f77b57c84fbc726`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bc606146c0fc0614e0c25f15063cb2ad3af3339f6321e805ac0fec76ebc1871a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68819297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d5c02dabbe3eb8913a1640db493872fc4a19655bd1aa7dfca09269c0cadaa0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:96b66b231fd64c79e68c691f1433a4bae3e42a85f281bae68f9d92ca74757725
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75695091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889c736f84811847c5c858939a4798aed2d8b76097caa4c6d78166be76e0a32`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e358f5a8c9afb1a2a92c448a0ead789ae73f7a3f08d60828c77a609488c14ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68936498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d58ad62e6f20633b36173add8ac4f67db4f318b98538e0af575671b1d23053f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:47ffcfa7647902c7736b3d3704c3518569e369f7685887a3a92728cede275092
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
$ docker pull buildpack-deps@sha256:4054e904ff87db4d4cd59ce1a799a6bc4dc8dc4d574f08516d17a8eb6da06295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125417592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8751ba61510c6429a6fe455c2a78766f760206df597fc71174d4a0ea8745ad1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:32c0afc692587a880c866a2873aeee60904b2952de835a39c9910900a9229804
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120270005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a9c21fec3461a0186b839f920493c85c3891eed172a6bfdcdf6428e120fb6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:24:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d33e8d4b6c3b1604296a932879e7916cac6072efd2b9383ab5b5cad23e3a50f`  
		Last Modified: Tue, 19 Dec 2023 05:32:57 GMT  
		Size: 52.3 MB (52331706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d35c6f876a97b11a7b0d1b3d71452790c80789f983752662f88ac6d8d3a08060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115448427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004da5f74d1b78082f2dd316ecfd46bdb25a39e06538b2c9cf9d40759716f7b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eecaf32e1cec433a3782e292748fa035da5e777baaf4ac1861fa6524865c86`  
		Last Modified: Tue, 21 Nov 2023 14:15:27 GMT  
		Size: 50.4 MB (50353119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ff18454961275c1935ed5b18ccb8bae5d160a03b450262ea77f44a5476ff1c36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124158114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc019b1cdf28e2e065552660e6edda4acf690cd59261dafd1566d8f7d0f33816`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ef0490bf126cc792a87619e071c478855a1e91401af0ff7c7e8da38762cc3ce2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128252439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44472fb72edf1f4fd0e9d0cb13f8ac12288109eecb18aeb11483cdd421aaba0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a344c33a496f0c80e861246ac1b15db106b888d28c7bb89d17b87d06a5f1abc`  
		Last Modified: Tue, 19 Dec 2023 03:37:57 GMT  
		Size: 55.9 MB (55937182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:12102b0ad56b679bdcb5dba9c67c2d93229d41aea8fe0b985d1bc7161d1abf62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122121986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da07e60f6d913cbd8660233af63d0d5648e8da5236bc1f6530597f66cbbb2fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:59:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e24f65044fa0f3a3c6a2bf5c15dd5d639173537bdcd52919cfc676d1bbd685`  
		Last Modified: Tue, 19 Dec 2023 03:22:58 GMT  
		Size: 53.3 MB (53302689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0b321f4ed509ca9b8a6fd514c00b095650f350fa88bc41aebed430c8e630183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134561541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad50681818836003e815808939eaf0bbcf38f7bb74d0ba6c1c0a98ea2023e54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaf6761a16c321d5d91b3da652f34fb1b7bde7c3cd21ef5adab0f5622b5abf6`  
		Last Modified: Tue, 21 Nov 2023 07:08:22 GMT  
		Size: 58.9 MB (58866450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3c98e3cfb95c8dfddbcf6a9c7c2ab92065e9739358e1198121f0eb6058e38cc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123002493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01b8fe57da07ed806d6e7abc328bee8c0693bd626282085fffbe8c7c8ab436d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:08:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818038e8ab94615d4f37c021912371b8c12b7678bedbb8ec6d6ab7f1831fae84`  
		Last Modified: Tue, 21 Nov 2023 06:17:26 GMT  
		Size: 54.1 MB (54065995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:84e089fe9cc980b4826aff3d566c70f45ef41494d8e40f7d90c9c38a67e9e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:be74f13d2267f14cdc166fb7b44ecf2bd22da42b68ae3f70aff9a4b6f9461127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311866686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b67dff3be852be21dddfdecfcd1dd83113d803cb8f91dee71e75c3efe60883`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:36:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea388039df9c5c51dda7a2d1d6908eac88ae220452b81495739aff1428c1f847`  
		Last Modified: Tue, 19 Dec 2023 04:43:30 GMT  
		Size: 51.9 MB (51874049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd4fbda45c5750b2808bd8a3385ffd64974432821cfa42ae41da8450163d1f1`  
		Last Modified: Tue, 19 Dec 2023 04:44:01 GMT  
		Size: 191.9 MB (191908351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c76c8657e7d2f791f6bd7e543d59640000cd66d8f5f15b9b0baea6cfc5b243a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277699569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8319f79b9a4182bd0131a1ed842d0d669ac7ad538a597c1a36edf01cd3c8c53f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:07:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:08:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934694a3a163c892d9694911102dffb8ebb1f12f68a415dcb5d3541126843231`  
		Last Modified: Tue, 21 Nov 2023 14:16:09 GMT  
		Size: 16.2 MB (16215654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de4e1a75f9848810a987d71b29b0bba9fe490d66f3b182aececdef19ab65af`  
		Last Modified: Tue, 21 Nov 2023 14:16:25 GMT  
		Size: 47.4 MB (47410944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c1aa8dd2c0542f76fcbe22cb4412107b5a6ba0a5180b163a4b0c6fe5a87636`  
		Last Modified: Tue, 21 Nov 2023 14:16:55 GMT  
		Size: 168.1 MB (168106662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:93c6e3c30f5f51f8efdb7a09546e267034f58a1b56ea48200270a553c360e34f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302428484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5cc3fcfbdd00f4058a971444e6bdf88182c50b8a5b5abbe719733d038d3444`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d456c530acfb23832dde83f96178a2763be16deeb8b0ff91a1b1853559c902d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321291139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907ac459c6c428b9d7a4299f7cc5ca8732c73ec4746390ac14995a62c5b1ccf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:30:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8899b7af5c2eb679d56ee31148fbe43b672bf3bdec30689f9fe7cbcd3698d34e`  
		Last Modified: Tue, 19 Dec 2023 03:39:14 GMT  
		Size: 53.5 MB (53487920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da21dce6f09c3eeff5569d78b6aa0e3607d894e61dd8a5d8f600c5215807c569`  
		Last Modified: Tue, 19 Dec 2023 03:39:59 GMT  
		Size: 198.4 MB (198448371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:0433f6a953f73ca4ae671d15cf86295f574e29b4c8fb7ed1896f4afc6f29257c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:64876dded9825a6cf7b8a31e2c33d7900a3733d9a0c1767b715543b5ea62d8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e658e7fb09464559edfc915b40eaf72ba8aed754782b07343595478086c90b23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:059447d0fd9743ab8aba7fad419472b0037239d4e608a7c130b8c8b1a7de2f33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62181963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d833e96373f6ea16ffe045a89bc2f7a2e6b39641f6f94a2c9e98e6143c5a88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934694a3a163c892d9694911102dffb8ebb1f12f68a415dcb5d3541126843231`  
		Last Modified: Tue, 21 Nov 2023 14:16:09 GMT  
		Size: 16.2 MB (16215654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b431bcfe09085976ed782734c45004cea4c1ba75cca9998ecc31adc28da2b8aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a5b77a1e60a1b3b05653902263c2f74789ef79c518b44b64b86b6764c91935`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:72446ef67a7efe80796d54f800f82d918f5167ad4b8a0ea1beed984c5611e045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54846806879701cd710b18d0336f7e6bdb603682a7457520002605f150cf5a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:08cf14e37ddea892f4813b69c96b754c81045ad4e6ca4a329763ffa947ed54c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2432e97da43b885c90f029e643e09ffeebd9ba9dc5b6bd9e17f2c65a21dcb740
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119958335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83642e394b3573bf483c85a48de952bbcb3a7108706ff9d35b60fd10ce49f1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea388039df9c5c51dda7a2d1d6908eac88ae220452b81495739aff1428c1f847`  
		Last Modified: Tue, 19 Dec 2023 04:43:30 GMT  
		Size: 51.9 MB (51874049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f2b609de3ed2af6b898956f11a0f084cb7c3b3084e45d89556588957641b88b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109592907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57d448c11473b0001595ce6859c5a5a96ceb20d0ff31f9218d89ad093f82211`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:07:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934694a3a163c892d9694911102dffb8ebb1f12f68a415dcb5d3541126843231`  
		Last Modified: Tue, 21 Nov 2023 14:16:09 GMT  
		Size: 16.2 MB (16215654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de4e1a75f9848810a987d71b29b0bba9fe490d66f3b182aececdef19ab65af`  
		Last Modified: Tue, 21 Nov 2023 14:16:25 GMT  
		Size: 47.4 MB (47410944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6abfa3a0a28651d69e53ac9208acdd248eadbaf715ade52b3abfbb8a869d2249
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118952394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15032aee25b1a1ed3908832804798e4dd2eddcb74f8211fe07e97fa38400bbad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e43320ac4b0316f8d1aac727e49481a86c697332dd4a50689d584404bfcc290c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122842768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc57108a0768fac7c09eb649a01d0f50fb4ec416bff16cda596d4ae04a651cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8899b7af5c2eb679d56ee31148fbe43b672bf3bdec30689f9fe7cbcd3698d34e`  
		Last Modified: Tue, 19 Dec 2023 03:39:14 GMT  
		Size: 53.5 MB (53487920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:920f9226523d7a3ff92b78096f94f13c418345e1102e2e4f24d144aac6906531
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
$ docker pull buildpack-deps@sha256:cda8ec97c57294a6ceea1ae08c6af7dde37538d69753575aab2f1176d7bbd014
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73607702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87bac02476a0657252b47c4e4d6e60f121745c8c0c7e48a0101e4a2c1b85333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:390f50a032923f246d5a5df336203e186a8e7172b92d0aa8eae7b7929a7dd369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70043879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8fc90fd2b8868771734a3c47d342dda49fa8df68657aa64e0482b50cdd3b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ec7e94e60582861838948e4ca3f4913d5cea61af7cc8c9f1d6686387082a6a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67131988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357880f61f3530c27c69c6693c30200854440034160cb3835bb44ee35c62bc51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:889ca82473cf4a98c425f8c9039a68b8b94e14b5cfd091ca5a3d13744bb3d23f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd0a05de4ae3c58150f70b4783f7e41beb77eb181ee286d4cee9d931fb037b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af799b89d3e04d76c2b38183417363b6e95e8237850de2493bb01dec150a2667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75465937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bafaf5619993ee37dd6ffbfb62531b24a142a5c802cf6c744d3592d037aecc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6ff6fba6f20b86b8b0e8c20fb83dec2fdf5d16f69ce9d27fe7adc2a32f4ae8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bd8ac63c464f8fbe3346a160c6616fbb3d38c75666d3af63234ae420b5ce4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:784282fea3a27c11b3c8668acf83fdf5fa1f805e2c648264766bd6bedda9f057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79274604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927ae87f00aa3f0f3b5f1fccbc2848eda2dec7b3d1754259fdd0af08c5485cf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:56dea1f8a449f195ffdd426569472adfdcbb657344ea182789923be11c8b79f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3cde7adf1be7b7277ab9b2cd62cc5ea051cb781184b34e1645be1f946290f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:2d2731a5b40d1d21c76fcb5c4b00f9e9bb32b01987b5fcc9082e694f43e9db02
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
$ docker pull buildpack-deps@sha256:49f0fe4b976ac043f12a62f04bfd8adae2a952319778afc169f86509c107cf54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245752201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bc6d1de5710d03053e857c3a5eacd2b279784a069ecd156b0bd9341560518d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:15:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c20b8fe2791b6e15ca0e0c8fea173a474ac8b32c473ecd8fa0dad8254c1e0a2`  
		Last Modified: Sat, 16 Dec 2023 11:19:27 GMT  
		Size: 60.9 MB (60905474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b523f8830fca8275613fc3047b1e22961f1a7a6c7587e0bb64efed53078c94f`  
		Last Modified: Sat, 16 Dec 2023 11:19:55 GMT  
		Size: 145.1 MB (145133108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ead267650cca2661fd3975f2167362411203145a6e0caaf11c64557ac9209966
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211975825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb9bc4d2d36893e22cbb00d98af36e0ae0eb65642ef2e2b049e0a438719d401`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:18:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:22:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c119a8724608a6685fa0b34a61b0823649b200614b0f28f8e95663a4767fa`  
		Last Modified: Sat, 16 Dec 2023 09:27:47 GMT  
		Size: 9.6 MB (9599966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8358ab0bcee36d3539fb9f170efecfa9df4f1e74fa2251adc49ac10ac74952`  
		Last Modified: Sat, 16 Dec 2023 09:28:08 GMT  
		Size: 55.8 MB (55826952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f013a6bc4ca4d255a23c1e63d1fdfb28fa00386a7ff938cb51c8be1534176f`  
		Last Modified: Sat, 16 Dec 2023 09:28:34 GMT  
		Size: 121.9 MB (121947935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5b69f8f962cd85a7ce6e1bc45af306a1b8f4a78f009745a3ba34dc3252b920d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235995417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d417a10a146a055d70ef31ad8691921cacc065dd0580ce1a37f90316339e5d82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:43:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:46:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380c4384112ff5756a21a782cb3e56349b2d988fff912c2e300f7b05d457489`  
		Last Modified: Sat, 16 Dec 2023 09:52:17 GMT  
		Size: 11.0 MB (10982154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0746ab73b10a8a0e12014132cb3aa809cd3d140bfd04313883a205e6865f3`  
		Last Modified: Sat, 16 Dec 2023 09:52:34 GMT  
		Size: 61.0 MB (61012651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b011d880a900a17a3579d4920a78e1db60f769ea5c1320c9d4c0d5ba13063133`  
		Last Modified: Sat, 16 Dec 2023 09:52:55 GMT  
		Size: 136.8 MB (136797468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9482ce99fa3db42f7a580b25fc815210a3e9c376af14fa20d1034a5aa905afd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269520442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff837df70e1e592c3481bafa0e7a896d708a20c3083fcd534544afa0c050c102`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24901584c9da8423a19466ec4f3fb08b243d7102f5729a448869330a71ddc72`  
		Last Modified: Sat, 16 Dec 2023 10:34:01 GMT  
		Size: 12.9 MB (12937872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa67c542474baed45a0213236f852bc5d88639a093406a5b6231182f0058379`  
		Last Modified: Sat, 16 Dec 2023 10:34:27 GMT  
		Size: 69.6 MB (69647829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da84586fa63993f70fe6085c9b15c047c6ab3f4972037446c59141b9f844da1`  
		Last Modified: Sat, 16 Dec 2023 10:35:01 GMT  
		Size: 153.6 MB (153620421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:26660628f08bf320b00ae56a23204adabd214fb2422d14c3e98266ee173376ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226566330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774b65bf1694731af3655d129bcde92acd24f67498241b439e97dcd041f8e42e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:36:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbf59c6d3812f9f521b9fdfa2e6419c4ca08ffe8c5b6274489f04617d3e472`  
		Last Modified: Sat, 16 Dec 2023 07:41:54 GMT  
		Size: 10.7 MB (10689243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedb8b7c21d705ae2098924b2fe7951f410607de309a9159dcdea4656aa56f2`  
		Last Modified: Sat, 16 Dec 2023 07:42:11 GMT  
		Size: 60.3 MB (60310872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068074ec6695840845bf59a1dd16020f9db21b42ba9fb2e6149fce2ba86301`  
		Last Modified: Sat, 16 Dec 2023 07:42:33 GMT  
		Size: 128.6 MB (128550581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:7673b9d081573366ee82451aeec4b93a51e984ff765a8ea4ba791e0ca1024ead
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
$ docker pull buildpack-deps@sha256:199296415be961c4de236bfaaedc28a5b636890f193be30a9d4f977fa2ac44e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39713619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4528a57e0a1e9bb08fb9517e7aaf0675082cc77c9ea4ccb2fd55e4f856a24f6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f9a69781583e135fb2aa2e2b0302ffa4ae705e49027921fec90d7288a3b8b2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34200938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00ceec0d98579d19143ec7f0196882bcc060b9db40c6202e7a5a69b5da37d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c119a8724608a6685fa0b34a61b0823649b200614b0f28f8e95663a4767fa`  
		Last Modified: Sat, 16 Dec 2023 09:27:47 GMT  
		Size: 9.6 MB (9599966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6efec07dc3a777004a46c0a8b2ed890cf7033f33429d330252bed280c0c97805
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38185298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc297c299b325e22a1633441633105ca79bf1298f61b9423a98cdacc7784a5c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380c4384112ff5756a21a782cb3e56349b2d988fff912c2e300f7b05d457489`  
		Last Modified: Sat, 16 Dec 2023 09:52:17 GMT  
		Size: 11.0 MB (10982154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ac8f8dd96bde4f8f4852b9a4fb8b175b5984523cda0c4d3338c4c0528e7d3ce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46252192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f822c88396dabb70cd5d79d2159d3af9403964f9d5f44bc0418880a7a80a2eb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24901584c9da8423a19466ec4f3fb08b243d7102f5729a448869330a71ddc72`  
		Last Modified: Sat, 16 Dec 2023 10:34:01 GMT  
		Size: 12.9 MB (12937872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c992346b2af6d0020b193b7ccab7200cf7f698304a8adcea18790b7943a598e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37704877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656c410fdb9477c3bfc25768bd1c0aeb364911339ae1a706cee91c71db42aaf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbf59c6d3812f9f521b9fdfa2e6419c4ca08ffe8c5b6274489f04617d3e472`  
		Last Modified: Sat, 16 Dec 2023 07:41:54 GMT  
		Size: 10.7 MB (10689243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:48abb2c0ef13a4b8fdbae1025ba09a1a35b2c42a94c3b56b916f01e124c9afcc
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
$ docker pull buildpack-deps@sha256:2f9f349caffb0f2ade36f793a86536457b2d1e90ecf0eae5a47e328cdd0209f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100619093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7eb0e22f5cdbc37401c41319e3d76937da1e13fea7145cd2f5b058e06101383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c20b8fe2791b6e15ca0e0c8fea173a474ac8b32c473ecd8fa0dad8254c1e0a2`  
		Last Modified: Sat, 16 Dec 2023 11:19:27 GMT  
		Size: 60.9 MB (60905474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c83bfb6ddd50d498ff2f8c5369ea9af0534c7efa1fb4e5f63ea82c6a485ca553
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90027890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec1117d1a21421464a86195d1999ee114972d08f566cbea3682acbec840b2bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:18:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c119a8724608a6685fa0b34a61b0823649b200614b0f28f8e95663a4767fa`  
		Last Modified: Sat, 16 Dec 2023 09:27:47 GMT  
		Size: 9.6 MB (9599966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8358ab0bcee36d3539fb9f170efecfa9df4f1e74fa2251adc49ac10ac74952`  
		Last Modified: Sat, 16 Dec 2023 09:28:08 GMT  
		Size: 55.8 MB (55826952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:21230d6ec8667eba155677ad4f989b2e8d3b048bc345195f2e02f3c08628676a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572ab89760ba6e8291b6220d9c957d164f60e4891e38efe948c041932b04048`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:43:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380c4384112ff5756a21a782cb3e56349b2d988fff912c2e300f7b05d457489`  
		Last Modified: Sat, 16 Dec 2023 09:52:17 GMT  
		Size: 11.0 MB (10982154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0746ab73b10a8a0e12014132cb3aa809cd3d140bfd04313883a205e6865f3`  
		Last Modified: Sat, 16 Dec 2023 09:52:34 GMT  
		Size: 61.0 MB (61012651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c01c302d76283ec69bb5f663be6eacfebecfab55ac8900ac24381c8356f4784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115900021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efaea0fdf20b37cf12e6ede5f231fb98a2f8ecfa4ce7d052adaae0fdf5d3b5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24901584c9da8423a19466ec4f3fb08b243d7102f5729a448869330a71ddc72`  
		Last Modified: Sat, 16 Dec 2023 10:34:01 GMT  
		Size: 12.9 MB (12937872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa67c542474baed45a0213236f852bc5d88639a093406a5b6231182f0058379`  
		Last Modified: Sat, 16 Dec 2023 10:34:27 GMT  
		Size: 69.6 MB (69647829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:45bd2d6a723b69f1b5725e152eb9c9408820ee88b83aebfeda2dbc762625a608
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98015749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91729fbd0e1d0d3131931af841fafbf382392b3ff7ed33224ccc7121923f8a65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbf59c6d3812f9f521b9fdfa2e6419c4ca08ffe8c5b6274489f04617d3e472`  
		Last Modified: Sat, 16 Dec 2023 07:41:54 GMT  
		Size: 10.7 MB (10689243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedb8b7c21d705ae2098924b2fe7951f410607de309a9159dcdea4656aa56f2`  
		Last Modified: Sat, 16 Dec 2023 07:42:11 GMT  
		Size: 60.3 MB (60310872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:49b793d37e8a36dc753be343944245ace0ecbbeea19e92f2e74f53667c980960
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
$ docker pull buildpack-deps@sha256:4e9ec861c92dd67153dc1df1bd320fa25fd939e3edbc1627f636519b2d851b3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250058059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc43e4dd19cacc4018557e4f8c1d8ba55c56fc8c97c81b0720e740798dfa60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:18:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f8a7d572599c1debd48a9a5385f70cedee3efa5a035ac4fadc034948979add`  
		Last Modified: Sat, 16 Dec 2023 11:20:04 GMT  
		Size: 7.1 MB (7120117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c652b51acaba2f62dbf9b6e6932913b693eedd3e57ff251e5faf8080d3c720`  
		Last Modified: Sat, 16 Dec 2023 11:20:17 GMT  
		Size: 39.4 MB (39449471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b478d7d46710e8853d12306efe80ce48c807b3231fdfc4f17520ff18c63a443`  
		Last Modified: Sat, 16 Dec 2023 11:20:47 GMT  
		Size: 173.0 MB (173041894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dbbe13206b85834b453ce8234781872bc06448ce9a0face06c2ff2e273e872da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217311039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c826fee543bf4eb2ba7846a7f1fadcca269ca35896fe5d84a95a2f385baba78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:23:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:26:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f504dab242e1422942a773ffdc9f64b32c4ad2f2f933ae11318503879f2a6ed`  
		Last Modified: Sat, 16 Dec 2023 09:29:01 GMT  
		Size: 42.2 MB (42242672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cf30da1b3ef01b4af8dd61ab5eb311b8e4be8efa96b653e046fd005abe5d76`  
		Last Modified: Sat, 16 Dec 2023 09:29:28 GMT  
		Size: 140.5 MB (140523941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6c844a32a7bd2bc6b3d66ab135dfd74a85950ec0be28ed880d876ee5c7be1d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241349528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79943c4510fbd7c8b1e9b5967046a394984f59a12f6322c98583c10f7c58c32c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:47:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:51:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc1bb4922c3e6d6889ba7d474f6494f842ea5c58240c316f57c7f5477fd654`  
		Last Modified: Sat, 16 Dec 2023 09:53:05 GMT  
		Size: 7.1 MB (7066930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeeca1d35896d142baf29e201ff724b2629edcdd13eb39f8626bf934688bfc5`  
		Last Modified: Sat, 16 Dec 2023 09:53:19 GMT  
		Size: 39.4 MB (39361768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a34d39413fa289767cabec02f0b6fc9c0307332135b7cff694bdb09f6792062`  
		Last Modified: Sat, 16 Dec 2023 09:53:43 GMT  
		Size: 166.5 MB (166520548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:63f7f73318401ff45d60e23d4abb79e81d894f0005640972adbfa81997e1cdf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271363680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b3cb0ea7d30ad6375a0b20a6ae1011fbdd767aef03c672cc9111e9a122fc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:32:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de72efc09d1753caaf8c6b7fe2a5c73ace22d3acbe741d516b394a3ea5da0e7`  
		Last Modified: Sat, 16 Dec 2023 10:35:11 GMT  
		Size: 8.3 MB (8251190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c62be8e399ad2464e4d6d9e85d6f386366fabde00e1827a575829ecdd9e0820`  
		Last Modified: Sat, 16 Dec 2023 10:35:34 GMT  
		Size: 43.8 MB (43757200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3944fbddc2f4c3d092e69c6d382062dbde8f011a9d284ad77536b555cb4f0d`  
		Last Modified: Sat, 16 Dec 2023 10:36:11 GMT  
		Size: 183.7 MB (183700003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e48724d5ab7c15d9b2ab747b567a8771ef0b1ccd2f847c686f702670f4a6cadc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223840565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7c392df462a791435348bbbecc0b095f301dad5056219b1757ba03f0c77614`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:40:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4f2f1a144ba324fd3d8f8de5743652dff50c6a1029fe9d13bde04a34e5203`  
		Last Modified: Sat, 16 Dec 2023 07:42:53 GMT  
		Size: 39.4 MB (39415933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f499214031851861cc142460636b031c9cf19c11f6bbfccd95d813ad58191cc`  
		Last Modified: Sat, 16 Dec 2023 07:43:16 GMT  
		Size: 148.7 MB (148735867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:a98b0fe24b763e73fdac95caae22fbbce42b08dc238f98f0ceecce9465202a53
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
$ docker pull buildpack-deps@sha256:52bcaf8ff7d06ef5401f07f8e0afbcae02869216a7267a1b3827653c9336a857
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37566694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94de21796f573d9a3a6af2d14b1689335758184c456a2919a7677b8da0bdfead`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f8a7d572599c1debd48a9a5385f70cedee3efa5a035ac4fadc034948979add`  
		Last Modified: Sat, 16 Dec 2023 11:20:04 GMT  
		Size: 7.1 MB (7120117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:794d4a7c2505b118312f0b87dbd096ed01125d71c276c00f626a6cb087563773
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34544426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caac03054dbe2534c96a94c560c11d194ad26437fd6aaea6527656ee740a454`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4bd34233799cf9e09842419611c3700369e4b6abf1dbc4e6dee20f7b3f626e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35467212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e091a057505270dabc7203764307dfa8202a1d26da917fc3ee31feb8f5af3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc1bb4922c3e6d6889ba7d474f6494f842ea5c58240c316f57c7f5477fd654`  
		Last Modified: Sat, 16 Dec 2023 09:53:05 GMT  
		Size: 7.1 MB (7066930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:27aab4c3f2c3715203f459b788bc649aa9a2cede8e02b6c8a222629c7832eda1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43906477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee396606e247688cf49ca59b3c75f1e703757667ffee897e0da10e561d078ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de72efc09d1753caaf8c6b7fe2a5c73ace22d3acbe741d516b394a3ea5da0e7`  
		Last Modified: Sat, 16 Dec 2023 10:35:11 GMT  
		Size: 8.3 MB (8251190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8e5c93e0a2b6f080ce22e8634f9458ba487d22ad6511a50cd58cd77e00ff3d6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35688765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259643b7037de2f7883fb2369c666a716b2e13ee6afa3a6966e9e1929de6425c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:55b10c49fb8ef41cfca4c4bf74883ebfb8d8cf1444ce5d7ad495ee2e496c28cd
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
$ docker pull buildpack-deps@sha256:8a371d947edabb4c20886bec14e4533511e36494d1fc5b85259d65ea91a3e2ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77016165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a6a6919eee790ae031bdc496c2497f76c71998df2103a2e2840912740f44e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f8a7d572599c1debd48a9a5385f70cedee3efa5a035ac4fadc034948979add`  
		Last Modified: Sat, 16 Dec 2023 11:20:04 GMT  
		Size: 7.1 MB (7120117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c652b51acaba2f62dbf9b6e6932913b693eedd3e57ff251e5faf8080d3c720`  
		Last Modified: Sat, 16 Dec 2023 11:20:17 GMT  
		Size: 39.4 MB (39449471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:38a1ff60aa9570a38f695a8307b23b02025fa13de8e57ccc02735bac9b13684b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76787098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06986ac37ff65f3803f0ea5173f1874910b9aecc18a4d81f09df321a75d0145d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:23:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f504dab242e1422942a773ffdc9f64b32c4ad2f2f933ae11318503879f2a6ed`  
		Last Modified: Sat, 16 Dec 2023 09:29:01 GMT  
		Size: 42.2 MB (42242672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4254c1144719e2605489be9bac32321d4ef182cfdcbc05c323a8316252b5ee57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74828980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadc8f4b91f9c77cd5b48b837983355c6ecd357d1e7c07eff67e3b2fbd176780`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:47:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc1bb4922c3e6d6889ba7d474f6494f842ea5c58240c316f57c7f5477fd654`  
		Last Modified: Sat, 16 Dec 2023 09:53:05 GMT  
		Size: 7.1 MB (7066930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeeca1d35896d142baf29e201ff724b2629edcdd13eb39f8626bf934688bfc5`  
		Last Modified: Sat, 16 Dec 2023 09:53:19 GMT  
		Size: 39.4 MB (39361768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b4387cc3c5f1d662269be84b7d4e1fb9e7b85add31e40adecd2e3b73ab6cb801
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87663677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98515b2ab08c9a83f764288ed55907398534d81830acddc1efc9cd925b37acbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de72efc09d1753caaf8c6b7fe2a5c73ace22d3acbe741d516b394a3ea5da0e7`  
		Last Modified: Sat, 16 Dec 2023 10:35:11 GMT  
		Size: 8.3 MB (8251190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c62be8e399ad2464e4d6d9e85d6f386366fabde00e1827a575829ecdd9e0820`  
		Last Modified: Sat, 16 Dec 2023 10:35:34 GMT  
		Size: 43.8 MB (43757200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0e42e21c35bb4b3bd4d859cb9b7dee5da8b81cf3405e2aa761e0a56468a5bc28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75104698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85ebc1388dfe0e77d7f13fe90e51ea5e5fe960c81fee08d7d956876cea8559c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4f2f1a144ba324fd3d8f8de5743652dff50c6a1029fe9d13bde04a34e5203`  
		Last Modified: Sat, 16 Dec 2023 07:42:53 GMT  
		Size: 39.4 MB (39415933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:06ecaa5b0816973ff3754ed13b53143817b5c0496aa31c2abeb1d93bee9bd92d
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
$ docker pull buildpack-deps@sha256:cab48bf340039495180cbca35d871f443db57ec9d532cfe3e3a8ab6639d53cc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348837034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d791bc1cb1f6c7c46712226d0be47fb831eaad91261f02e43658860c5ddd14a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43bd898d5fbe0e1606380820047fd1e8b421722c9e69ac12757474305bd6702`  
		Last Modified: Tue, 19 Dec 2023 04:42:04 GMT  
		Size: 211.1 MB (211097790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a8cc47c1663b1b036c8bf86e0ff4c0b53743221e050d8adb5d7f5cebc6dd1925
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315969673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f57754b027a778fc62c44ad7ae37f75c346b214449818bac406b2e887d60fd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:23:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5ddaed1389aec60f80faad6640540555cb8a57f3acbc1566f210c60f5773d9`  
		Last Modified: Tue, 19 Dec 2023 05:32:27 GMT  
		Size: 184.4 MB (184416924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a815ad278fe7dc89833dd6a7b684532b6057cac1767b962afa4983575aa1f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301446383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b5e278b9d73862aec6702c3e56e8b857bf8a19cb6e66bcde7eeb68d5063df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85053a74f42624bfc14f242a6031c07b0852c368395192d70b48f596e4d153c`  
		Last Modified: Tue, 21 Nov 2023 14:14:16 GMT  
		Size: 59.3 MB (59266480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb946cf4e2606f2c7964d891cd5bd5f657448a82b430e9b2cf898f85bebd20c`  
		Last Modified: Tue, 21 Nov 2023 14:14:53 GMT  
		Size: 175.0 MB (175047915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf8885d05e431485082a33c2677686253af6bcf2dcbdc0eb3b3c83d373b3151f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339641326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ca1f96b92da15e8cb6b0264f9e7d9b036c94064f8dd766058fd40e112908a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:58:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95089c600b361807380090316c250b0b8eaf4fa2175b11ac8f49bb7581c61125`  
		Last Modified: Tue, 21 Nov 2023 08:06:50 GMT  
		Size: 202.4 MB (202449525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:41348688de89e48544adfc8884c24a7641235850d399948843d4ee5a548a8a13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351472342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2401a98522a5b225355bc86da6eb9157f7e0da556a31222d528e53437f47ccc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:26:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0d6b307a56e19161f69c60eb7c94378540e6b20f49d8b1039becdeb53cdde5`  
		Last Modified: Tue, 19 Dec 2023 03:37:24 GMT  
		Size: 210.0 MB (210025484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:09903ccf65ed5d5f71dadb8d8326f7fd50d5ef3c4bbef73440f0ee7d81b1bbc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325827014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f31fea6bf40650e456044ad189ce02c1a40169cce4e7b84e3ec9445d3fb39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:57:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d627909a3ff9de03889850fa5e83ecd71d896b3c313a14fb5c6e9915cc9b62e6`  
		Last Modified: Tue, 19 Dec 2023 03:21:51 GMT  
		Size: 189.7 MB (189684223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff34a667d81db5798aaf33085e09a789e13a45e7b48e804c87809631102b0ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362952942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b6ecc5afbeef5b86b674ec0993915e6bb01b89f9c44f901050856f10a1bf0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a54ea75827017eaea7b7055d8fca97c313c72d7a237502105b83ab018bd5ad`  
		Last Modified: Tue, 21 Nov 2023 07:07:08 GMT  
		Size: 69.6 MB (69584187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e986f224599c525ac40be9636489d408b4daff891bb3567a7986f6ae5c817cc1`  
		Last Modified: Tue, 21 Nov 2023 07:07:49 GMT  
		Size: 214.1 MB (214094151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d1822d31d3c58472a93084eaa39396b37585eb538479e3ca57d5e2e50d7470c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.2 MB (318217378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dcda8469adc1e80e5b8779671680724ff22c47c0c87e7d0658d100902caa19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c99a00cc05c2b6ae13b5a9c1b8997b9915ab687454a9fcd00d485bbb2d9a5d`  
		Last Modified: Tue, 21 Nov 2023 06:16:33 GMT  
		Size: 63.1 MB (63132875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cf7e37f4b53af6dfd3bdea89a2078a221738e8eeade3f46428f3def3e4c97c`  
		Last Modified: Tue, 21 Nov 2023 06:17:01 GMT  
		Size: 183.1 MB (183096415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:c7d7d6c28531bd9639b523bf679ccbc5d9bfd0034f4873b793a9141e1b3eb28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7b21e65f1f87a4d40c1e08ece63cdcf6d5bbb8a4ce86d1be098f46806b6c0638
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268668481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf78db3ee5ca832b01afa6e1fea9e19e28684224ec976d52b0ebec060e81872`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:14:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:19:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cee0249186900006ed579d35166f58e4d6a442a4e9b66ccb46a0243e7373da`  
		Last Modified: Sat, 02 Dec 2023 04:29:21 GMT  
		Size: 44.4 MB (44397170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8603ddc2ff7a137d2e15fbd2cea7e7e2b50e6f759511ea19bab5bf68d63a0d56`  
		Last Modified: Sat, 02 Dec 2023 04:29:52 GMT  
		Size: 182.9 MB (182858840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9306d55146ab27ef6646d3fb352cbaf44b376a52f1ee3336fb7f892393a187e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232495724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cae9150824b11c935ce2ddb3ee4e9dbfcd621a84b9dd613e2bc722a65395994`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:42:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f87a80e6c43b6548cd5b0e643f892f2fc0720cc0e1d1ca6af5004e41a46d0`  
		Last Modified: Sat, 02 Dec 2023 06:50:46 GMT  
		Size: 48.7 MB (48676390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92698ff8c25dbec9fb4ed937cd5666cea12ebe98e9d3e017cee2bb065c4911a`  
		Last Modified: Sat, 02 Dec 2023 06:51:14 GMT  
		Size: 145.7 MB (145708660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:385cb697dad3e2ba56c6a20b1afc6c56667b65f5cbfed930582d38fb13e74da5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258195944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be66fd44876dc484b4d741834e27903c02c33084a21c89ef0d518a54facc3395`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:21:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6fb536587f5b74e79c018e8e0ebffe9a2c75df578ac81ccc61a03df3accf1b`  
		Last Modified: Sat, 02 Dec 2023 05:28:44 GMT  
		Size: 44.2 MB (44238010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4868cd226407813b998f896a42c2220e514a98c0eefaeb601337750598dbe8e`  
		Last Modified: Sat, 02 Dec 2023 05:29:10 GMT  
		Size: 173.6 MB (173596864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28b94bcee4a8cb055fed2423c4a5f5eed3bddb44d642562ed919eaa94d1f61be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293032704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1edb88229280a5ee9a9bfda500be2f459fbd94de6047b1582af4c3337d92f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:39:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42ca5f151bb20d6c7b51d59876dbd19d36051f90cb24bcc0222c799a32797e9`  
		Last Modified: Sat, 02 Dec 2023 04:50:37 GMT  
		Size: 49.1 MB (49095383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bebcb056e42972476a4e6cafb3b1846641913ba2688e69054d94d3fb54cc81`  
		Last Modified: Sat, 02 Dec 2023 04:51:15 GMT  
		Size: 196.2 MB (196192278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b483a2f9d145d2d9002f37a70f79889cfd1a416c07d602971819654dff2abde5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240238066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94723dc8eb8f69ded807e3081249547013b685b7ea457bfe13797ded1fa219db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:06:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:08:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81554de0a0b21fe0679e6e99ecca0110eb2f9aa31f580f3d3e5d1b613737bbfc`  
		Last Modified: Sat, 02 Dec 2023 06:15:07 GMT  
		Size: 44.3 MB (44269164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21b029899d618b899a5bcf09c8f047e53df0420b01963eed2629239c9c37fbb`  
		Last Modified: Sat, 02 Dec 2023 06:15:33 GMT  
		Size: 155.7 MB (155723369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:529bef561ae8a198f9a0dc1f909a993a5f9cf3c8f3380dde7b7e780724c9419b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:35625ee9cb8bdb3736140d7bed8927c84ff7864fe22ad4e3862ad13f73183b2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41412471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3709cf8f8ea250fe64cda5451abaaabf8deed4ed356c5486b539a22bd49a4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0c960bf8fe85e3de325c6286655e0f0e4843462352d762744571ca4413cb3a74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38110674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dfc5354e2f27ef3aeec4e772fbddb68c3548ed79058e2e8b458663a165c1b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:850b5d8601434b851402a02d2ca745d1f54c092dcfda8c4b477eae3f11eb6a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40361070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682085e559812c18bf38779ad53974fa00af4526a3687b71c8c0f918f510072b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a0e775a0e8aefa89fe4a614f5e4160606ac9169daa9fe6420cd24e234be3ca00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24f363699741030eaad8a4735f5035cbd186d20ce147a91e10b12379dd19b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dc7b59511df9c0e21dea14d09d9b12caae9b68fe771f5946d0433776a6d453cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40245533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b48c45599caba4ecb590cab8765de0bc6cede721952ab762c574728a32180a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:8ff52549b29abd6fe2a6875d9cdfdc0a36434d45dfd420eee2d8cebd3338ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a4db1988a45960358fe344b3dd1706eb1378473e437187704aa4f0a9cc1f8ddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85809641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22511557ee0335085870fa236d32414b23f74e17bcc90dea2f56437d43f05672`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:14:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cee0249186900006ed579d35166f58e4d6a442a4e9b66ccb46a0243e7373da`  
		Last Modified: Sat, 02 Dec 2023 04:29:21 GMT  
		Size: 44.4 MB (44397170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fd63f5636aa03062899bc9a817b28b3646e702d5786120addf1052dd4d43a8cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86787064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5834b475edf594d4f57be97e2ea1e8cdbcd6a332194968f8ef09cd2469fbd1c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f87a80e6c43b6548cd5b0e643f892f2fc0720cc0e1d1ca6af5004e41a46d0`  
		Last Modified: Sat, 02 Dec 2023 06:50:46 GMT  
		Size: 48.7 MB (48676390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5208247a6a4aff72f60895a92f041d9afa3e52b280d94fd41b6c1ae182a8949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84599080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf32e027c36186e2f14c18da71be0e0aac6a2da16c77e591bdcacd8114441be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6fb536587f5b74e79c018e8e0ebffe9a2c75df578ac81ccc61a03df3accf1b`  
		Last Modified: Sat, 02 Dec 2023 05:28:44 GMT  
		Size: 44.2 MB (44238010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3f8d2d702a8d32d5ded0aee43f819fee8cc4afccdff55176e33865aec97dd462
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96840426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c692f5d3fc7325f389b2f39efd3b9c3c80dfda067e432769ba157cf4baf60ead`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42ca5f151bb20d6c7b51d59876dbd19d36051f90cb24bcc0222c799a32797e9`  
		Last Modified: Sat, 02 Dec 2023 04:50:37 GMT  
		Size: 49.1 MB (49095383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f62a41cb0e8eb2aaad22d208540d4fe09c2baf81142123136a786d7ee963770b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84514697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee9e70705122eba45793e0a1f619cc0570e8a5520d6dd5664eafd45cda6a870`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:06:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81554de0a0b21fe0679e6e99ecca0110eb2f9aa31f580f3d3e5d1b613737bbfc`  
		Last Modified: Sat, 02 Dec 2023 06:15:07 GMT  
		Size: 44.3 MB (44269164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:bda82b5ce4abbfcca5aa613c7b4eefa7244fdaa78274a1257ce3fed7c7b468aa
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
$ docker pull buildpack-deps@sha256:e1640709591c9d9e0038347965dec617f717cceec03895d42666cfbaea33545c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279758764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfef5d2082eaa961e2d3cefef8e67a7d13c9269c329297040dd1ca2d2360b92f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:26:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760243c1a983844f069a293b501cd9301cbd819c4fb9551cc389ff6e1e7cb238`  
		Last Modified: Sat, 02 Dec 2023 04:30:20 GMT  
		Size: 44.8 MB (44753276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938a8634af1b782bcdc4d1714f961d7e4beb6bf923b888e9ff9db9a53165adf`  
		Last Modified: Sat, 02 Dec 2023 04:30:54 GMT  
		Size: 197.0 MB (197026602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b6a8197e03c16a5e5c64bfe05fb54494947096f94b9d8aac266320b571278e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246704690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb114e88bdc70517c782d36daab42fa65b90488add07631546f47e8c48d2b46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:46:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3624564a762546bdc52895b1c66bc1408260d1efaa2e2b2b765adadd9c8f8`  
		Last Modified: Sat, 02 Dec 2023 06:51:41 GMT  
		Size: 48.9 MB (48942472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aeb74102316977bd7618d2394b9a9b8f7871ce0db4fa7f72ff72287befbde4`  
		Last Modified: Sat, 02 Dec 2023 06:52:11 GMT  
		Size: 162.6 MB (162594872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d62de9add5227d3e50479035c3a5c90546bf4eb61de363dc77bbf7c5630518a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271776124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6002b7cadfd93e9864d95610be91fd2b4e31e9530491ec54797bf44df2f7a49f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:23:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:25:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3c268c4f8b402b3f9907fba74a035e04caa79bd82292e937192630e4a7e64e`  
		Last Modified: Sat, 02 Dec 2023 05:29:35 GMT  
		Size: 44.7 MB (44665066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282eba19e4b5f40a7947b90ee497e8544dd23f1b54758d9068e3352ce8847e32`  
		Last Modified: Sat, 02 Dec 2023 05:30:03 GMT  
		Size: 190.1 MB (190109195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4d837a54ed79c3697e81fe74410d427abcc9ebfde406fe98a1aed32710212ac1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293583524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbf6c27960d11c3cacd25fa84f3c4a28ccd7e42d8b3b888bdbff7212085aed7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:41:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:46:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c14fb2f649d6e1f2a6ecdb5517e059449e766f72791aa8c47aa868b20d52f1`  
		Last Modified: Sat, 02 Dec 2023 04:51:47 GMT  
		Size: 49.5 MB (49544508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7b8396201f82cfdb61aa43db57c73838c2ee3354bbba5efa522ec63f8a82ed`  
		Last Modified: Sat, 02 Dec 2023 04:52:25 GMT  
		Size: 200.1 MB (200126675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eabf406ea7248077acda817b048130604c4d31ca60b0de1626699a3e2eb097cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257648877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6ba5eec539c6ac927968b4411466cd495be79e29749d9cdb335895cc3fcab7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:09:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:12:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5727db7a5897b08af6f62472ddfb225235a5740723521606d98d708b40b5b5c`  
		Last Modified: Sat, 02 Dec 2023 06:15:55 GMT  
		Size: 45.2 MB (45237357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924da814eb1bd8f1adf34e963bb6011fa2589858be016a1a9960442bf68fcc2f`  
		Last Modified: Sat, 02 Dec 2023 06:16:22 GMT  
		Size: 175.1 MB (175070849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:da38651b553d6f5be98ccc7c042b76d9065954276b7ae53d9d8e22ea79b5333e
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
$ docker pull buildpack-deps@sha256:c6f602b7643df9f295b45b95bfb4be8dfa85b98b94dd4e280809748a07d3dc36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37978886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c449b2867d49805ee4b096b0a3444aafcb711d7e3543e906c551acfb15076`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3541766b77a9d7cddffe0f683ba3de91d803ac8d96ba7997383ea11960f2645f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35167346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cf56efa7a77d4c21597de504086e09392aa92b2c6580e1188183c766fb4102`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f6f179f365fa65e5ffd520b13c82e630a1096364c6d85ff06d1d8444e51d8531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37001863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e4dd9aa8816d78892e82986f2cd6bf118375327fea8790e2fd05ae9d46879d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:04a3cc193a0eceb4125d729128dd4d0f0bb1b8a47085e1e23edf8f7d56da9b0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43912341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8991fd5c6982603f7891b53566d2c7e1439126fa3cdf93b211adbff3f17bc315`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0345da18bdf37949faa61a968b9bba8f243aff91193d4a73935b406a9330bb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37340671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e272dd5d4ca4e107463f2bcc1f447f7c851b09a44fe6729d35ae0140f60f90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:9c75924264f5ce4613ed1c74d6a1357e26212f4fb7d0bee3c7cd3dcde041e181
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
$ docker pull buildpack-deps@sha256:c7e495a12a1464b2f7a02eda48b5aaaafe94d24645bb7352d2d86eb107bac600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3da1fd7d5dc4e9975002d36007814c5c3077c22612c43346ed3266b6f55ad2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760243c1a983844f069a293b501cd9301cbd819c4fb9551cc389ff6e1e7cb238`  
		Last Modified: Sat, 02 Dec 2023 04:30:20 GMT  
		Size: 44.8 MB (44753276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0302aaedd3bab6cff8ac153d9ee30bb8b87df3a1aa0768d28cf2b67929653a76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84109818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b260ff917b448a207bc835791aafc586e4f773f48b4238d9e927ada3c5ad598`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3624564a762546bdc52895b1c66bc1408260d1efaa2e2b2b765adadd9c8f8`  
		Last Modified: Sat, 02 Dec 2023 06:51:41 GMT  
		Size: 48.9 MB (48942472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:343eb645cde6e6956c8b7164ed9d042a1e49174872fb13a4ba23d2c8c6b41235
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81666929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d83d40fc9df2bc35558833212c0763dfb4db7db07263e0ddf7cd02316790ced`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:23:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3c268c4f8b402b3f9907fba74a035e04caa79bd82292e937192630e4a7e64e`  
		Last Modified: Sat, 02 Dec 2023 05:29:35 GMT  
		Size: 44.7 MB (44665066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e3dc8db0d9983ef98c6265650ef17b378e2e0fb0dc4df96cd6e6e6e23d2fa73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93456849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975a408a5e5596adcff48d38f73cf3ecffd1da203fe40d0444a14a5270af9278`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:41:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c14fb2f649d6e1f2a6ecdb5517e059449e766f72791aa8c47aa868b20d52f1`  
		Last Modified: Sat, 02 Dec 2023 04:51:47 GMT  
		Size: 49.5 MB (49544508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:186933f2e2cc721e6fff568a413d0303f4a87bcd36cc143b64adeb1ba51f73bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82578028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3d6fb80611ed2c14a1f255df327a9462516576473e64c3024844b15eccd4ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:09:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5727db7a5897b08af6f62472ddfb225235a5740723521606d98d708b40b5b5c`  
		Last Modified: Sat, 02 Dec 2023 06:15:55 GMT  
		Size: 45.2 MB (45237357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:84e089fe9cc980b4826aff3d566c70f45ef41494d8e40f7d90c9c38a67e9e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:be74f13d2267f14cdc166fb7b44ecf2bd22da42b68ae3f70aff9a4b6f9461127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311866686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b67dff3be852be21dddfdecfcd1dd83113d803cb8f91dee71e75c3efe60883`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:36:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea388039df9c5c51dda7a2d1d6908eac88ae220452b81495739aff1428c1f847`  
		Last Modified: Tue, 19 Dec 2023 04:43:30 GMT  
		Size: 51.9 MB (51874049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd4fbda45c5750b2808bd8a3385ffd64974432821cfa42ae41da8450163d1f1`  
		Last Modified: Tue, 19 Dec 2023 04:44:01 GMT  
		Size: 191.9 MB (191908351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c76c8657e7d2f791f6bd7e543d59640000cd66d8f5f15b9b0baea6cfc5b243a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277699569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8319f79b9a4182bd0131a1ed842d0d669ac7ad538a597c1a36edf01cd3c8c53f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:07:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:08:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934694a3a163c892d9694911102dffb8ebb1f12f68a415dcb5d3541126843231`  
		Last Modified: Tue, 21 Nov 2023 14:16:09 GMT  
		Size: 16.2 MB (16215654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de4e1a75f9848810a987d71b29b0bba9fe490d66f3b182aececdef19ab65af`  
		Last Modified: Tue, 21 Nov 2023 14:16:25 GMT  
		Size: 47.4 MB (47410944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c1aa8dd2c0542f76fcbe22cb4412107b5a6ba0a5180b163a4b0c6fe5a87636`  
		Last Modified: Tue, 21 Nov 2023 14:16:55 GMT  
		Size: 168.1 MB (168106662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:93c6e3c30f5f51f8efdb7a09546e267034f58a1b56ea48200270a553c360e34f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302428484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5cc3fcfbdd00f4058a971444e6bdf88182c50b8a5b5abbe719733d038d3444`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d456c530acfb23832dde83f96178a2763be16deeb8b0ff91a1b1853559c902d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321291139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907ac459c6c428b9d7a4299f7cc5ca8732c73ec4746390ac14995a62c5b1ccf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:30:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8899b7af5c2eb679d56ee31148fbe43b672bf3bdec30689f9fe7cbcd3698d34e`  
		Last Modified: Tue, 19 Dec 2023 03:39:14 GMT  
		Size: 53.5 MB (53487920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da21dce6f09c3eeff5569d78b6aa0e3607d894e61dd8a5d8f600c5215807c569`  
		Last Modified: Tue, 19 Dec 2023 03:39:59 GMT  
		Size: 198.4 MB (198448371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:0433f6a953f73ca4ae671d15cf86295f574e29b4c8fb7ed1896f4afc6f29257c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:64876dded9825a6cf7b8a31e2c33d7900a3733d9a0c1767b715543b5ea62d8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e658e7fb09464559edfc915b40eaf72ba8aed754782b07343595478086c90b23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:059447d0fd9743ab8aba7fad419472b0037239d4e608a7c130b8c8b1a7de2f33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62181963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d833e96373f6ea16ffe045a89bc2f7a2e6b39641f6f94a2c9e98e6143c5a88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934694a3a163c892d9694911102dffb8ebb1f12f68a415dcb5d3541126843231`  
		Last Modified: Tue, 21 Nov 2023 14:16:09 GMT  
		Size: 16.2 MB (16215654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b431bcfe09085976ed782734c45004cea4c1ba75cca9998ecc31adc28da2b8aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a5b77a1e60a1b3b05653902263c2f74789ef79c518b44b64b86b6764c91935`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:72446ef67a7efe80796d54f800f82d918f5167ad4b8a0ea1beed984c5611e045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54846806879701cd710b18d0336f7e6bdb603682a7457520002605f150cf5a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:08cf14e37ddea892f4813b69c96b754c81045ad4e6ca4a329763ffa947ed54c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2432e97da43b885c90f029e643e09ffeebd9ba9dc5b6bd9e17f2c65a21dcb740
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119958335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83642e394b3573bf483c85a48de952bbcb3a7108706ff9d35b60fd10ce49f1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea388039df9c5c51dda7a2d1d6908eac88ae220452b81495739aff1428c1f847`  
		Last Modified: Tue, 19 Dec 2023 04:43:30 GMT  
		Size: 51.9 MB (51874049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f2b609de3ed2af6b898956f11a0f084cb7c3b3084e45d89556588957641b88b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109592907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57d448c11473b0001595ce6859c5a5a96ceb20d0ff31f9218d89ad093f82211`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:07:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934694a3a163c892d9694911102dffb8ebb1f12f68a415dcb5d3541126843231`  
		Last Modified: Tue, 21 Nov 2023 14:16:09 GMT  
		Size: 16.2 MB (16215654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de4e1a75f9848810a987d71b29b0bba9fe490d66f3b182aececdef19ab65af`  
		Last Modified: Tue, 21 Nov 2023 14:16:25 GMT  
		Size: 47.4 MB (47410944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6abfa3a0a28651d69e53ac9208acdd248eadbaf715ade52b3abfbb8a869d2249
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118952394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15032aee25b1a1ed3908832804798e4dd2eddcb74f8211fe07e97fa38400bbad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e43320ac4b0316f8d1aac727e49481a86c697332dd4a50689d584404bfcc290c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122842768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc57108a0768fac7c09eb649a01d0f50fb4ec416bff16cda596d4ae04a651cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8899b7af5c2eb679d56ee31148fbe43b672bf3bdec30689f9fe7cbcd3698d34e`  
		Last Modified: Tue, 19 Dec 2023 03:39:14 GMT  
		Size: 53.5 MB (53487920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:379b7a278c2c0bd77484f30e960362980bb739a2d40325f8c5380a9d5678e79f
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
$ docker pull buildpack-deps@sha256:b81ac95e1cbe6774145a8c46c70798f3abada991aed19e74c711a667d06c313b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322298176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693a3b0e9f0beeb137d71fd998420f2ed5e4a873f1a925b166fd73d9d8c67d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:34:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e04794082b8082ce8c158a02cb11d1d737d6c0cd1542062514b3e2a93f6c70`  
		Last Modified: Tue, 19 Dec 2023 04:43:04 GMT  
		Size: 196.9 MB (196880584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a1ebfbfcc336a9f01d4cff2524309fd8b64f24d077436c9cad5856b4ddc8bc0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295368190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e3414d217203458c81aff1b8ea98e2b097fdf45f0356f282ec5876d5f2815`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:24:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:25:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d33e8d4b6c3b1604296a932879e7916cac6072efd2b9383ab5b5cad23e3a50f`  
		Last Modified: Tue, 19 Dec 2023 05:32:57 GMT  
		Size: 52.3 MB (52331706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4500a3ccfba84ad29d6a187a1df58375b465c6b72d771c80b4ba92087ef6a90`  
		Last Modified: Tue, 19 Dec 2023 05:33:31 GMT  
		Size: 175.1 MB (175098185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:281c2e7852166ddfeddf3eeb4e89583bbae350d41b7e8343ff9e31371aa3122b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282799881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e319e2640284bad2c1d9d24bd03f403a9619d08ff70efbb26f940147ba97a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:06:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eecaf32e1cec433a3782e292748fa035da5e777baaf4ac1861fa6524865c86`  
		Last Modified: Tue, 21 Nov 2023 14:15:27 GMT  
		Size: 50.4 MB (50353119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7849827a6023dc0eb89664b4bbcb1022abfed00e52a6656cf5c7d397bf3fc7`  
		Last Modified: Tue, 21 Nov 2023 14:15:57 GMT  
		Size: 167.4 MB (167351454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf1e855f9c67ff4a7db063750a11952d01ed274933c1f6ed704bf85a3f2c4b19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313958448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180f08699a0077d6aef1bbb77ab77e3696234930f168750b984377131dac7299`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe2c38c6b934d9d3107cc7ce50d9e852c8ccef92d5cbc324a6f083b5aef0d1`  
		Last Modified: Tue, 21 Nov 2023 08:07:42 GMT  
		Size: 189.8 MB (189800334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d2daaa23b6589fe5fa4ad0819ac5ff9897ea02be04e946b5de89bb38ff76d577
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328049320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8d2042afa39d811a9b7f8c7987284473a9820285c3cf850a40238dfc0b2f9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:28:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a344c33a496f0c80e861246ac1b15db106b888d28c7bb89d17b87d06a5f1abc`  
		Last Modified: Tue, 19 Dec 2023 03:37:57 GMT  
		Size: 55.9 MB (55937182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb89bdf92d460c8b83c3effc827149c832709e4d9e4e2262456e267a2e4decf`  
		Last Modified: Tue, 19 Dec 2023 03:38:42 GMT  
		Size: 199.8 MB (199796881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:88c6ced740de3f92bf92cd928e088b729645b104ba5e65063725a14562b603ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747475f2af1327aa65d7b48d20a89889bc44a4f8c346713a0840d4167cc9fb4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:59:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:05:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e24f65044fa0f3a3c6a2bf5c15dd5d639173537bdcd52919cfc676d1bbd685`  
		Last Modified: Tue, 19 Dec 2023 03:22:58 GMT  
		Size: 53.3 MB (53302689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b629433016e1325add5a9e6adac29d769012947b8e2ffaccf1a6796cf6312892`  
		Last Modified: Tue, 19 Dec 2023 03:24:56 GMT  
		Size: 179.0 MB (179003314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7733751255f51040ad326e2d497c3d6aabe11a8ed24f783c9636ab12482f2ea1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330807464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9fbbaaeb6eea31291adf92f760e668048a0a46665f6b4aea3f842b280bc4d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:58:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaf6761a16c321d5d91b3da652f34fb1b7bde7c3cd21ef5adab0f5622b5abf6`  
		Last Modified: Tue, 21 Nov 2023 07:08:22 GMT  
		Size: 58.9 MB (58866450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071a148a4e40b127789a1fa17ce9bddefefb7832718f122f278a3521df2a87d8`  
		Last Modified: Tue, 21 Nov 2023 07:08:59 GMT  
		Size: 196.2 MB (196245923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d21eb43ffae9bddb2833bb2cc089a45a2657ceb129fbc1efe82596c29ef7a606
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295896976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4523cd15fcda2a1659bf2e046932979faa9852aae1b3abfb45dc8067736010`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:08:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:09:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818038e8ab94615d4f37c021912371b8c12b7678bedbb8ec6d6ab7f1831fae84`  
		Last Modified: Tue, 21 Nov 2023 06:17:26 GMT  
		Size: 54.1 MB (54065995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e80e3f19dd08ea1b9709c3e94f513a117ed8eecd4e17bbd3c4c34659f2fdda0`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 172.9 MB (172894483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:2de8a157ca69bd523133578bcee92946162393c8ea7f04d71b17238a1c0dca6c
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
$ docker pull buildpack-deps@sha256:37be48bc80197588b2d2feccf03120a53ec9aabd184144da7f2dcfa2f6641ac8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70822152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17abab90e5d47b5cad8673b9daaa37fcc26a4fdc5ffb4582e9872be12317034a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a03bad59148d9bf40f8166f217b6dda704928fb16505f2d21a0b9192b083b381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67938299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a29583da0e595c9442acc92ae579e0cf9edad17a16a1766486d022284270f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ad86b6a5c10024d3a342add15039ffb3ec622b8489665819e6526d6c20888992
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65095308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d2362666a519f1f8c5b6aa3419b0fa2db7e0e46f3aacf502ae06a7488ca50a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a66d27332240bff4f704ed98e6b0f9c76bcdb3f404159083b2146dbf53f1102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69457985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5417794b6f151c095aabdcfd742fd5c0c9d5ac6ddac5d0f5904fe51f6f65b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e4b2172754daa7430e6b100b2d40337984129de33ad4b6a6a064583df70fdbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72315257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83b0ae55d018c7a1f72e40e264e6908ab764cffe472766f5f77b57c84fbc726`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bc606146c0fc0614e0c25f15063cb2ad3af3339f6321e805ac0fec76ebc1871a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68819297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d5c02dabbe3eb8913a1640db493872fc4a19655bd1aa7dfca09269c0cadaa0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:96b66b231fd64c79e68c691f1433a4bae3e42a85f281bae68f9d92ca74757725
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75695091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889c736f84811847c5c858939a4798aed2d8b76097caa4c6d78166be76e0a32`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e358f5a8c9afb1a2a92c448a0ead789ae73f7a3f08d60828c77a609488c14ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68936498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d58ad62e6f20633b36173add8ac4f67db4f318b98538e0af575671b1d23053f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:47ffcfa7647902c7736b3d3704c3518569e369f7685887a3a92728cede275092
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
$ docker pull buildpack-deps@sha256:4054e904ff87db4d4cd59ce1a799a6bc4dc8dc4d574f08516d17a8eb6da06295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125417592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8751ba61510c6429a6fe455c2a78766f760206df597fc71174d4a0ea8745ad1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:32c0afc692587a880c866a2873aeee60904b2952de835a39c9910900a9229804
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120270005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a9c21fec3461a0186b839f920493c85c3891eed172a6bfdcdf6428e120fb6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:24:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d33e8d4b6c3b1604296a932879e7916cac6072efd2b9383ab5b5cad23e3a50f`  
		Last Modified: Tue, 19 Dec 2023 05:32:57 GMT  
		Size: 52.3 MB (52331706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d35c6f876a97b11a7b0d1b3d71452790c80789f983752662f88ac6d8d3a08060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115448427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004da5f74d1b78082f2dd316ecfd46bdb25a39e06538b2c9cf9d40759716f7b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eecaf32e1cec433a3782e292748fa035da5e777baaf4ac1861fa6524865c86`  
		Last Modified: Tue, 21 Nov 2023 14:15:27 GMT  
		Size: 50.4 MB (50353119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ff18454961275c1935ed5b18ccb8bae5d160a03b450262ea77f44a5476ff1c36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124158114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc019b1cdf28e2e065552660e6edda4acf690cd59261dafd1566d8f7d0f33816`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ef0490bf126cc792a87619e071c478855a1e91401af0ff7c7e8da38762cc3ce2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128252439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44472fb72edf1f4fd0e9d0cb13f8ac12288109eecb18aeb11483cdd421aaba0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a344c33a496f0c80e861246ac1b15db106b888d28c7bb89d17b87d06a5f1abc`  
		Last Modified: Tue, 19 Dec 2023 03:37:57 GMT  
		Size: 55.9 MB (55937182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:12102b0ad56b679bdcb5dba9c67c2d93229d41aea8fe0b985d1bc7161d1abf62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122121986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da07e60f6d913cbd8660233af63d0d5648e8da5236bc1f6530597f66cbbb2fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:59:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e24f65044fa0f3a3c6a2bf5c15dd5d639173537bdcd52919cfc676d1bbd685`  
		Last Modified: Tue, 19 Dec 2023 03:22:58 GMT  
		Size: 53.3 MB (53302689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0b321f4ed509ca9b8a6fd514c00b095650f350fa88bc41aebed430c8e630183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134561541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad50681818836003e815808939eaf0bbcf38f7bb74d0ba6c1c0a98ea2023e54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaf6761a16c321d5d91b3da652f34fb1b7bde7c3cd21ef5adab0f5622b5abf6`  
		Last Modified: Tue, 21 Nov 2023 07:08:22 GMT  
		Size: 58.9 MB (58866450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3c98e3cfb95c8dfddbcf6a9c7c2ab92065e9739358e1198121f0eb6058e38cc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123002493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01b8fe57da07ed806d6e7abc328bee8c0693bd626282085fffbe8c7c8ab436d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:08:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818038e8ab94615d4f37c021912371b8c12b7678bedbb8ec6d6ab7f1831fae84`  
		Last Modified: Tue, 21 Nov 2023 06:17:26 GMT  
		Size: 54.1 MB (54065995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:1cbc77f04c5facaecfeda50d61d2636f35f49161e26f7e89ab0d177e964a96f2
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
$ docker pull buildpack-deps@sha256:a3fba8caf6509c5246a424e170457c0fa67a654b8cf3b9adb7ebdb32d6e55dd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74c65587a9edbcf9a75606c9753bbc489d003c39838e299fa593e655bd31766`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fe46ac679ff949d5099a4d5e3c4846bf93801df8852f569d4b98acd702804616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2830d417ae6fd93ea6f902e7c515936f50e33ddd54431596e33dbad425026`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0531a6dee1ec00ac6c4467943728d8df874a0db45976e6717b6f6bb7d625c3f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126398468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e6f0f26595e7d2f41e4027ddcb1a44e10b203994b8a19e47b7c02bb2905c48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85053a74f42624bfc14f242a6031c07b0852c368395192d70b48f596e4d153c`  
		Last Modified: Tue, 21 Nov 2023 14:14:16 GMT  
		Size: 59.3 MB (59266480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce0af9ba6e5a5840c7fbbe85a3ac5d2f028a84167b274095b85e353c37996b56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137191801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6117910a955cc657572894f9d7fcfe8b0e051e427abaa349776e641b089c6b4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:07139c0b1ab111539ee39037d7176130c6e8c7bd2f8a0c0c25d5eb0841358089
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141446858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ddd0f8763eba9ac84fc03f15e7e4ed7b7555c3f1b2617c15c0ef31fb6d1451`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f6bc94392d10b737484515c04dcc61b2c129c94735217591ea4ad865b35098ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136142791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa001887bc8f8fc436a8584002635ae26f975a75d402283a48799fc0a478e53d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad518e13047a2bffa7358d6ed80141ee89918b12549d94563fe33dfe97693f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148858791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1afccc4310e63668ea2fa68e7ed2114f91aa1c4023a673f0dbd3cb0d533ddd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a54ea75827017eaea7b7055d8fca97c313c72d7a237502105b83ab018bd5ad`  
		Last Modified: Tue, 21 Nov 2023 07:07:08 GMT  
		Size: 69.6 MB (69584187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a1788f5a7099541c5a0691f88050070dd6e2d5f4b0c97777b19ed32f799c64e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135120963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2372afa7eb1de18c0332fe8e706503fe4a85393e04c4f9b30e3689e074ea3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c99a00cc05c2b6ae13b5a9c1b8997b9915ab687454a9fcd00d485bbb2d9a5d`  
		Last Modified: Tue, 21 Nov 2023 06:16:33 GMT  
		Size: 63.1 MB (63132875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:3b1f824f051acf35594227b8e7008cdadd108bfd2836fe01620f24eaf83b942b
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
$ docker pull buildpack-deps@sha256:c845ddbdbb0fa7e4bd3cf5974fc76b42adb5f8c56dfdb8bd4bc1cdf5eea8a316
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (403022326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37917f3f1a9598b7f32def6b58c12fbc145e485fc831ce2aaef3982ae65869de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:38:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9565a064a4e2c8d2e24ea50bb5793fd5453d880cc1268075d4c95136016c2`  
		Last Modified: Tue, 19 Dec 2023 04:44:29 GMT  
		Size: 66.0 MB (66049037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6485f47f21b2f643a2d43d6b92fe5745eb69bb2804ae95f0bebc3e1ec52b8c7b`  
		Last Modified: Tue, 19 Dec 2023 04:45:09 GMT  
		Size: 261.0 MB (260959970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3a4fa67d6308c9d11531802a1714b7e3a30f7a0e2fdda70c23e2ec9565eb1350
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370914489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b521f21f6e40b32094690d87fef9846447df7e982f17cdf3775c7078d652fe9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:28:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1076957cedc8a5a67b5ef8a93c803e6193f70ae925dc66e3135d08c87986fa`  
		Last Modified: Tue, 19 Dec 2023 05:34:49 GMT  
		Size: 235.1 MB (235059785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e988e2b761b7907248c3baec9d8b049bc00d14cf504d536fa5bd326741b3c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329762097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bf22b48f37312328eb7e982bbc9d1e2c935a9405231e9ac750dcc1fe1d4b3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7a5eecc1f0a2e75f1dc4cc1953feec4555e8fb395f67d882284d7c17af33c`  
		Last Modified: Tue, 21 Nov 2023 14:17:25 GMT  
		Size: 60.6 MB (60615689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b893a98c470e054f25c3d481469624db1f3da7ac9daea450c53b2a2143f696a`  
		Last Modified: Tue, 21 Nov 2023 14:18:01 GMT  
		Size: 199.2 MB (199248157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f225bbcadae8e6551be733c86ec70bdfbf01b19f0e7e455fa62e0abf26aa53b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.3 MB (371250495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd8802d413e16d8959c5b5ff9372558d845c6e8e17362f75316d30ceaeb7eb2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:03:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a3b26cecdfe35cedc579177de975c502073e0ec3b623c7408d7145436fd16`  
		Last Modified: Tue, 21 Nov 2023 08:08:57 GMT  
		Size: 65.6 MB (65611513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19182edeea8364f6c86849824848525bb23ffaa624f5316c079717a211be36da`  
		Last Modified: Tue, 21 Nov 2023 08:09:28 GMT  
		Size: 229.0 MB (229024712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f223534a49fdd91590e92469d3b44a3b66e5187cc236c26c9f45150a59d0c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.8 MB (403778905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9a75df9181fd5bf88807fe290de501affc38a281b1db10a31e07aa69e35cc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:33:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e5706d82a57d517f5b2faa92178f9346b9a474417ad5a9158a842164e920a6`  
		Last Modified: Tue, 19 Dec 2023 03:40:36 GMT  
		Size: 67.8 MB (67809651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1c36b513ad68c22e61b529691192c0fc48c4d221456d5d0e9c2369fe1553ef`  
		Last Modified: Tue, 19 Dec 2023 03:41:34 GMT  
		Size: 258.0 MB (257966559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d5e4e403e5b231279b9a643c0e32b8d3eb8d640c2debc18a403b750a5ee69bd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372669397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6405ec487dc34ccbdc687f1e61d093d714dda4add87ff3db3ef75cd70e666ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:08:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:15:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539b334e5a1b4f830e2cb90767d1d6bd23065595b3d40e6cd589ec973f33276`  
		Last Modified: Tue, 19 Dec 2023 03:26:15 GMT  
		Size: 64.9 MB (64877294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0428530ea0a6a33939b2c19cf5f38e214292abff9ad746bdc4afcfea7397bcd7`  
		Last Modified: Tue, 19 Dec 2023 03:28:48 GMT  
		Size: 232.3 MB (232306893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1766ed0c020a64b0c0245a19f9ba7a951551f98147642a9acf6ede2115229dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393372396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e24823afdd39ee710bbbc971c39d0aa4ff7fb43aebaf6a79c893b045539c7d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:02:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fb001517f3aa634674774ca44ff1ee072157218fcd0522c1630479101d895`  
		Last Modified: Tue, 21 Nov 2023 07:09:33 GMT  
		Size: 70.9 MB (70920797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b31909696ac928d37c89a4769a0d196f1f4641efdd73d46c6a365e9c76eea9b`  
		Last Modified: Tue, 21 Nov 2023 07:10:21 GMT  
		Size: 239.0 MB (239016768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8da7b54261080b809f45176c4399c2a846f298c5dca668c5ef9d891960e05619
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.9 MB (435912718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66322a3b41a21a07cd1c50aaacb0216d49a586c240665706c1eb10bfe1357d36`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:41:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe6c23c39483f54e5cc09f3805cbea29d02f6bbc773bf62d752dbdc74d194e3`  
		Last Modified: Tue, 19 Dec 2023 02:43:08 GMT  
		Size: 65.3 MB (65295558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cdabb923ae43d95eb49f5a86e41045d58be42c151b0890419973020357d956`  
		Last Modified: Tue, 19 Dec 2023 02:49:01 GMT  
		Size: 296.6 MB (296602883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c93fc2e94d1d3a26456ef129ab582ef7d63a767ab8762db8940202c77f1388df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355072174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc793a1658b88281067a4063d6ed988d648fdb13eb5611f6e42534971d82b3da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21db908a00e81480eebf3fad2c4e13874394ba9f9978d3ea7677d3be28b4fb`  
		Last Modified: Tue, 21 Nov 2023 06:18:18 GMT  
		Size: 66.5 MB (66490545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d423dea4ea04d9998b72e9dca146ee1f13e78ec50b02fa0de85998fc82032b`  
		Last Modified: Tue, 21 Nov 2023 06:18:48 GMT  
		Size: 211.3 MB (211321007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:4a430ed950cc4b98eadd6279ed85deb6a30b8c1236ecce50f607fefda69410cf
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
$ docker pull buildpack-deps@sha256:7fd071471c070146e579b6e18e3385299f6bd90fcdac5376a06e689a769d5e9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76013319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c938c72d716541c88f972961bbd785d121eb6be6212ee7519eb38483bf81aff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6619eb9db222bd053555e7cb22ca730e3186bd13c78473a06b5c617036fabc6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72177696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be421aff42b9b42179286525e3b47418aaf1a1c3514b8d81c7da8f912e66bfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:91852f70f0cc52e34e2337e46e2299c93f1f788c16ee5355947448e4b95aeccd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69898251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c0e073649b042ef2a2fe654648e05461d464a86fc72415260cece782621787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7d94a1efff10fcb19fbd83cfb66d8d450a7ed085c20a21d34777ddeea944d677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76614270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84f666bba1d3f33d489b7f1ca30183b36b1949707e4cfcc5b70fad6f28dfe30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f5bce5b2a812ac3e4d477ded664ef22b441a4e04cf273a87c312d5ebef7ee6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78002695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0b69328536bca8f709bb9cbc16648970c323d17878bc58bf9d30c585881148`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1e5bcd2de6aac0d979e9e3ac7288764dc6ba5531745b4ea398fcf254dc899375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75485210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6422bcdcce20e3e6dcea181aea6a3ae12e19f7ed14a04a35cd8c79a1f6a07330`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bf7b2c6f20aeaa97efb86336a12338247f96a743fa032cbb6e848100e365d25e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83434831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e185b08bc814b3731dcb7aa4ef80f272175c6d3715e08afb5a280d02f76715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e2b661dc9029e826be1456b9abde55f5a23438a6f9f7ac222510e045a0d9f8a
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b585177a3343949dae98f8d0e2e5591bb16fa3a41b44d130e49941538583ed42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:132caa5f4dfbbce1e1f7a982aa07300d03415c825ae2ba80361c5c01a31e8332
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77260622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e28664175d244c1cd5e4e6f02cccb38f1c27e640751ef1722a1529d588c2a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:8db8de49bb5c7774ab4edafa8e72f9481ef5af1fe1f8b79412e95874a398250f
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
$ docker pull buildpack-deps@sha256:e0d5e41352ab8cf617b9920e2249a5a53258e38c0a21a33e2c18993575ab51e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142062356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a979ddc17b1169bcd0e7d369cee427e20e75db30073643f8df8f9d1443751d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9565a064a4e2c8d2e24ea50bb5793fd5453d880cc1268075d4c95136016c2`  
		Last Modified: Tue, 19 Dec 2023 04:44:29 GMT  
		Size: 66.0 MB (66049037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eda7ad1c9adf08141546487b4ca131c7c951de47acff64152d95db04680b52af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135854704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd629151c9a68becd2cd8cecc176f909736db356d0d4889c5700cbd713dcf67d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43bd039a111ff18dd0a63cd13a31d9dd641b36941ebd1cb91eeac6d9cb35d1a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130513940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ee8381f8cf9588f0e2a248e8ff70be2963e34f40b9d56f53796168d3f1103d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7a5eecc1f0a2e75f1dc4cc1953feec4555e8fb395f67d882284d7c17af33c`  
		Last Modified: Tue, 21 Nov 2023 14:17:25 GMT  
		Size: 60.6 MB (60615689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:af589c91ef37d6c32116a1b241e4aad363808ff422474ba16f569efd841b146f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142225783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222f9f3797f956ce854e32cffc6df6746b36e71ec083ec3b8e35759cf731ff9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a3b26cecdfe35cedc579177de975c502073e0ec3b623c7408d7145436fd16`  
		Last Modified: Tue, 21 Nov 2023 08:08:57 GMT  
		Size: 65.6 MB (65611513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b403e321a12af49825b52173de020258f34e044645d5b4c7e407638600344d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145812346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c0378b636a237178ce1710b59568f8522ef9de3399ff88454c0edb618c2d03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e5706d82a57d517f5b2faa92178f9346b9a474417ad5a9158a842164e920a6`  
		Last Modified: Tue, 19 Dec 2023 03:40:36 GMT  
		Size: 67.8 MB (67809651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7d6b57ec0772da03f76089453b7948af8001f2b7c4cd6275133e62771f6c4842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140362504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268dd58b533640c04942005a5685b8022869bd3c3cf19a393c854217f467a20f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:08:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539b334e5a1b4f830e2cb90767d1d6bd23065595b3d40e6cd589ec973f33276`  
		Last Modified: Tue, 19 Dec 2023 03:26:15 GMT  
		Size: 64.9 MB (64877294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:24a7862e93585787852dbaecc311fe50c85ca997c602ae777a5a40f37264db6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f839951b7a1ec1855581f34657a10b0e452a76662c147f9893fb5b4b1355743a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fb001517f3aa634674774ca44ff1ee072157218fcd0522c1630479101d895`  
		Last Modified: Tue, 21 Nov 2023 07:09:33 GMT  
		Size: 70.9 MB (70920797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cab57db4abded03a615cdeb1b61f19d471f83b61cd62d49fe9248e47afd5ddfa
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139309835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b18f767be5d0b44739d653a26034dce3433781c850d7429a89e91f08e6aee7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe6c23c39483f54e5cc09f3805cbea29d02f6bbc773bf62d752dbdc74d194e3`  
		Last Modified: Tue, 19 Dec 2023 02:43:08 GMT  
		Size: 65.3 MB (65295558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1769e0bcb2fe395e6ae63c7c91bdeee37003e88269a8db80d927a4fc64840f8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143751167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47000f61dc60af3bdb834e3d3470c752ac2e6269191cb531d5f7264a413791e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21db908a00e81480eebf3fad2c4e13874394ba9f9978d3ea7677d3be28b4fb`  
		Last Modified: Tue, 21 Nov 2023 06:18:18 GMT  
		Size: 66.5 MB (66490545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:06ecaa5b0816973ff3754ed13b53143817b5c0496aa31c2abeb1d93bee9bd92d
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
$ docker pull buildpack-deps@sha256:cab48bf340039495180cbca35d871f443db57ec9d532cfe3e3a8ab6639d53cc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348837034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d791bc1cb1f6c7c46712226d0be47fb831eaad91261f02e43658860c5ddd14a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43bd898d5fbe0e1606380820047fd1e8b421722c9e69ac12757474305bd6702`  
		Last Modified: Tue, 19 Dec 2023 04:42:04 GMT  
		Size: 211.1 MB (211097790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a8cc47c1663b1b036c8bf86e0ff4c0b53743221e050d8adb5d7f5cebc6dd1925
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315969673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f57754b027a778fc62c44ad7ae37f75c346b214449818bac406b2e887d60fd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:23:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5ddaed1389aec60f80faad6640540555cb8a57f3acbc1566f210c60f5773d9`  
		Last Modified: Tue, 19 Dec 2023 05:32:27 GMT  
		Size: 184.4 MB (184416924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a815ad278fe7dc89833dd6a7b684532b6057cac1767b962afa4983575aa1f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301446383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b5e278b9d73862aec6702c3e56e8b857bf8a19cb6e66bcde7eeb68d5063df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:05:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85053a74f42624bfc14f242a6031c07b0852c368395192d70b48f596e4d153c`  
		Last Modified: Tue, 21 Nov 2023 14:14:16 GMT  
		Size: 59.3 MB (59266480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb946cf4e2606f2c7964d891cd5bd5f657448a82b430e9b2cf898f85bebd20c`  
		Last Modified: Tue, 21 Nov 2023 14:14:53 GMT  
		Size: 175.0 MB (175047915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf8885d05e431485082a33c2677686253af6bcf2dcbdc0eb3b3c83d373b3151f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339641326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ca1f96b92da15e8cb6b0264f9e7d9b036c94064f8dd766058fd40e112908a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:58:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95089c600b361807380090316c250b0b8eaf4fa2175b11ac8f49bb7581c61125`  
		Last Modified: Tue, 21 Nov 2023 08:06:50 GMT  
		Size: 202.4 MB (202449525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:41348688de89e48544adfc8884c24a7641235850d399948843d4ee5a548a8a13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351472342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2401a98522a5b225355bc86da6eb9157f7e0da556a31222d528e53437f47ccc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:26:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0d6b307a56e19161f69c60eb7c94378540e6b20f49d8b1039becdeb53cdde5`  
		Last Modified: Tue, 19 Dec 2023 03:37:24 GMT  
		Size: 210.0 MB (210025484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:09903ccf65ed5d5f71dadb8d8326f7fd50d5ef3c4bbef73440f0ee7d81b1bbc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325827014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f31fea6bf40650e456044ad189ce02c1a40169cce4e7b84e3ec9445d3fb39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:57:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d627909a3ff9de03889850fa5e83ecd71d896b3c313a14fb5c6e9915cc9b62e6`  
		Last Modified: Tue, 19 Dec 2023 03:21:51 GMT  
		Size: 189.7 MB (189684223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff34a667d81db5798aaf33085e09a789e13a45e7b48e804c87809631102b0ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362952942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b6ecc5afbeef5b86b674ec0993915e6bb01b89f9c44f901050856f10a1bf0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a54ea75827017eaea7b7055d8fca97c313c72d7a237502105b83ab018bd5ad`  
		Last Modified: Tue, 21 Nov 2023 07:07:08 GMT  
		Size: 69.6 MB (69584187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e986f224599c525ac40be9636489d408b4daff891bb3567a7986f6ae5c817cc1`  
		Last Modified: Tue, 21 Nov 2023 07:07:49 GMT  
		Size: 214.1 MB (214094151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d1822d31d3c58472a93084eaa39396b37585eb538479e3ca57d5e2e50d7470c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.2 MB (318217378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dcda8469adc1e80e5b8779671680724ff22c47c0c87e7d0658d100902caa19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c99a00cc05c2b6ae13b5a9c1b8997b9915ab687454a9fcd00d485bbb2d9a5d`  
		Last Modified: Tue, 21 Nov 2023 06:16:33 GMT  
		Size: 63.1 MB (63132875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cf7e37f4b53af6dfd3bdea89a2078a221738e8eeade3f46428f3def3e4c97c`  
		Last Modified: Tue, 21 Nov 2023 06:17:01 GMT  
		Size: 183.1 MB (183096415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:920f9226523d7a3ff92b78096f94f13c418345e1102e2e4f24d144aac6906531
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
$ docker pull buildpack-deps@sha256:cda8ec97c57294a6ceea1ae08c6af7dde37538d69753575aab2f1176d7bbd014
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73607702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87bac02476a0657252b47c4e4d6e60f121745c8c0c7e48a0101e4a2c1b85333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:390f50a032923f246d5a5df336203e186a8e7172b92d0aa8eae7b7929a7dd369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70043879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8fc90fd2b8868771734a3c47d342dda49fa8df68657aa64e0482b50cdd3b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ec7e94e60582861838948e4ca3f4913d5cea61af7cc8c9f1d6686387082a6a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67131988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357880f61f3530c27c69c6693c30200854440034160cb3835bb44ee35c62bc51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:889ca82473cf4a98c425f8c9039a68b8b94e14b5cfd091ca5a3d13744bb3d23f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd0a05de4ae3c58150f70b4783f7e41beb77eb181ee286d4cee9d931fb037b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af799b89d3e04d76c2b38183417363b6e95e8237850de2493bb01dec150a2667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75465937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bafaf5619993ee37dd6ffbfb62531b24a142a5c802cf6c744d3592d037aecc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6ff6fba6f20b86b8b0e8c20fb83dec2fdf5d16f69ce9d27fe7adc2a32f4ae8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bd8ac63c464f8fbe3346a160c6616fbb3d38c75666d3af63234ae420b5ce4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:784282fea3a27c11b3c8668acf83fdf5fa1f805e2c648264766bd6bedda9f057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79274604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927ae87f00aa3f0f3b5f1fccbc2848eda2dec7b3d1754259fdd0af08c5485cf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:56dea1f8a449f195ffdd426569472adfdcbb657344ea182789923be11c8b79f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3cde7adf1be7b7277ab9b2cd62cc5ea051cb781184b34e1645be1f946290f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:1cbc77f04c5facaecfeda50d61d2636f35f49161e26f7e89ab0d177e964a96f2
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
$ docker pull buildpack-deps@sha256:a3fba8caf6509c5246a424e170457c0fa67a654b8cf3b9adb7ebdb32d6e55dd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74c65587a9edbcf9a75606c9753bbc489d003c39838e299fa593e655bd31766`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fe46ac679ff949d5099a4d5e3c4846bf93801df8852f569d4b98acd702804616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131552749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2830d417ae6fd93ea6f902e7c515936f50e33ddd54431596e33dbad425026`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0531a6dee1ec00ac6c4467943728d8df874a0db45976e6717b6f6bb7d625c3f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126398468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e6f0f26595e7d2f41e4027ddcb1a44e10b203994b8a19e47b7c02bb2905c48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:33 GMT
ADD file:e90da0ca6ed29299007a9b8fd99fb4134cb37f22a833a55752add2b86657f694 in / 
# Tue, 21 Nov 2023 03:57:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52c01871afffc7432976815bfd8aab1abb41e8df039231492714566f852db38a`  
		Last Modified: Tue, 21 Nov 2023 04:01:24 GMT  
		Size: 45.2 MB (45180046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb054df5eff93daa6563e5c3e43d6288fda872fd7bdcb684c5bd0a39f4f501`  
		Last Modified: Tue, 21 Nov 2023 14:13:54 GMT  
		Size: 22.0 MB (21951942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85053a74f42624bfc14f242a6031c07b0852c368395192d70b48f596e4d153c`  
		Last Modified: Tue, 21 Nov 2023 14:14:16 GMT  
		Size: 59.3 MB (59266480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce0af9ba6e5a5840c7fbbe85a3ac5d2f028a84167b274095b85e353c37996b56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137191801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6117910a955cc657572894f9d7fcfe8b0e051e427abaa349776e641b089c6b4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:07139c0b1ab111539ee39037d7176130c6e8c7bd2f8a0c0c25d5eb0841358089
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141446858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ddd0f8763eba9ac84fc03f15e7e4ed7b7555c3f1b2617c15c0ef31fb6d1451`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f6bc94392d10b737484515c04dcc61b2c129c94735217591ea4ad865b35098ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136142791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa001887bc8f8fc436a8584002635ae26f975a75d402283a48799fc0a478e53d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad518e13047a2bffa7358d6ed80141ee89918b12549d94563fe33dfe97693f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148858791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1afccc4310e63668ea2fa68e7ed2114f91aa1c4023a673f0dbd3cb0d533ddd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:23:59 GMT
ADD file:209097c8dfcefec7951851d25bc9e8c1d56aefed076c682c5f2e077cc05aeaf8 in / 
# Tue, 21 Nov 2023 04:24:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d694a6aceb98c067febf569d227d6249cd8d39b11dead73e4840d07861a25e9`  
		Last Modified: Tue, 21 Nov 2023 04:28:27 GMT  
		Size: 53.6 MB (53575858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71d255e683d12334b12df8a9e23692d03ce5d514a74efe4553f12269885d87`  
		Last Modified: Tue, 21 Nov 2023 07:06:46 GMT  
		Size: 25.7 MB (25698746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a54ea75827017eaea7b7055d8fca97c313c72d7a237502105b83ab018bd5ad`  
		Last Modified: Tue, 21 Nov 2023 07:07:08 GMT  
		Size: 69.6 MB (69584187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a1788f5a7099541c5a0691f88050070dd6e2d5f4b0c97777b19ed32f799c64e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135120963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2372afa7eb1de18c0332fe8e706503fe4a85393e04c4f9b30e3689e074ea3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:00 GMT
ADD file:8bb55d91755618d4e84d57150867ddbe9513d01cf9543fa953cf7cd1745397ac in / 
# Tue, 21 Nov 2023 05:04:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7318387eb66a53962a6ff8f603919b1f2eebd63059538ee442fb3f3643d79fd1`  
		Last Modified: Tue, 21 Nov 2023 05:10:07 GMT  
		Size: 47.9 MB (47943002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20203ebe78a0c1643a97475f1f406b6af2dedd0e14005e4ca4bbeca0470d21`  
		Last Modified: Tue, 21 Nov 2023 06:16:17 GMT  
		Size: 24.0 MB (24045086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c99a00cc05c2b6ae13b5a9c1b8997b9915ab687454a9fcd00d485bbb2d9a5d`  
		Last Modified: Tue, 21 Nov 2023 06:16:33 GMT  
		Size: 63.1 MB (63132875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:4bd6e26ec0ea35484b4172b0306be7cd8eed5013b03c15c460edb2819f344fb8
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
$ docker pull buildpack-deps@sha256:2d5e989857d1e1f64ace65ec7af0794b7f990c3fcea51a62110360c9781ffc58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396707025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e4884de179770a56b2f4f6d82a82db6e330cdc21307212134f537fcd47c9ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:40:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86533899ea4c6a05c0bc99be1cf97d8c7b1864649d1d7b07f04486b15f07cb0`  
		Last Modified: Tue, 19 Dec 2023 04:45:40 GMT  
		Size: 66.1 MB (66061532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee84ae1998d47ab8aff67d6563bd2a6e54efb95c3d90f97ef91f104b052d9eb2`  
		Last Modified: Tue, 19 Dec 2023 04:46:20 GMT  
		Size: 254.6 MB (254641404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d803c828fa78e4048b6dd9f0819767f330151ea595818e1febed9c5afd3cb1a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364689828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733f23a4295ce61add3f84746d870e37e455f2f81532ea3486e741341710334`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:30:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0751a1e8acd62fd190d7c3bec2800497b26033c33f78f5fb4ac87c59dc9eff`  
		Last Modified: Tue, 19 Dec 2023 05:36:11 GMT  
		Size: 228.9 MB (228855857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff1cca875ae566271b3e769bd18bb09f37df748943985be07efba04551815174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328762631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b60a050106dfcfdebe1886a016eb6e80fd1d8a0426c5d811ab6d3fcf6288882`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:12:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b87af5a0303242349bd3387e8e710da8c4bed4c8b6c9248b7adbe02282821`  
		Last Modified: Tue, 21 Nov 2023 14:18:32 GMT  
		Size: 60.6 MB (60613394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf7f63febe06481274b0d67a3ef0711788f1f0bc3415bf73b3899511d6561e`  
		Last Modified: Tue, 21 Nov 2023 14:19:07 GMT  
		Size: 199.2 MB (199173746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c018690c4f0c300dd387799ca9b994a0562975a819c054ce966bccfe5adc7b8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369944620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e08aacb8e0e6187a75e6b7b12ad2de093844519931c5e6e53f3d51caee3a9a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:05:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f062b3f69830199094fd9bd9a07a08b65ee4def0bd5c712c6ee103880bff09ac`  
		Last Modified: Tue, 21 Nov 2023 08:09:55 GMT  
		Size: 65.6 MB (65608954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c6b57a3426da6d5ea042dec10d08ff79196d6cc9483bcc52884a82b0a640c`  
		Last Modified: Tue, 21 Nov 2023 08:10:27 GMT  
		Size: 228.9 MB (228936466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cbe2dbf67545dc5c97c3c6f5b728aaddf86e84287e90c82d23ed35bfcac6adcd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397358797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170a759d81adcc81daeeb7b7a13324c354ceaed76dcb35dd0f258b4e3ac3bbcf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:35:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cab3bcda927a6bdf058c09d2eb156aa0af0222312987068a8db4995e0e7b38`  
		Last Modified: Tue, 19 Dec 2023 03:42:10 GMT  
		Size: 67.8 MB (67818215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9a37e534304fa065f9b443c37df037032a614c5be60ac7a59f1ad9b9ba36f1`  
		Last Modified: Tue, 19 Dec 2023 03:43:07 GMT  
		Size: 251.6 MB (251576047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40b4181b80cf65fc42c77a9553ea0cdc6e0040612932097d1a8e3f4dd1cce56a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356010219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f220b84e9f7445f61892b7b44a97ee9a994f5bdc7f638dacbdddce253e4f87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:16:18 GMT
ADD file:5a5a104714237ebb36fb780708ec93fc6f37e226c70a6cb07acb454559074354 in / 
# Tue, 21 Nov 2023 04:16:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:51:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:57:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d49b5078b4e69925915d9f9be6cb94f93e60122ef1d800b354bcd8216ec830be`  
		Last Modified: Tue, 21 Nov 2023 04:27:30 GMT  
		Size: 49.3 MB (49327517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d3064a22d3ef7862a5268a8afe02ea1fd4667ea569463a73e72e664e09e6a`  
		Last Modified: Tue, 21 Nov 2023 13:08:31 GMT  
		Size: 26.1 MB (26073748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20a1437fbf153264541271f63ca64815b844be642e2c03279cb0e53ad0725bf`  
		Last Modified: Tue, 21 Nov 2023 13:09:24 GMT  
		Size: 64.3 MB (64313324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9682bf3e11922ae5e8c90100b670cb465c8b8c08e66f44c7cb49b086a3899f7`  
		Last Modified: Tue, 21 Nov 2023 13:11:47 GMT  
		Size: 216.3 MB (216295630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7122304c08fa3322fb619c28b1d079afd3d5d1ae28d49a7c9e5e054c1b641aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 MB (392079404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd296328898f802900eb913bb6523c2ceecf64df4a720940a7c51218cce74b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:05:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09699f0245492a67f8cf23ca1a57b1830e534c2904c0101f5032102ad5f2c4c1`  
		Last Modified: Tue, 21 Nov 2023 07:10:57 GMT  
		Size: 70.9 MB (70922067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67883ae22a135174fd28adf25d7ee6ae5e6bce0ed0f2184e2e8693a052f4d849`  
		Last Modified: Tue, 21 Nov 2023 07:11:43 GMT  
		Size: 238.9 MB (238904628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fc3c7f7fdec6e003481bbeb0997f6daa643394d8da369bd4790ac484bf03a5bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353469255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c825610f278f9458ee2308b22e1fb54a3e9f39fe8f41b26fcba0d3d2b866a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:13:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09114f0213626e79784208aa286e09335b4ba1f291eb0eca1b085809f09d3a4`  
		Last Modified: Tue, 21 Nov 2023 06:19:11 GMT  
		Size: 66.5 MB (66490948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f4a65c94de18a1fd53de8a964d1e72298a66a44688d4fcc60dd699744a8ae`  
		Last Modified: Tue, 21 Nov 2023 06:19:41 GMT  
		Size: 211.2 MB (211178710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:11cb13d012d51186560a65c702cfe6c0a360a68393d7bc90e3f9529092b3ced4
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
$ docker pull buildpack-deps@sha256:3f50f9a8ec92d7613a2c9e4314890e8fa5fb3f242848fa896996af67bed51ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76004089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd5b9cda28dfe341c6bfaec8d1d565301d3484e35aa826ec7c2422b55976899`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:54054aae8d2509a606118039eeeee6c1efa28c6bbeb78b90e4812da597c0b30a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72158146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b16c510c0ddc939492d299d77df951dc4daec95385122ea2920a9f278bd749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:24af446129c20fed40646ef159c8b9901f24b6d6016c9d196ba51fe5a217e4c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68975491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de296b4a5fa842242b30d85c8a249eb0b82878ffd618e96f3a3cd73ad4ec0f3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b8c8fa8fa1b762cb6082830128bcba69fb55d1dce8c7669125b54d28f54a27b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75399200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800fef3e46173a59495d29a44218fa0b3400cfdfc28efd7e0088224f05da0dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee003c3f905a9cad83790fc2caeae421adf065218be7ae4d9fc6c1cc9f172540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77964535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b7006dfc2585e037c17696b58061ff5f3e840dff2ddd30d634621ac0b48054`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8d53552c020d8577a97b4d00b9e69b62db059054744745792dbe36cd56940603
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76039896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395b3db0610d69b3233d02d9a8dff807dc7974d8e92e849268c9aa8a8ac9466b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:20:17 GMT
ADD file:8ea6310c27e7f62f29291d04a24b83af6da2d5e3faa1996293119c2feddc0c07 in / 
# Tue, 19 Dec 2023 02:20:23 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b33999eae7d9b8d6555148eda58da0cc5207bcf4c08ed630879dc0190791680f`  
		Last Modified: Tue, 19 Dec 2023 02:31:43 GMT  
		Size: 49.1 MB (49068400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbe2cdae3821f18626a3cba0479848ecb8d93b32bc3d454eb52e1fe702148fd`  
		Last Modified: Tue, 19 Dec 2023 03:29:12 GMT  
		Size: 27.0 MB (26971496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:965f912e338611b668babc493a452d7633aada0b922596c5ef12cc6e50e27a3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82252709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bdba459863fec3e91bd7c853b0ea34383073b319aa7a132424943ec736438d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3cec0b4b3003b6e8ca7b66e3ea1180aacfef23d35fe6903a4accc9f2e403d199
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75799597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31893a587eeb03b3917a1a1c908f5d45b32756818b46d56b8e081ce5579ba7f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:fbbddbf5f22ac7c7c8ecc9fcc471d8949cee637b3644bfbd7ee2cd153da554fd
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
$ docker pull buildpack-deps@sha256:c0671311fe2df63cb6409bfc09fb8981d8340b18f1095bfb33c7526b6a26dd16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142065621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4dd427945b05d85995a35fa4d41637c064ea78cdf1cc59adc53f627d7097623`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86533899ea4c6a05c0bc99be1cf97d8c7b1864649d1d7b07f04486b15f07cb0`  
		Last Modified: Tue, 19 Dec 2023 04:45:40 GMT  
		Size: 66.1 MB (66061532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:13bceeb03345c9a59eac75e79c3d51e7fcd73ba4f6b510649a033585731dc1d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135833971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c888f7c37c41a6c2475dcea11c0c95537cd1b746e2673e122ae4fb352585c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:90a681e8e90b6720921b8f7ac6294c41fdbdb0b3352a3898522409425e690f5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129588885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ef0b823d873fb6d43427a124bdb38b6738c0afee2a830b1d27b87b454468ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b87af5a0303242349bd3387e8e710da8c4bed4c8b6c9248b7adbe02282821`  
		Last Modified: Tue, 21 Nov 2023 14:18:32 GMT  
		Size: 60.6 MB (60613394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9b8986ba543d946187b8c26349ecde3edcb0112fd2c27e08f362b5e1c277b605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141008154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2406e1f99a452aabbb862577d2e816ff3e79019d35079785c5703e6f89d592`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f062b3f69830199094fd9bd9a07a08b65ee4def0bd5c712c6ee103880bff09ac`  
		Last Modified: Tue, 21 Nov 2023 08:09:55 GMT  
		Size: 65.6 MB (65608954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe2f5901d6fe0d1944a3856bd2bedb58332b2f3049ace7138edffb4668c677bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145782750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2fd75b070f0a4c5276459e18f30b018df15fae60a9f1d899cbe1e1782ddfc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cab3bcda927a6bdf058c09d2eb156aa0af0222312987068a8db4995e0e7b38`  
		Last Modified: Tue, 19 Dec 2023 03:42:10 GMT  
		Size: 67.8 MB (67818215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d1dc0b8fdda160220d48b8e2d0efe0fe602b51705fcdd4a12e81de92e80f6cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b21ef50f4ae8cd5a1aac2dee9f4573f60c80c927af1e3a651567b79ac682fe8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:16:18 GMT
ADD file:5a5a104714237ebb36fb780708ec93fc6f37e226c70a6cb07acb454559074354 in / 
# Tue, 21 Nov 2023 04:16:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:51:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d49b5078b4e69925915d9f9be6cb94f93e60122ef1d800b354bcd8216ec830be`  
		Last Modified: Tue, 21 Nov 2023 04:27:30 GMT  
		Size: 49.3 MB (49327517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d3064a22d3ef7862a5268a8afe02ea1fd4667ea569463a73e72e664e09e6a`  
		Last Modified: Tue, 21 Nov 2023 13:08:31 GMT  
		Size: 26.1 MB (26073748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20a1437fbf153264541271f63ca64815b844be642e2c03279cb0e53ad0725bf`  
		Last Modified: Tue, 21 Nov 2023 13:09:24 GMT  
		Size: 64.3 MB (64313324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d10b4a6b3ef635a2b679169bacda8ac4b674df60ae3371a03c8a1f5cc86e7a93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153174776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ba107c9d649eae78c14111b541fbffa91311376657fbeebbcb7275085fe88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09699f0245492a67f8cf23ca1a57b1830e534c2904c0101f5032102ad5f2c4c1`  
		Last Modified: Tue, 21 Nov 2023 07:10:57 GMT  
		Size: 70.9 MB (70922067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1151634c7e3a017b784f1eb9a20d31ca5b19e61af07410c71d068ffca257b06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142290545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585f78d00d4e7d5176cfb4e20e019ad8271fa52f40eae6313924bd54827c4bde`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09114f0213626e79784208aa286e09335b4ba1f291eb0eca1b085809f09d3a4`  
		Last Modified: Tue, 21 Nov 2023 06:19:11 GMT  
		Size: 66.5 MB (66490948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:4bd6e26ec0ea35484b4172b0306be7cd8eed5013b03c15c460edb2819f344fb8
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
$ docker pull buildpack-deps@sha256:2d5e989857d1e1f64ace65ec7af0794b7f990c3fcea51a62110360c9781ffc58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396707025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e4884de179770a56b2f4f6d82a82db6e330cdc21307212134f537fcd47c9ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:40:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86533899ea4c6a05c0bc99be1cf97d8c7b1864649d1d7b07f04486b15f07cb0`  
		Last Modified: Tue, 19 Dec 2023 04:45:40 GMT  
		Size: 66.1 MB (66061532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee84ae1998d47ab8aff67d6563bd2a6e54efb95c3d90f97ef91f104b052d9eb2`  
		Last Modified: Tue, 19 Dec 2023 04:46:20 GMT  
		Size: 254.6 MB (254641404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d803c828fa78e4048b6dd9f0819767f330151ea595818e1febed9c5afd3cb1a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364689828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733f23a4295ce61add3f84746d870e37e455f2f81532ea3486e741341710334`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:30:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0751a1e8acd62fd190d7c3bec2800497b26033c33f78f5fb4ac87c59dc9eff`  
		Last Modified: Tue, 19 Dec 2023 05:36:11 GMT  
		Size: 228.9 MB (228855857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff1cca875ae566271b3e769bd18bb09f37df748943985be07efba04551815174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328762631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b60a050106dfcfdebe1886a016eb6e80fd1d8a0426c5d811ab6d3fcf6288882`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:12:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b87af5a0303242349bd3387e8e710da8c4bed4c8b6c9248b7adbe02282821`  
		Last Modified: Tue, 21 Nov 2023 14:18:32 GMT  
		Size: 60.6 MB (60613394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf7f63febe06481274b0d67a3ef0711788f1f0bc3415bf73b3899511d6561e`  
		Last Modified: Tue, 21 Nov 2023 14:19:07 GMT  
		Size: 199.2 MB (199173746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c018690c4f0c300dd387799ca9b994a0562975a819c054ce966bccfe5adc7b8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369944620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e08aacb8e0e6187a75e6b7b12ad2de093844519931c5e6e53f3d51caee3a9a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:05:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f062b3f69830199094fd9bd9a07a08b65ee4def0bd5c712c6ee103880bff09ac`  
		Last Modified: Tue, 21 Nov 2023 08:09:55 GMT  
		Size: 65.6 MB (65608954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c6b57a3426da6d5ea042dec10d08ff79196d6cc9483bcc52884a82b0a640c`  
		Last Modified: Tue, 21 Nov 2023 08:10:27 GMT  
		Size: 228.9 MB (228936466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cbe2dbf67545dc5c97c3c6f5b728aaddf86e84287e90c82d23ed35bfcac6adcd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397358797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170a759d81adcc81daeeb7b7a13324c354ceaed76dcb35dd0f258b4e3ac3bbcf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:35:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cab3bcda927a6bdf058c09d2eb156aa0af0222312987068a8db4995e0e7b38`  
		Last Modified: Tue, 19 Dec 2023 03:42:10 GMT  
		Size: 67.8 MB (67818215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9a37e534304fa065f9b443c37df037032a614c5be60ac7a59f1ad9b9ba36f1`  
		Last Modified: Tue, 19 Dec 2023 03:43:07 GMT  
		Size: 251.6 MB (251576047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40b4181b80cf65fc42c77a9553ea0cdc6e0040612932097d1a8e3f4dd1cce56a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356010219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f220b84e9f7445f61892b7b44a97ee9a994f5bdc7f638dacbdddce253e4f87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:16:18 GMT
ADD file:5a5a104714237ebb36fb780708ec93fc6f37e226c70a6cb07acb454559074354 in / 
# Tue, 21 Nov 2023 04:16:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:51:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:57:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d49b5078b4e69925915d9f9be6cb94f93e60122ef1d800b354bcd8216ec830be`  
		Last Modified: Tue, 21 Nov 2023 04:27:30 GMT  
		Size: 49.3 MB (49327517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d3064a22d3ef7862a5268a8afe02ea1fd4667ea569463a73e72e664e09e6a`  
		Last Modified: Tue, 21 Nov 2023 13:08:31 GMT  
		Size: 26.1 MB (26073748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20a1437fbf153264541271f63ca64815b844be642e2c03279cb0e53ad0725bf`  
		Last Modified: Tue, 21 Nov 2023 13:09:24 GMT  
		Size: 64.3 MB (64313324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9682bf3e11922ae5e8c90100b670cb465c8b8c08e66f44c7cb49b086a3899f7`  
		Last Modified: Tue, 21 Nov 2023 13:11:47 GMT  
		Size: 216.3 MB (216295630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7122304c08fa3322fb619c28b1d079afd3d5d1ae28d49a7c9e5e054c1b641aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 MB (392079404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd296328898f802900eb913bb6523c2ceecf64df4a720940a7c51218cce74b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:05:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09699f0245492a67f8cf23ca1a57b1830e534c2904c0101f5032102ad5f2c4c1`  
		Last Modified: Tue, 21 Nov 2023 07:10:57 GMT  
		Size: 70.9 MB (70922067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67883ae22a135174fd28adf25d7ee6ae5e6bce0ed0f2184e2e8693a052f4d849`  
		Last Modified: Tue, 21 Nov 2023 07:11:43 GMT  
		Size: 238.9 MB (238904628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fc3c7f7fdec6e003481bbeb0997f6daa643394d8da369bd4790ac484bf03a5bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353469255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c825610f278f9458ee2308b22e1fb54a3e9f39fe8f41b26fcba0d3d2b866a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:13:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09114f0213626e79784208aa286e09335b4ba1f291eb0eca1b085809f09d3a4`  
		Last Modified: Tue, 21 Nov 2023 06:19:11 GMT  
		Size: 66.5 MB (66490948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f4a65c94de18a1fd53de8a964d1e72298a66a44688d4fcc60dd699744a8ae`  
		Last Modified: Tue, 21 Nov 2023 06:19:41 GMT  
		Size: 211.2 MB (211178710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:11cb13d012d51186560a65c702cfe6c0a360a68393d7bc90e3f9529092b3ced4
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
$ docker pull buildpack-deps@sha256:3f50f9a8ec92d7613a2c9e4314890e8fa5fb3f242848fa896996af67bed51ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76004089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd5b9cda28dfe341c6bfaec8d1d565301d3484e35aa826ec7c2422b55976899`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:54054aae8d2509a606118039eeeee6c1efa28c6bbeb78b90e4812da597c0b30a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72158146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b16c510c0ddc939492d299d77df951dc4daec95385122ea2920a9f278bd749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:24af446129c20fed40646ef159c8b9901f24b6d6016c9d196ba51fe5a217e4c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68975491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de296b4a5fa842242b30d85c8a249eb0b82878ffd618e96f3a3cd73ad4ec0f3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b8c8fa8fa1b762cb6082830128bcba69fb55d1dce8c7669125b54d28f54a27b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75399200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800fef3e46173a59495d29a44218fa0b3400cfdfc28efd7e0088224f05da0dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee003c3f905a9cad83790fc2caeae421adf065218be7ae4d9fc6c1cc9f172540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77964535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b7006dfc2585e037c17696b58061ff5f3e840dff2ddd30d634621ac0b48054`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8d53552c020d8577a97b4d00b9e69b62db059054744745792dbe36cd56940603
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76039896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395b3db0610d69b3233d02d9a8dff807dc7974d8e92e849268c9aa8a8ac9466b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:20:17 GMT
ADD file:8ea6310c27e7f62f29291d04a24b83af6da2d5e3faa1996293119c2feddc0c07 in / 
# Tue, 19 Dec 2023 02:20:23 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b33999eae7d9b8d6555148eda58da0cc5207bcf4c08ed630879dc0190791680f`  
		Last Modified: Tue, 19 Dec 2023 02:31:43 GMT  
		Size: 49.1 MB (49068400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbe2cdae3821f18626a3cba0479848ecb8d93b32bc3d454eb52e1fe702148fd`  
		Last Modified: Tue, 19 Dec 2023 03:29:12 GMT  
		Size: 27.0 MB (26971496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:965f912e338611b668babc493a452d7633aada0b922596c5ef12cc6e50e27a3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82252709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bdba459863fec3e91bd7c853b0ea34383073b319aa7a132424943ec736438d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3cec0b4b3003b6e8ca7b66e3ea1180aacfef23d35fe6903a4accc9f2e403d199
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75799597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31893a587eeb03b3917a1a1c908f5d45b32756818b46d56b8e081ce5579ba7f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:fbbddbf5f22ac7c7c8ecc9fcc471d8949cee637b3644bfbd7ee2cd153da554fd
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
$ docker pull buildpack-deps@sha256:c0671311fe2df63cb6409bfc09fb8981d8340b18f1095bfb33c7526b6a26dd16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142065621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4dd427945b05d85995a35fa4d41637c064ea78cdf1cc59adc53f627d7097623`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86533899ea4c6a05c0bc99be1cf97d8c7b1864649d1d7b07f04486b15f07cb0`  
		Last Modified: Tue, 19 Dec 2023 04:45:40 GMT  
		Size: 66.1 MB (66061532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:13bceeb03345c9a59eac75e79c3d51e7fcd73ba4f6b510649a033585731dc1d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135833971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c888f7c37c41a6c2475dcea11c0c95537cd1b746e2673e122ae4fb352585c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:90a681e8e90b6720921b8f7ac6294c41fdbdb0b3352a3898522409425e690f5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129588885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ef0b823d873fb6d43427a124bdb38b6738c0afee2a830b1d27b87b454468ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b87af5a0303242349bd3387e8e710da8c4bed4c8b6c9248b7adbe02282821`  
		Last Modified: Tue, 21 Nov 2023 14:18:32 GMT  
		Size: 60.6 MB (60613394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9b8986ba543d946187b8c26349ecde3edcb0112fd2c27e08f362b5e1c277b605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141008154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2406e1f99a452aabbb862577d2e816ff3e79019d35079785c5703e6f89d592`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f062b3f69830199094fd9bd9a07a08b65ee4def0bd5c712c6ee103880bff09ac`  
		Last Modified: Tue, 21 Nov 2023 08:09:55 GMT  
		Size: 65.6 MB (65608954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe2f5901d6fe0d1944a3856bd2bedb58332b2f3049ace7138edffb4668c677bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145782750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2fd75b070f0a4c5276459e18f30b018df15fae60a9f1d899cbe1e1782ddfc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cab3bcda927a6bdf058c09d2eb156aa0af0222312987068a8db4995e0e7b38`  
		Last Modified: Tue, 19 Dec 2023 03:42:10 GMT  
		Size: 67.8 MB (67818215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d1dc0b8fdda160220d48b8e2d0efe0fe602b51705fcdd4a12e81de92e80f6cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b21ef50f4ae8cd5a1aac2dee9f4573f60c80c927af1e3a651567b79ac682fe8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:16:18 GMT
ADD file:5a5a104714237ebb36fb780708ec93fc6f37e226c70a6cb07acb454559074354 in / 
# Tue, 21 Nov 2023 04:16:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:51:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d49b5078b4e69925915d9f9be6cb94f93e60122ef1d800b354bcd8216ec830be`  
		Last Modified: Tue, 21 Nov 2023 04:27:30 GMT  
		Size: 49.3 MB (49327517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d3064a22d3ef7862a5268a8afe02ea1fd4667ea569463a73e72e664e09e6a`  
		Last Modified: Tue, 21 Nov 2023 13:08:31 GMT  
		Size: 26.1 MB (26073748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20a1437fbf153264541271f63ca64815b844be642e2c03279cb0e53ad0725bf`  
		Last Modified: Tue, 21 Nov 2023 13:09:24 GMT  
		Size: 64.3 MB (64313324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d10b4a6b3ef635a2b679169bacda8ac4b674df60ae3371a03c8a1f5cc86e7a93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153174776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ba107c9d649eae78c14111b541fbffa91311376657fbeebbcb7275085fe88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09699f0245492a67f8cf23ca1a57b1830e534c2904c0101f5032102ad5f2c4c1`  
		Last Modified: Tue, 21 Nov 2023 07:10:57 GMT  
		Size: 70.9 MB (70922067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1151634c7e3a017b784f1eb9a20d31ca5b19e61af07410c71d068ffca257b06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142290545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585f78d00d4e7d5176cfb4e20e019ad8271fa52f40eae6313924bd54827c4bde`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09114f0213626e79784208aa286e09335b4ba1f291eb0eca1b085809f09d3a4`  
		Last Modified: Tue, 21 Nov 2023 06:19:11 GMT  
		Size: 66.5 MB (66490948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:3b1f824f051acf35594227b8e7008cdadd108bfd2836fe01620f24eaf83b942b
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
$ docker pull buildpack-deps@sha256:c845ddbdbb0fa7e4bd3cf5974fc76b42adb5f8c56dfdb8bd4bc1cdf5eea8a316
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (403022326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37917f3f1a9598b7f32def6b58c12fbc145e485fc831ce2aaef3982ae65869de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:38:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9565a064a4e2c8d2e24ea50bb5793fd5453d880cc1268075d4c95136016c2`  
		Last Modified: Tue, 19 Dec 2023 04:44:29 GMT  
		Size: 66.0 MB (66049037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6485f47f21b2f643a2d43d6b92fe5745eb69bb2804ae95f0bebc3e1ec52b8c7b`  
		Last Modified: Tue, 19 Dec 2023 04:45:09 GMT  
		Size: 261.0 MB (260959970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3a4fa67d6308c9d11531802a1714b7e3a30f7a0e2fdda70c23e2ec9565eb1350
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370914489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b521f21f6e40b32094690d87fef9846447df7e982f17cdf3775c7078d652fe9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:28:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1076957cedc8a5a67b5ef8a93c803e6193f70ae925dc66e3135d08c87986fa`  
		Last Modified: Tue, 19 Dec 2023 05:34:49 GMT  
		Size: 235.1 MB (235059785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e988e2b761b7907248c3baec9d8b049bc00d14cf504d536fa5bd326741b3c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329762097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bf22b48f37312328eb7e982bbc9d1e2c935a9405231e9ac750dcc1fe1d4b3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7a5eecc1f0a2e75f1dc4cc1953feec4555e8fb395f67d882284d7c17af33c`  
		Last Modified: Tue, 21 Nov 2023 14:17:25 GMT  
		Size: 60.6 MB (60615689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b893a98c470e054f25c3d481469624db1f3da7ac9daea450c53b2a2143f696a`  
		Last Modified: Tue, 21 Nov 2023 14:18:01 GMT  
		Size: 199.2 MB (199248157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f225bbcadae8e6551be733c86ec70bdfbf01b19f0e7e455fa62e0abf26aa53b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.3 MB (371250495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd8802d413e16d8959c5b5ff9372558d845c6e8e17362f75316d30ceaeb7eb2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:03:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a3b26cecdfe35cedc579177de975c502073e0ec3b623c7408d7145436fd16`  
		Last Modified: Tue, 21 Nov 2023 08:08:57 GMT  
		Size: 65.6 MB (65611513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19182edeea8364f6c86849824848525bb23ffaa624f5316c079717a211be36da`  
		Last Modified: Tue, 21 Nov 2023 08:09:28 GMT  
		Size: 229.0 MB (229024712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f223534a49fdd91590e92469d3b44a3b66e5187cc236c26c9f45150a59d0c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.8 MB (403778905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9a75df9181fd5bf88807fe290de501affc38a281b1db10a31e07aa69e35cc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:33:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e5706d82a57d517f5b2faa92178f9346b9a474417ad5a9158a842164e920a6`  
		Last Modified: Tue, 19 Dec 2023 03:40:36 GMT  
		Size: 67.8 MB (67809651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1c36b513ad68c22e61b529691192c0fc48c4d221456d5d0e9c2369fe1553ef`  
		Last Modified: Tue, 19 Dec 2023 03:41:34 GMT  
		Size: 258.0 MB (257966559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d5e4e403e5b231279b9a643c0e32b8d3eb8d640c2debc18a403b750a5ee69bd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372669397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6405ec487dc34ccbdc687f1e61d093d714dda4add87ff3db3ef75cd70e666ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:08:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:15:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539b334e5a1b4f830e2cb90767d1d6bd23065595b3d40e6cd589ec973f33276`  
		Last Modified: Tue, 19 Dec 2023 03:26:15 GMT  
		Size: 64.9 MB (64877294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0428530ea0a6a33939b2c19cf5f38e214292abff9ad746bdc4afcfea7397bcd7`  
		Last Modified: Tue, 19 Dec 2023 03:28:48 GMT  
		Size: 232.3 MB (232306893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1766ed0c020a64b0c0245a19f9ba7a951551f98147642a9acf6ede2115229dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393372396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e24823afdd39ee710bbbc971c39d0aa4ff7fb43aebaf6a79c893b045539c7d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:02:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fb001517f3aa634674774ca44ff1ee072157218fcd0522c1630479101d895`  
		Last Modified: Tue, 21 Nov 2023 07:09:33 GMT  
		Size: 70.9 MB (70920797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b31909696ac928d37c89a4769a0d196f1f4641efdd73d46c6a365e9c76eea9b`  
		Last Modified: Tue, 21 Nov 2023 07:10:21 GMT  
		Size: 239.0 MB (239016768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8da7b54261080b809f45176c4399c2a846f298c5dca668c5ef9d891960e05619
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.9 MB (435912718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66322a3b41a21a07cd1c50aaacb0216d49a586c240665706c1eb10bfe1357d36`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:41:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe6c23c39483f54e5cc09f3805cbea29d02f6bbc773bf62d752dbdc74d194e3`  
		Last Modified: Tue, 19 Dec 2023 02:43:08 GMT  
		Size: 65.3 MB (65295558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cdabb923ae43d95eb49f5a86e41045d58be42c151b0890419973020357d956`  
		Last Modified: Tue, 19 Dec 2023 02:49:01 GMT  
		Size: 296.6 MB (296602883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c93fc2e94d1d3a26456ef129ab582ef7d63a767ab8762db8940202c77f1388df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355072174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc793a1658b88281067a4063d6ed988d648fdb13eb5611f6e42534971d82b3da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21db908a00e81480eebf3fad2c4e13874394ba9f9978d3ea7677d3be28b4fb`  
		Last Modified: Tue, 21 Nov 2023 06:18:18 GMT  
		Size: 66.5 MB (66490545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d423dea4ea04d9998b72e9dca146ee1f13e78ec50b02fa0de85998fc82032b`  
		Last Modified: Tue, 21 Nov 2023 06:18:48 GMT  
		Size: 211.3 MB (211321007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:4a430ed950cc4b98eadd6279ed85deb6a30b8c1236ecce50f607fefda69410cf
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
$ docker pull buildpack-deps@sha256:7fd071471c070146e579b6e18e3385299f6bd90fcdac5376a06e689a769d5e9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76013319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c938c72d716541c88f972961bbd785d121eb6be6212ee7519eb38483bf81aff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6619eb9db222bd053555e7cb22ca730e3186bd13c78473a06b5c617036fabc6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72177696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be421aff42b9b42179286525e3b47418aaf1a1c3514b8d81c7da8f912e66bfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:91852f70f0cc52e34e2337e46e2299c93f1f788c16ee5355947448e4b95aeccd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69898251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c0e073649b042ef2a2fe654648e05461d464a86fc72415260cece782621787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7d94a1efff10fcb19fbd83cfb66d8d450a7ed085c20a21d34777ddeea944d677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76614270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84f666bba1d3f33d489b7f1ca30183b36b1949707e4cfcc5b70fad6f28dfe30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f5bce5b2a812ac3e4d477ded664ef22b441a4e04cf273a87c312d5ebef7ee6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78002695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0b69328536bca8f709bb9cbc16648970c323d17878bc58bf9d30c585881148`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1e5bcd2de6aac0d979e9e3ac7288764dc6ba5531745b4ea398fcf254dc899375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75485210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6422bcdcce20e3e6dcea181aea6a3ae12e19f7ed14a04a35cd8c79a1f6a07330`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bf7b2c6f20aeaa97efb86336a12338247f96a743fa032cbb6e848100e365d25e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83434831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e185b08bc814b3731dcb7aa4ef80f272175c6d3715e08afb5a280d02f76715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e2b661dc9029e826be1456b9abde55f5a23438a6f9f7ac222510e045a0d9f8a
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b585177a3343949dae98f8d0e2e5591bb16fa3a41b44d130e49941538583ed42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:132caa5f4dfbbce1e1f7a982aa07300d03415c825ae2ba80361c5c01a31e8332
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77260622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e28664175d244c1cd5e4e6f02cccb38f1c27e640751ef1722a1529d588c2a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:8db8de49bb5c7774ab4edafa8e72f9481ef5af1fe1f8b79412e95874a398250f
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
$ docker pull buildpack-deps@sha256:e0d5e41352ab8cf617b9920e2249a5a53258e38c0a21a33e2c18993575ab51e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142062356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a979ddc17b1169bcd0e7d369cee427e20e75db30073643f8df8f9d1443751d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9565a064a4e2c8d2e24ea50bb5793fd5453d880cc1268075d4c95136016c2`  
		Last Modified: Tue, 19 Dec 2023 04:44:29 GMT  
		Size: 66.0 MB (66049037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eda7ad1c9adf08141546487b4ca131c7c951de47acff64152d95db04680b52af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135854704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd629151c9a68becd2cd8cecc176f909736db356d0d4889c5700cbd713dcf67d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43bd039a111ff18dd0a63cd13a31d9dd641b36941ebd1cb91eeac6d9cb35d1a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130513940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ee8381f8cf9588f0e2a248e8ff70be2963e34f40b9d56f53796168d3f1103d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7a5eecc1f0a2e75f1dc4cc1953feec4555e8fb395f67d882284d7c17af33c`  
		Last Modified: Tue, 21 Nov 2023 14:17:25 GMT  
		Size: 60.6 MB (60615689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:af589c91ef37d6c32116a1b241e4aad363808ff422474ba16f569efd841b146f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142225783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222f9f3797f956ce854e32cffc6df6746b36e71ec083ec3b8e35759cf731ff9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a3b26cecdfe35cedc579177de975c502073e0ec3b623c7408d7145436fd16`  
		Last Modified: Tue, 21 Nov 2023 08:08:57 GMT  
		Size: 65.6 MB (65611513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b403e321a12af49825b52173de020258f34e044645d5b4c7e407638600344d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145812346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c0378b636a237178ce1710b59568f8522ef9de3399ff88454c0edb618c2d03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e5706d82a57d517f5b2faa92178f9346b9a474417ad5a9158a842164e920a6`  
		Last Modified: Tue, 19 Dec 2023 03:40:36 GMT  
		Size: 67.8 MB (67809651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7d6b57ec0772da03f76089453b7948af8001f2b7c4cd6275133e62771f6c4842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140362504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268dd58b533640c04942005a5685b8022869bd3c3cf19a393c854217f467a20f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:08:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539b334e5a1b4f830e2cb90767d1d6bd23065595b3d40e6cd589ec973f33276`  
		Last Modified: Tue, 19 Dec 2023 03:26:15 GMT  
		Size: 64.9 MB (64877294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:24a7862e93585787852dbaecc311fe50c85ca997c602ae777a5a40f37264db6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f839951b7a1ec1855581f34657a10b0e452a76662c147f9893fb5b4b1355743a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fb001517f3aa634674774ca44ff1ee072157218fcd0522c1630479101d895`  
		Last Modified: Tue, 21 Nov 2023 07:09:33 GMT  
		Size: 70.9 MB (70920797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cab57db4abded03a615cdeb1b61f19d471f83b61cd62d49fe9248e47afd5ddfa
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139309835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b18f767be5d0b44739d653a26034dce3433781c850d7429a89e91f08e6aee7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe6c23c39483f54e5cc09f3805cbea29d02f6bbc773bf62d752dbdc74d194e3`  
		Last Modified: Tue, 19 Dec 2023 02:43:08 GMT  
		Size: 65.3 MB (65295558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1769e0bcb2fe395e6ae63c7c91bdeee37003e88269a8db80d927a4fc64840f8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143751167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47000f61dc60af3bdb834e3d3470c752ac2e6269191cb531d5f7264a413791e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21db908a00e81480eebf3fad2c4e13874394ba9f9978d3ea7677d3be28b4fb`  
		Last Modified: Tue, 21 Nov 2023 06:18:18 GMT  
		Size: 66.5 MB (66490545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
