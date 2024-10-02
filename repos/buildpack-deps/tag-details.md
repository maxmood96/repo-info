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
$ docker pull buildpack-deps@sha256:577e9ec16adb3b259f47f6a443b588ddc18c9447699b5fa54133e9d74439d8c0
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
$ docker pull buildpack-deps@sha256:eb005d096537f6e0ce572bf7db414d7ef175ca02ac242164d2e94d4f9b3d36f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245815416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4661b4b35b62dea52e3520bd8834eabbd6276945b919687793bf05630ebffe56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 02:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411f4debc2af1b53b390cebb61b5125cc06e081e824a5825224cc682c2bf773`  
		Last Modified: Wed, 02 Oct 2024 02:11:09 GMT  
		Size: 60.9 MB (60924590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d5f36cdada3d609f453d228d3262e60f632da905b81771514003a0d9693b00`  
		Last Modified: Wed, 02 Oct 2024 02:11:35 GMT  
		Size: 145.2 MB (145157943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:890d20d508d983eddcc8bb370f1ec5ef232f755c1ae7bdeacab51225f8cdd7a0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212090368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f3cf6c925c427d77bff997e5b970168c2269fbea26b09bd8f49aef7de94b32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:32:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60e2872eabcd665fccca4b65322b8780ad6b271f98a487b9d013700d8c5f24`  
		Last Modified: Wed, 02 Oct 2024 01:43:08 GMT  
		Size: 55.9 MB (55883126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8b0b9aa19777ccae3558e0bf4281be454586399e4a494e29f10828270f6c8`  
		Last Modified: Wed, 02 Oct 2024 01:43:35 GMT  
		Size: 122.0 MB (121985340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ee373c089e904e2b6531ee023201499d123088fb160e5333f79cf9858338a7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236099455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b77f0d460102e798a3a9ed12bd7a1dcb2a8f060d85b79ffa409534f7681a221`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:06:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670a3422be6c3e543f9ce6d7faec576205d847616531df1aa7e2a7eb4af90ae`  
		Last Modified: Wed, 02 Oct 2024 01:17:37 GMT  
		Size: 61.1 MB (61063346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7348dd49b23e004a903fed62d36d6a335821d58d4c8196cdd32e8c24840d43`  
		Last Modified: Wed, 02 Oct 2024 01:17:59 GMT  
		Size: 136.8 MB (136838946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e7f3381b3131a78f99e6b193969be1bb49322b125ccad189f426f9f2a93d0db9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269578591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518bf3b5b6d378150338db41dae26967d4a3170b9565fd47f9c1e96c5fcc266b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:42:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade1a5274d6f1d0318337f54ba1338a12318fa208dc455dd515fa9ef53b0e5a`  
		Last Modified: Wed, 02 Oct 2024 01:54:55 GMT  
		Size: 69.7 MB (69663914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1528d9dc1802d58a5a717971d5fb1f5c987182703dfa1609978c2eba47dd7db`  
		Last Modified: Wed, 02 Oct 2024 01:55:27 GMT  
		Size: 153.6 MB (153635944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a23422a64432cd7bc640957a0ef9bd2dbd4c6c34ef94f32277c1438f12fc9cf0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226626818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab10d23c033224e1244ef269b5526124d5a44516b29e8802b4bacd8c38417de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:30:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e411b5e611b843166f906b0c9e1fe81a442e2896e3ed2d11bcc79eaa131eb0c2`  
		Last Modified: Wed, 02 Oct 2024 01:38:47 GMT  
		Size: 10.7 MB (10705562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bfeb71e62b9e0d28b328d69d7eb15fec4de57186b9bb2f38b4d793525ed453`  
		Last Modified: Wed, 02 Oct 2024 01:39:00 GMT  
		Size: 60.4 MB (60354960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed2f074058303c8c52d6bceb8de4cbfcf06f1f1eb813fd43fd4bf7b2ce959b7`  
		Last Modified: Wed, 02 Oct 2024 01:39:22 GMT  
		Size: 128.6 MB (128553976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:61bb3de1b71b504f10b19eb1a1d3484057d7cf84fb01703c86d20c77b1145059
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
$ docker pull buildpack-deps@sha256:b04185df0458f8714f540b4175fbe617a7702e9c1b48638960051c7dec5cd92b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39732883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940d7e2e113e4fcec4495578013dd4b911ce74893c731d4a6ccc0eaebdf54f60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dab2c53045177f347ab34f1bbe87a35ed7b6e068702ed7e9d067ab8c31247b01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34221902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedd5fba35b00db65f8f08ec4cb4795a6a4a885b660b03123833453aff7a0aee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7c49b92e6e731da55707dfcbfa37bc2d1cc589c202a9d48a264372103ee88527
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38197163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f318f15f592da550e713fddda1a5d88bdaab5e08a0f863fd7e2702ab6cc3e84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:85a17b2741f19d79fe55d8ef050629d032ba7c9126946a643d33ebc0c743a8ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46278733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fa1feeb69f1b34be579bab607d1be14a5b938fa5d67e0ad09223b8d8355b37`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:affd261433e068060b2909589ae53ade8f9d03bc0c513517e78c02a613e9cdf1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33886911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6cc75e4d9830a411550b57eafb957f4df14ef2b1534e3c21ad5964d3bcf8f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:44:06 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:44:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:44:35 GMT
ADD file:2b79df939efa8d17a9cd9432bbfe34fed1d540f46c23529b1cdab31b56362460 in / 
# Wed, 18 Sep 2024 04:44:37 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:48:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:304b7e8d05828d18c71c5dac4c2a30c8d5f9ceb02888ac26bb8065157d250996`  
		Last Modified: Wed, 02 Oct 2024 02:11:36 GMT  
		Size: 24.2 MB (24248318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf8fb897037c00782cd45fd16483b13d79bb259031660d58a354790e08968e`  
		Last Modified: Wed, 02 Oct 2024 02:11:27 GMT  
		Size: 9.6 MB (9638593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d83b15406fb31af647047d561e4c9771d45905ff710eb144ab9affca08462db4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37717882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc7bc96c10ec9f4c7e373c4a67fdd52bac65f8579d7e1987c80b00d4d57baf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e411b5e611b843166f906b0c9e1fe81a442e2896e3ed2d11bcc79eaa131eb0c2`  
		Last Modified: Wed, 02 Oct 2024 01:38:47 GMT  
		Size: 10.7 MB (10705562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:7158ef1f084f90c6d88fcffbcb5cf8d628efdf290b5f33de5877adbb0bafdb5a
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
$ docker pull buildpack-deps@sha256:24fb1d94cdeb62452080ea88d57009d977d0ebc6145bef70b355217f0c0f3fe7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100657473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec521d79a736d2c908b76567cb34fe6800cda4cf11dd3425c35d5e57a60824`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411f4debc2af1b53b390cebb61b5125cc06e081e824a5825224cc682c2bf773`  
		Last Modified: Wed, 02 Oct 2024 02:11:09 GMT  
		Size: 60.9 MB (60924590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c1a6e7fff25cd5cd4577d9b2916182b135715d9a80b65798bd9f6957a61933e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90105028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2c2ac3150f534f92f33ffa953a9903dc97fc9d4ba861bf839905461129eb86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60e2872eabcd665fccca4b65322b8780ad6b271f98a487b9d013700d8c5f24`  
		Last Modified: Wed, 02 Oct 2024 01:43:08 GMT  
		Size: 55.9 MB (55883126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:27376f7d6da57e2d59d855f0c64d760261b3582adb037e2587288b0fb5544370
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99260509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3d9e73afca1925b94ce7e6fd49da77bc0b0c88092d11eb22c98ed3a65c5436`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670a3422be6c3e543f9ce6d7faec576205d847616531df1aa7e2a7eb4af90ae`  
		Last Modified: Wed, 02 Oct 2024 01:17:37 GMT  
		Size: 61.1 MB (61063346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7af077cdf974af9fe86ec9e2172292e1c3e38ab8fa006852a21ff906b43d08fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115942647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16138b3caaffcda0cd765a593a804d16d4abeae15bc694284c03ac99ba2e3dea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade1a5274d6f1d0318337f54ba1338a12318fa208dc455dd515fa9ef53b0e5a`  
		Last Modified: Wed, 02 Oct 2024 01:54:55 GMT  
		Size: 69.7 MB (69663914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1b427ee95bd906312746d3203eb018c28f5186ea236e3507be409bb4fb6d96be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98072842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4e8d795d898f8f116f1078c6d431fc56ea277ebac4283067aec11efde7376b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e411b5e611b843166f906b0c9e1fe81a442e2896e3ed2d11bcc79eaa131eb0c2`  
		Last Modified: Wed, 02 Oct 2024 01:38:47 GMT  
		Size: 10.7 MB (10705562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bfeb71e62b9e0d28b328d69d7eb15fec4de57186b9bb2f38b4d793525ed453`  
		Last Modified: Wed, 02 Oct 2024 01:39:00 GMT  
		Size: 60.4 MB (60354960 bytes)  
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
$ docker pull buildpack-deps@sha256:130fdd43b7f7182c2170e5be91becaa74d745454039e538299edf24e161fe59b
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
$ docker pull buildpack-deps@sha256:855e41565da34c0d899e593b4b65b2b1b3b63b04a0e5f434237629a7be422d9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280279727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec47e3865af2efe637625905d89dd33956fd36c929ce0e5e6d90ef8651b20af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:06:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f61a75956927ffbc601ace40bf7d9a2809e8f42f4b39f62b33f55508f1d0ad`  
		Last Modified: Wed, 02 Oct 2024 02:12:01 GMT  
		Size: 45.8 MB (45806658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec7556ce197095176d9c1c0a174299aa49154b2129be4a2b1c22f9702b9cb97`  
		Last Modified: Wed, 02 Oct 2024 02:12:33 GMT  
		Size: 190.2 MB (190244412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8beebc65116eed70f3d544e3e5352f798089b6589e8d0c88fa42ade8ccddb066
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240482827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40701d330116b48ea1af39e23e23e04c26ea4436a61bd0577d6796f6573a984d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:34:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:37:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb119f1d99566ed1f8d8fedaee28a2280adac0c223ce200e7777dcffec00164d`  
		Last Modified: Wed, 02 Oct 2024 01:44:03 GMT  
		Size: 49.3 MB (49298840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866fc43f033b51c1a06c3f6d07cf03de9e6190f7db0f4095112e514178858c1`  
		Last Modified: Wed, 02 Oct 2024 01:44:32 GMT  
		Size: 150.7 MB (150677473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e8de3ad24dac6c6cac494b4814e26aef75b307d664b6b2686340d9275cc9028
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271386929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258dd1dedbe32e7e1ece435c11db9077d0b9a7afcc0b020f4a760a4d2e608478`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:08:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:11:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6108651e89a3a91252dddfdeef0ab0fb469fb24f4de592a5944ffec8fb73f0`  
		Last Modified: Wed, 02 Oct 2024 01:18:24 GMT  
		Size: 45.8 MB (45769072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c427e7a315343f68b951b898d838e339e728f26647e6f21415d0406eb721ab29`  
		Last Modified: Wed, 02 Oct 2024 01:18:49 GMT  
		Size: 182.2 MB (182212309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3e6933bebca2224bdfb0f4848a3435f195e74753cab3f7ba314b32dab9fc60d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299165270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d25c8992edd3b648955db835b81ab65e652a274fb0f86f982ed29f0a0eb035`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:48:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e7171ec073330607865d4617beab15833dbc3b9a901748567e8cf863a6d11`  
		Last Modified: Wed, 02 Oct 2024 01:56:00 GMT  
		Size: 51.0 MB (51025292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bbb7d91dcba46580ae17389f5d59fa785af55f5c82e484aadbe29f242438b`  
		Last Modified: Wed, 02 Oct 2024 01:56:37 GMT  
		Size: 196.6 MB (196631172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:45f3312e6c2a729d57cb1f2b7610fb271b2c90321c7640ab9cbfb34346af7dd1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330651353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4858134d5a2db71f30a48e380017fb3484e7e002a7377773dca02c81f37d0bae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:59:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be136966d9b6f5be3f056d30013c4a4cb14f67709ef491a0319722e2e90095`  
		Last Modified: Wed, 02 Oct 2024 02:13:09 GMT  
		Size: 54.3 MB (54279540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df3932963d582081c4a83ba0f2ceac2157bf5102dbf61dc9d03b1bdd38f81a5`  
		Last Modified: Wed, 02 Oct 2024 02:17:20 GMT  
		Size: 230.1 MB (230105741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cc54f4891e70f65caced3604292265dad8d5946d65e7ffada45cbb26684ac156
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262342634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea52845d53e314e832d3d992b6a7e783c248355f8779bc05d15405210f16ab5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:32:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:34:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6058811ca71a5dbcf8603e3abea065f2302f30fff37e9cba98068af6b0b0fead`  
		Last Modified: Wed, 02 Oct 2024 01:39:42 GMT  
		Size: 47.4 MB (47408365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb7d36f8e577c791f1b0efcb5d6c1678e4a4d5c1b90122e5762820eb8b97405`  
		Last Modified: Wed, 02 Oct 2024 01:40:09 GMT  
		Size: 169.3 MB (169292965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:00ce9a522e9b96a06cf9c62ed5f886a086452de5fbe729817b22742d97ba27aa
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
$ docker pull buildpack-deps@sha256:2b5869019aea04face8fc1f58ac6e34aad6762c57822fd818b69b060bd4fc7ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44228657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be742ffca4dd43a363aac7275ebf6e97ac5547ed6bda6766fc42e2070e2b249b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eec735e64d7c2150361d844efc23d07624aa56d1a543ca65bf2fc0f9f675b905
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40506514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37404394553903d1b91235398803dd2638432faec207dfee4ba58a7fb09f956`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e020fee9857b1e24261121e651e2df6156cf76e644e80fb574a4ffc798975a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43405548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b9fe779bce78d95b027b243263b191a3715452165d409c2e1b55fbd47f6528`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eae46c940ffbdc3ac168d6be819cfc19265a43cbbc5748d4bd943f6cfac7ad19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51508806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640e48b20c33f7e1ca056bef068e19aa228353229d915df3c63db96930181b67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:96cca7615cf23168ee927a322ae7d73794d18881edcfaed32a1ecfc82b2bab1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46266072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb9816d3133f9b56df724c02667b50d24d340ed5af45ab422f3ac06a48bf4ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bb95a5db87c595c9980d507e5524a0725155d84f11fdc1a9d79ca26ff3c691a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45641304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe721fbe62ad193a72dce2096351fc2462cd3129a3257456d227bb4914b5df3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:43615a08e39277ab1351782e2eafc39ccd8f669aed6312ca55a1d6bca578bcda
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
$ docker pull buildpack-deps@sha256:c3466200f8283bade92b93dce4e91901b8ef6cfdc05358c7ff1b06693c13cdd3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90035315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cbeea6df9f212bbfbf2470c165d7e871b275988cedd5735ae00d4dc44a3cb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f61a75956927ffbc601ace40bf7d9a2809e8f42f4b39f62b33f55508f1d0ad`  
		Last Modified: Wed, 02 Oct 2024 02:12:01 GMT  
		Size: 45.8 MB (45806658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b6b8a896f838c1a87984cdd62955b1c525341af96890e86eba3c15087180f40
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89805354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91815d9b10848c23757aee3d650bc0cf88b678aec7aee46e0e467cbfa015cc1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:34:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb119f1d99566ed1f8d8fedaee28a2280adac0c223ce200e7777dcffec00164d`  
		Last Modified: Wed, 02 Oct 2024 01:44:03 GMT  
		Size: 49.3 MB (49298840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2752d5704eb5d48def6e45444720a7a6ecb74d065da6da9799f289d6248b01c4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89174620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b1d3be232034ff96943a9f18661af6bfd31326f0e935f3e664635ab3a2efb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:08:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6108651e89a3a91252dddfdeef0ab0fb469fb24f4de592a5944ffec8fb73f0`  
		Last Modified: Wed, 02 Oct 2024 01:18:24 GMT  
		Size: 45.8 MB (45769072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d4f2886afb48df4227a9956b4776266c0f8653040343fcab7d5f23716773d70e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102534098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301a9a27368e19914e3fc6387aef8995784aa499e48a3a361babba0a5d8e900c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e7171ec073330607865d4617beab15833dbc3b9a901748567e8cf863a6d11`  
		Last Modified: Wed, 02 Oct 2024 01:56:00 GMT  
		Size: 51.0 MB (51025292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:88f18425ee4d26a46b4c70662b1293ace4c09b92cc7c8f3ab90dd3e30352fc69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100545612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b14e8dfaa42499d53c1b9b3599066b7660fa86a25ec8cc641cd117ea3cf26a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be136966d9b6f5be3f056d30013c4a4cb14f67709ef491a0319722e2e90095`  
		Last Modified: Wed, 02 Oct 2024 02:13:09 GMT  
		Size: 54.3 MB (54279540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8ae431968b6acabe2bcd26a8779708c25071231c17e481cc27050296369575da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93049669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d350c9144d363bf55139acbd3c4c1c48dac3b6d07a535382311a763eaa4270`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:32:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6058811ca71a5dbcf8603e3abea065f2302f30fff37e9cba98068af6b0b0fead`  
		Last Modified: Wed, 02 Oct 2024 01:39:42 GMT  
		Size: 47.4 MB (47408365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10`

```console
$ docker pull buildpack-deps@sha256:0b2a42bf0df7f6ae23c9bee2cbc5dbd11e492eec2f0a65488f49f2ca60278764
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
$ docker pull buildpack-deps@sha256:1f39714b7552ebbe1d80a542a4e764ec7fff0eeb5ff155e5305c836b8e1bde6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293595121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd75f501048aea4153cf8a32016424ad5641c82b7450e1e602fabfc68f972d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:07:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:10:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba6e5f3d90cff89eeec5ed07e205cd2b78e8e111454ee7cfcdf300bfd6122d`  
		Last Modified: Wed, 02 Oct 2024 02:12:59 GMT  
		Size: 46.5 MB (46504774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b191893e4ede174d5397194694c3780fcc1122cf4a6798dc746a28b5b8090ee`  
		Last Modified: Wed, 02 Oct 2024 02:13:35 GMT  
		Size: 194.0 MB (194039068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2085016390fa315d8ae35cb1d0896be3d5d902f2c7b553376d3e9a259df11c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257295116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b4c9ee67c97324ae0cba8cbe153b91c3452c4a67125059a3e3636c350f9aa9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:42:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf4c374ea7ab02bd9e1c077c3f4295612de66efa2c54b41fef14db04e0aead`  
		Last Modified: Wed, 02 Oct 2024 01:44:59 GMT  
		Size: 49.5 MB (49478102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a543e4a77995b18667e3ce720c44d3f0e07160a7e910559184a9dd7fe0bb9484`  
		Last Modified: Wed, 02 Oct 2024 01:45:28 GMT  
		Size: 157.6 MB (157603332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9080b3fa5c7e031077d09cd1aa67f9d05d99a53aed134674352053088aa37937
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287690780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a835fd6185ddf21f8309db2fbf6d7b6eececcda785fc939aa3f1dbf5a9fb2ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:16:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeccf52d0c7d95f1cd621b4538c19cfff5867e52d01d5a00f759a459ea28999`  
		Last Modified: Wed, 02 Oct 2024 01:19:14 GMT  
		Size: 46.4 MB (46434300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925c4202924345a21194a077f853b64ce8ee8e676a6e91001d61fbc28dad6ba0`  
		Last Modified: Wed, 02 Oct 2024 01:19:40 GMT  
		Size: 188.3 MB (188255082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d2786b9534cd8ff21466912c2ae42c51e750cf7793219433622506e44175cdb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309380326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bc9f5ab72cde0cb37715560656f77831a32ee257219f9c207b0ee8a3062492`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09f090381214fba1abf5d6db78c3189b6ac1fc85765a40e6be5d83b7160a433`  
		Last Modified: Wed, 02 Oct 2024 01:57:09 GMT  
		Size: 51.8 MB (51772787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce954ce4c7e576b190694854b8f4ad4e44769c2ab96b6082ebb32f9a11300207`  
		Last Modified: Wed, 02 Oct 2024 01:57:47 GMT  
		Size: 197.7 MB (197707907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5dbad1736e445c9255daedd2291c1ed47071678ec62d7597c9bfc2e6151dc4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387512083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d6847932498e61a798352ad0688d37e20d3985f1cf61de61ff856afb6b0c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:10:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b19496a8d9dc226b4d60c0384e37525cab9161d87adbd6637828dfdeb65fda`  
		Last Modified: Wed, 02 Oct 2024 02:18:51 GMT  
		Size: 54.6 MB (54636883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1257422a528ad068c80493bd9a6a64aeba863bbaf8a67d7570a247d274ff1c15`  
		Last Modified: Wed, 02 Oct 2024 02:24:08 GMT  
		Size: 276.1 MB (276124113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1b94bfaa2e56c7aeaff52679ff4779a169746a2e6cbb4def3d569a168e7f1f4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271908522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543c8cdf61067f50de3da9ea6a9ca70cb685f31fc28f2c8d4858b1aebc73e8ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:38:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f66afb7703de047378bbcd7202a18143aa8936962a5cb32c6625771ab85206`  
		Last Modified: Wed, 02 Oct 2024 01:40:31 GMT  
		Size: 47.9 MB (47891767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f9b9a4e4d09843427eb68bed83f636b885ed208222043fe011670735db076`  
		Last Modified: Wed, 02 Oct 2024 01:40:58 GMT  
		Size: 170.2 MB (170171054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-curl`

```console
$ docker pull buildpack-deps@sha256:6499d16a7cda6edff74057981ea079f60738ad77655cd907049aeba1a3ae3ce8
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
$ docker pull buildpack-deps@sha256:43b36a5d4a544769e661359e4e9dede556771f8ac92c429a57dc62fa2cf69767
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53051279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cc0a3c2e25179d44f2a2b5542d854c52a61f5542608fc9a3b5f3c777ba83cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e5ef1ba7f72f74676ba3892c089ebd477003f69f394da04c2d5211aee345014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50213682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4120e010b3cf1347291742619438cd108a3202db2f105c8494bddcaa27fd5c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:14343f47d7690d366becb1a31403f2da6635e353263c0e0a268d6878b9d58eb9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53001398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e9a04501ce3c5ca1857dfcdab71868740920e9a238bf309f66560966c87ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0add5043015ef28f13bf6510cdd61812afcfe42c8f6c521ab9e9aad429887bc6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59899632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08108f3916d5257faed3846a0279abd43a4276137b0f83fcd33fafed745fcb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7ee40875c9bae0d9749f1240b3254b301a55e66e8f459064f75b40639506389c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56751087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2f966ccb05e961221b21a9db2d61c2a852abbe4fde1b1f73c04f1efe11b97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e0f1452312d316a117afce07d8b75245eb486a85fb8f35d4984727862a191429
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53845701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05be1340e4a56fff7138df8e2c81507408fe5ba9e4691ff6391d881041b7672`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:24.10-scm`

```console
$ docker pull buildpack-deps@sha256:62089f7b5997f0efefe64e81ae10ac6b840033070da4112ba5a2bedf25238e2c
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
$ docker pull buildpack-deps@sha256:bd46e031aaa9c9f1dda73d5e59905fa47de82a688d385741a17fb1bddf9df407
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99556053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a96bdc66278035d3d259d9f0a207a9bb529132142715c1cf7f189e5332c574`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:07:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba6e5f3d90cff89eeec5ed07e205cd2b78e8e111454ee7cfcdf300bfd6122d`  
		Last Modified: Wed, 02 Oct 2024 02:12:59 GMT  
		Size: 46.5 MB (46504774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6d3a96e2c941240fc90a61957f6267394476b470a1cdb48c877d7f95a9dc9317
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99691784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442ea755cbf1609c90ef5c5ee53c31cdf810ba83d8bba6299b7bde26969b131d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf4c374ea7ab02bd9e1c077c3f4295612de66efa2c54b41fef14db04e0aead`  
		Last Modified: Wed, 02 Oct 2024 01:44:59 GMT  
		Size: 49.5 MB (49478102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb51fb2c38fa781af7438d1b645ce1dbfa44de5e86b8bd6104587e791d9984f3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99435698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090ce4830fc911c60fd6e58b546d0111feb03513dd571a5616c8630899a56cf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeccf52d0c7d95f1cd621b4538c19cfff5867e52d01d5a00f759a459ea28999`  
		Last Modified: Wed, 02 Oct 2024 01:19:14 GMT  
		Size: 46.4 MB (46434300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d7118aff43ad9d0f937e5d9dd9bdac8082f0fb7d8e7e84347b52699a42558bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111672419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576fa791aeee9f8936c231826235059e4e789e1c71a4429251055a9ebeea4e18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09f090381214fba1abf5d6db78c3189b6ac1fc85765a40e6be5d83b7160a433`  
		Last Modified: Wed, 02 Oct 2024 01:57:09 GMT  
		Size: 51.8 MB (51772787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3f5f0ead2ff3ee3b884d099a66b85cc8c837f0e4b36cb485e3af599fbca9e631
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111387970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64f56c2dd7d2477c02dbfa01deba2aa40ee679b53de609c730d2b0333d1bea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b19496a8d9dc226b4d60c0384e37525cab9161d87adbd6637828dfdeb65fda`  
		Last Modified: Wed, 02 Oct 2024 02:18:51 GMT  
		Size: 54.6 MB (54636883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:24.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e30a832eb8441f147f02a188f52ccfd9fd34cbd8cec1953bf685552cc4b5b3c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101737468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1955d1d0bc03b7553c28e79aa0e49d120e72888356f86b52e496ec4c280c05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f66afb7703de047378bbcd7202a18143aa8936962a5cb32c6625771ab85206`  
		Last Modified: Wed, 02 Oct 2024 01:40:31 GMT  
		Size: 47.9 MB (47891767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:b764e1843f0b1bd2c7b37890ecff7fde2e4029b5e0ec589a1b255c0aba14508d
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
$ docker pull buildpack-deps@sha256:844abe43b7f300a180baeac94b0c7249cdb2f9f8ff3a2dc57c9483c3f28cb2e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349266065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f0102621ef1c91910324aaf53c1ffd78d7e5603c2d04f1b764cbd4d8b129a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d76f36288a8f45e858f9fff3920870a2f9b74a14ca3b61e9a95b4b6527323a07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316614016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a232a96e83f21c88fb15629e06a0604433314593bf2627ed4ab05befb77d05e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:58:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f621479573c327a4dda6b206f9b47e39026965bfb7d15fce780cfaea574d3`  
		Last Modified: Fri, 27 Sep 2024 04:03:45 GMT  
		Size: 62.0 MB (61998895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cfed630bec1a9dd2e2066da3e9ed425e619a1f794f8d9fb007c9224e134110`  
		Last Modified: Fri, 27 Sep 2024 04:04:19 GMT  
		Size: 184.6 MB (184554977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f90161ac2d7576dc819ca336190bc7a58a30ed812ca9714aca4541cd7a68d039
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301953065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450d081e2a32fb58c4bfb86035712433090a7726b40c58fece913c5b45cc1fb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:31:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d1155f47c5da74e62e760752114224ea723a8e594aebd7127329bb894a726dc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340180343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5d6bbbc780759c6ab0b6e84df986cfc74fa4961041bf0199ed0251582056fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d9846aa188aeb883a2832cd89e18999cdd6729abc5b19b781876c770432efe1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351865345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d575f61783f4cdab2d23ccbc14b5610c09708882da9c57fbf8d6f98678356a27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:00:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8fd2b0b6bf6600df9bb4a82d28d3ada17089cf6f175d29438a9e261fad8beaaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326330870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50823257c59f5cfbaf625f86fa64f2884bff4c295bcd40d84fe24324b24f8a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:40:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d744aaf940b526bb655f61ce4b295946be2cf4f9cb1c458cfa98d78183b03f03`  
		Last Modified: Fri, 27 Sep 2024 11:04:25 GMT  
		Size: 189.8 MB (189824612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7e39a67e545d21d8f3f87de8b89a94edc277cf523dcfb745febd8b8a5f1fd5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363380577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fde10daac6379bc4bfccf0270f2e63f0d6132a5dd5cb5c3106f78e245323ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:57:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a1d5bfc66cab4ba82e33b861964feadc27c2fc3ad6fbca3760a165bd4f3b385e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318773548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05aaec9dff1556f3677977bd7af301d5958a0841ed2a6b92fc7a543482763416`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:14:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:d9e45b933e88fec1af990490ba945719590f1b2b8b42e0d5937fab474bfb95a8
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
$ docker pull buildpack-deps@sha256:7cd34f6aa61a3c733d424a74dd7d74f5ec07f352826096978c0caef6e00fc5a3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996740c38dff205ca2785ba2a036ac963aaaa228c7b151b7eb06b9510cfed533`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:55cb1e4c19e4ce0bf8befa213f443a1cb079258b37bd96fb93df8753f205a6d0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e100329f986eee8d9fd68f61fdb0de4b3022de29cc53aa9e11cc1ace15686c7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e0103df7597b5a1f58d3340652fd4e2ef182e6f3a4e6d50504141d699a85a95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20b8cd6905490f862d25ee649cef83b5c280b42c9b126a402618bb337a7d033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:07ef2b337dbaa3b24f512765d8647a4b18100d8c964ca1837bdc3c252771f671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0765495cc8e1d55218a919fa0964b0f2ba70d1835cd38dfbc39a578bb7eed8fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:357d8038f8b2afd5aa2ce4df26f984cfde01ceae64db1a57631d38c0ad688960
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75472063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4269028d3d3cec5a247eea96f8ebd805d13a843ef53aa83d7620a96109780c23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c27d7e6ddf0c975659df682da2dd95cbfd8d688c04bae878dc808ad8bc5473c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73208962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3bed2fbe01889b0dd4aa1472925c83f532d87d6ce064307fc1b580f104e8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2a34312a58e86dec2a572befc36ec41429bc23eddddee1f7df8a1397ea45568b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79265358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7d7ae581ca969b11912d5321c5bdb01df75c5a86ecd4ac4dff87aae8e55cd6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bc324164742dcb747c497b6e48d8e1b6525531ba158618a3ebc7811fee22e71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71990644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8261d005fafe79e46470e17827e8110c5b219222f828faf2c1bf3fb82e0a5575`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:e11f406032a4d2feb352cb67eafe24bef8fe34e694f598d0e89d27765a03bffd
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
$ docker pull buildpack-deps@sha256:cdeb27a4b786ecd529d4ba561a21636f9f2c12978106fdfd0c251e7688d4d4b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138000423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256f5d3f483568706fb9df2caac236da768819cf28455c6c0c0d557f6150d188`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b4bed19797b1a45bf83aed141a7c5c840df6e86c5b5df1fd5849547c160a11a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132059039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceee25cfa608bf7d28af66a01dd3514e68c871aeabb8dac1819da58adf72883c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f621479573c327a4dda6b206f9b47e39026965bfb7d15fce780cfaea574d3`  
		Last Modified: Fri, 27 Sep 2024 04:03:45 GMT  
		Size: 62.0 MB (61998895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69ffd73b6d892f801b4efa09c063974514dafeecfd976c74208a8adb37836678
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126745127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a860569244686aa20ef28222e3cf0f8a3f9a06115043280f1fadcdaf701f6d4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c511f0a2c78bfee9e532c0854584204b5613b96f7fa951fbc416612231899820
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efb79080b7192496c79c55cd230e6554a55fdf5b710985ebf7d23a7a7157ae4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9e62a82d839392f6e96187cbf80a16d2bc6b9f6ee69bb46eaf1f98e18441045a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141683005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68d5203ba4f8ccbd3a59b3be1d5e60b1507280d22bb4093074144b32149c527`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3ccc6ca2f3cd3da62fbba482ae0f7ab4b7e7762149fca5e0bac80c87f62a09e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136506258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4137a21de1b19963fef5cffdc14a7a26f7544ddc4bb934022ca9e06ee08cb8f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b13a20b76943a028b928f105a448b56054d5ecdf8e4df28aec30cb6350a673d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149094859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e8de729db2ff936bca848d32d17073a4be7b7485e28f2950fcb77c6d47b57d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0fca24d12422d5546ec9cf5d31171ea318913c4239a822ce12e7670da6286434
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9af3b078649bdc6f7a9a4152248dd30c88deea81edd802d617a2ad046ac482`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:d84922a7e26145fa71ee524463d90cac8ce7acfd1eca06d55f24e298b3912a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8d488f71540922ed4e5ac79cc16948db7a8e27e55c36a59805e82701f9697f9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322638361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbc4f4afa7a42e85251fcc85d67762b540686b81e5e08338190a107e9b287db`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55229002f3e9c7812c0683243cb3c109a172685bc13b60c4a179ee19cb7532dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3a2ebcacccc6059614008b1907339ca81a687bf111616dc228adc76140a3ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:33:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1a2070b645c8a3f79ee80782704ed85243e8bf44babcae36a54f1853b0dcd51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314282508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b4370cefb3f07fe64cbde2b559cb8b3826c9de7e492b1498a01ce2ef4d1fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6100b530306a52fd78be9546745584313d9e86581e5aed21350078bb708c17a0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328344341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1c2768b4a90b2ddc66844478825f74ac75420e5b0339c6f1b07ca4fd77ef8a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:02:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93938e3248ca49e16485c4e39a8c601801fe32600e913ea08b6a71a42acd7759`  
		Last Modified: Fri, 27 Sep 2024 08:09:12 GMT  
		Size: 200.0 MB (199967470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:39e63076945fb9ae56fddca98857b36940023ba60be84b680722266bee8c6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:493c3a47ac40dfb1b98b81aa90975efaf13260da7541c93f07942965bdc90e80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa31de3a8326a44ac072e5b372515ac96493ac4f6d6f00204179bacdcf7b0400`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0f8ea823454d8e07af80adfe6fc4d2ece17f96c194bbd11f22b5d22e0073a656
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffd1af5abfc86f8ab9ad2686f3ebc030fe4608cdf6e6facd16ddfa2d99ea583`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:842922b68678f1fac48d835049726c5398604b702ee421f40636d9e459d56491
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69483562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e86dfc5995a61ab1d4efcd1df3d5327b56e7039fb319cc94e5e6684cba5247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3d8cb4112d4b04633bb393b5a807b261208d72c1a3b573b4a4bcdd6eccb2cd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5514e433d3d2c001a6ebd4510c3dc44fb6f0134f3609a97d5eb8d818ca95237`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:2150df029cc4842b260b4c20ad9d8efcf1c283618513a2cc9d0bb31293b3cf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:790a36dfc8741a87edf1b09c31ad50381dd38fba5cea5fc6a9b46cee906b2631
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125569359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3ba45f5d00b86b9115a49cb01f515d1d386648325df11100c565089533619e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9d6d31034a1a0cb48093f49f4b1a5783c35284c62f7527b98d0f539d406a4bc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115738618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98180b24df2dae8337b3c1769d35a6fd95901f5511bb29183c2d224404e04899`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df229d9fe9c016f00c1893313e285b7f7d9262d9b81cc8093b37019c1e77e9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124318256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62aed602c832fdcb32fae77caf1c392f521669b679f4e4fc4358f2b528c9cad3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:38f00700b5ccbfcaad7854588ea97bfac8e5cad9f0f95da5b5768e7a4ce43006
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128376871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a3cce83e8b5ea3db5e0f2381970ba23dd139640398efd21fc05885497d2ced`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:d9e45b933e88fec1af990490ba945719590f1b2b8b42e0d5937fab474bfb95a8
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
$ docker pull buildpack-deps@sha256:7cd34f6aa61a3c733d424a74dd7d74f5ec07f352826096978c0caef6e00fc5a3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996740c38dff205ca2785ba2a036ac963aaaa228c7b151b7eb06b9510cfed533`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:55cb1e4c19e4ce0bf8befa213f443a1cb079258b37bd96fb93df8753f205a6d0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e100329f986eee8d9fd68f61fdb0de4b3022de29cc53aa9e11cc1ace15686c7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e0103df7597b5a1f58d3340652fd4e2ef182e6f3a4e6d50504141d699a85a95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20b8cd6905490f862d25ee649cef83b5c280b42c9b126a402618bb337a7d033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:07ef2b337dbaa3b24f512765d8647a4b18100d8c964ca1837bdc3c252771f671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0765495cc8e1d55218a919fa0964b0f2ba70d1835cd38dfbc39a578bb7eed8fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:357d8038f8b2afd5aa2ce4df26f984cfde01ceae64db1a57631d38c0ad688960
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75472063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4269028d3d3cec5a247eea96f8ebd805d13a843ef53aa83d7620a96109780c23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c27d7e6ddf0c975659df682da2dd95cbfd8d688c04bae878dc808ad8bc5473c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73208962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3bed2fbe01889b0dd4aa1472925c83f532d87d6ce064307fc1b580f104e8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2a34312a58e86dec2a572befc36ec41429bc23eddddee1f7df8a1397ea45568b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79265358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7d7ae581ca969b11912d5321c5bdb01df75c5a86ecd4ac4dff87aae8e55cd6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bc324164742dcb747c497b6e48d8e1b6525531ba158618a3ebc7811fee22e71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71990644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8261d005fafe79e46470e17827e8110c5b219222f828faf2c1bf3fb82e0a5575`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:577e9ec16adb3b259f47f6a443b588ddc18c9447699b5fa54133e9d74439d8c0
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
$ docker pull buildpack-deps@sha256:eb005d096537f6e0ce572bf7db414d7ef175ca02ac242164d2e94d4f9b3d36f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245815416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4661b4b35b62dea52e3520bd8834eabbd6276945b919687793bf05630ebffe56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 02:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411f4debc2af1b53b390cebb61b5125cc06e081e824a5825224cc682c2bf773`  
		Last Modified: Wed, 02 Oct 2024 02:11:09 GMT  
		Size: 60.9 MB (60924590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d5f36cdada3d609f453d228d3262e60f632da905b81771514003a0d9693b00`  
		Last Modified: Wed, 02 Oct 2024 02:11:35 GMT  
		Size: 145.2 MB (145157943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:890d20d508d983eddcc8bb370f1ec5ef232f755c1ae7bdeacab51225f8cdd7a0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212090368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f3cf6c925c427d77bff997e5b970168c2269fbea26b09bd8f49aef7de94b32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:32:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60e2872eabcd665fccca4b65322b8780ad6b271f98a487b9d013700d8c5f24`  
		Last Modified: Wed, 02 Oct 2024 01:43:08 GMT  
		Size: 55.9 MB (55883126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8b0b9aa19777ccae3558e0bf4281be454586399e4a494e29f10828270f6c8`  
		Last Modified: Wed, 02 Oct 2024 01:43:35 GMT  
		Size: 122.0 MB (121985340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ee373c089e904e2b6531ee023201499d123088fb160e5333f79cf9858338a7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236099455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b77f0d460102e798a3a9ed12bd7a1dcb2a8f060d85b79ffa409534f7681a221`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:06:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670a3422be6c3e543f9ce6d7faec576205d847616531df1aa7e2a7eb4af90ae`  
		Last Modified: Wed, 02 Oct 2024 01:17:37 GMT  
		Size: 61.1 MB (61063346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7348dd49b23e004a903fed62d36d6a335821d58d4c8196cdd32e8c24840d43`  
		Last Modified: Wed, 02 Oct 2024 01:17:59 GMT  
		Size: 136.8 MB (136838946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e7f3381b3131a78f99e6b193969be1bb49322b125ccad189f426f9f2a93d0db9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269578591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518bf3b5b6d378150338db41dae26967d4a3170b9565fd47f9c1e96c5fcc266b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:42:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade1a5274d6f1d0318337f54ba1338a12318fa208dc455dd515fa9ef53b0e5a`  
		Last Modified: Wed, 02 Oct 2024 01:54:55 GMT  
		Size: 69.7 MB (69663914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1528d9dc1802d58a5a717971d5fb1f5c987182703dfa1609978c2eba47dd7db`  
		Last Modified: Wed, 02 Oct 2024 01:55:27 GMT  
		Size: 153.6 MB (153635944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a23422a64432cd7bc640957a0ef9bd2dbd4c6c34ef94f32277c1438f12fc9cf0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226626818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab10d23c033224e1244ef269b5526124d5a44516b29e8802b4bacd8c38417de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:30:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e411b5e611b843166f906b0c9e1fe81a442e2896e3ed2d11bcc79eaa131eb0c2`  
		Last Modified: Wed, 02 Oct 2024 01:38:47 GMT  
		Size: 10.7 MB (10705562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bfeb71e62b9e0d28b328d69d7eb15fec4de57186b9bb2f38b4d793525ed453`  
		Last Modified: Wed, 02 Oct 2024 01:39:00 GMT  
		Size: 60.4 MB (60354960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed2f074058303c8c52d6bceb8de4cbfcf06f1f1eb813fd43fd4bf7b2ce959b7`  
		Last Modified: Wed, 02 Oct 2024 01:39:22 GMT  
		Size: 128.6 MB (128553976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:61bb3de1b71b504f10b19eb1a1d3484057d7cf84fb01703c86d20c77b1145059
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
$ docker pull buildpack-deps@sha256:b04185df0458f8714f540b4175fbe617a7702e9c1b48638960051c7dec5cd92b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39732883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940d7e2e113e4fcec4495578013dd4b911ce74893c731d4a6ccc0eaebdf54f60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dab2c53045177f347ab34f1bbe87a35ed7b6e068702ed7e9d067ab8c31247b01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34221902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedd5fba35b00db65f8f08ec4cb4795a6a4a885b660b03123833453aff7a0aee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7c49b92e6e731da55707dfcbfa37bc2d1cc589c202a9d48a264372103ee88527
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38197163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f318f15f592da550e713fddda1a5d88bdaab5e08a0f863fd7e2702ab6cc3e84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:85a17b2741f19d79fe55d8ef050629d032ba7c9126946a643d33ebc0c743a8ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46278733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fa1feeb69f1b34be579bab607d1be14a5b938fa5d67e0ad09223b8d8355b37`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:affd261433e068060b2909589ae53ade8f9d03bc0c513517e78c02a613e9cdf1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33886911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6cc75e4d9830a411550b57eafb957f4df14ef2b1534e3c21ad5964d3bcf8f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:44:06 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:44:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:44:35 GMT
ADD file:2b79df939efa8d17a9cd9432bbfe34fed1d540f46c23529b1cdab31b56362460 in / 
# Wed, 18 Sep 2024 04:44:37 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:48:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:304b7e8d05828d18c71c5dac4c2a30c8d5f9ceb02888ac26bb8065157d250996`  
		Last Modified: Wed, 02 Oct 2024 02:11:36 GMT  
		Size: 24.2 MB (24248318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf8fb897037c00782cd45fd16483b13d79bb259031660d58a354790e08968e`  
		Last Modified: Wed, 02 Oct 2024 02:11:27 GMT  
		Size: 9.6 MB (9638593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d83b15406fb31af647047d561e4c9771d45905ff710eb144ab9affca08462db4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37717882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc7bc96c10ec9f4c7e373c4a67fdd52bac65f8579d7e1987c80b00d4d57baf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e411b5e611b843166f906b0c9e1fe81a442e2896e3ed2d11bcc79eaa131eb0c2`  
		Last Modified: Wed, 02 Oct 2024 01:38:47 GMT  
		Size: 10.7 MB (10705562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:7158ef1f084f90c6d88fcffbcb5cf8d628efdf290b5f33de5877adbb0bafdb5a
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
$ docker pull buildpack-deps@sha256:24fb1d94cdeb62452080ea88d57009d977d0ebc6145bef70b355217f0c0f3fe7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100657473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec521d79a736d2c908b76567cb34fe6800cda4cf11dd3425c35d5e57a60824`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411f4debc2af1b53b390cebb61b5125cc06e081e824a5825224cc682c2bf773`  
		Last Modified: Wed, 02 Oct 2024 02:11:09 GMT  
		Size: 60.9 MB (60924590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c1a6e7fff25cd5cd4577d9b2916182b135715d9a80b65798bd9f6957a61933e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90105028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2c2ac3150f534f92f33ffa953a9903dc97fc9d4ba861bf839905461129eb86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60e2872eabcd665fccca4b65322b8780ad6b271f98a487b9d013700d8c5f24`  
		Last Modified: Wed, 02 Oct 2024 01:43:08 GMT  
		Size: 55.9 MB (55883126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:27376f7d6da57e2d59d855f0c64d760261b3582adb037e2587288b0fb5544370
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99260509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3d9e73afca1925b94ce7e6fd49da77bc0b0c88092d11eb22c98ed3a65c5436`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670a3422be6c3e543f9ce6d7faec576205d847616531df1aa7e2a7eb4af90ae`  
		Last Modified: Wed, 02 Oct 2024 01:17:37 GMT  
		Size: 61.1 MB (61063346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7af077cdf974af9fe86ec9e2172292e1c3e38ab8fa006852a21ff906b43d08fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115942647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16138b3caaffcda0cd765a593a804d16d4abeae15bc694284c03ac99ba2e3dea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade1a5274d6f1d0318337f54ba1338a12318fa208dc455dd515fa9ef53b0e5a`  
		Last Modified: Wed, 02 Oct 2024 01:54:55 GMT  
		Size: 69.7 MB (69663914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1b427ee95bd906312746d3203eb018c28f5186ea236e3507be409bb4fb6d96be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98072842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4e8d795d898f8f116f1078c6d431fc56ea277ebac4283067aec11efde7376b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e411b5e611b843166f906b0c9e1fe81a442e2896e3ed2d11bcc79eaa131eb0c2`  
		Last Modified: Wed, 02 Oct 2024 01:38:47 GMT  
		Size: 10.7 MB (10705562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bfeb71e62b9e0d28b328d69d7eb15fec4de57186b9bb2f38b4d793525ed453`  
		Last Modified: Wed, 02 Oct 2024 01:39:00 GMT  
		Size: 60.4 MB (60354960 bytes)  
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
$ docker pull buildpack-deps@sha256:b764e1843f0b1bd2c7b37890ecff7fde2e4029b5e0ec589a1b255c0aba14508d
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
$ docker pull buildpack-deps@sha256:844abe43b7f300a180baeac94b0c7249cdb2f9f8ff3a2dc57c9483c3f28cb2e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349266065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f0102621ef1c91910324aaf53c1ffd78d7e5603c2d04f1b764cbd4d8b129a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d76f36288a8f45e858f9fff3920870a2f9b74a14ca3b61e9a95b4b6527323a07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316614016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a232a96e83f21c88fb15629e06a0604433314593bf2627ed4ab05befb77d05e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:58:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f621479573c327a4dda6b206f9b47e39026965bfb7d15fce780cfaea574d3`  
		Last Modified: Fri, 27 Sep 2024 04:03:45 GMT  
		Size: 62.0 MB (61998895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cfed630bec1a9dd2e2066da3e9ed425e619a1f794f8d9fb007c9224e134110`  
		Last Modified: Fri, 27 Sep 2024 04:04:19 GMT  
		Size: 184.6 MB (184554977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f90161ac2d7576dc819ca336190bc7a58a30ed812ca9714aca4541cd7a68d039
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301953065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450d081e2a32fb58c4bfb86035712433090a7726b40c58fece913c5b45cc1fb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:31:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d1155f47c5da74e62e760752114224ea723a8e594aebd7127329bb894a726dc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340180343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5d6bbbc780759c6ab0b6e84df986cfc74fa4961041bf0199ed0251582056fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d9846aa188aeb883a2832cd89e18999cdd6729abc5b19b781876c770432efe1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351865345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d575f61783f4cdab2d23ccbc14b5610c09708882da9c57fbf8d6f98678356a27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:00:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8fd2b0b6bf6600df9bb4a82d28d3ada17089cf6f175d29438a9e261fad8beaaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326330870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50823257c59f5cfbaf625f86fa64f2884bff4c295bcd40d84fe24324b24f8a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:40:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d744aaf940b526bb655f61ce4b295946be2cf4f9cb1c458cfa98d78183b03f03`  
		Last Modified: Fri, 27 Sep 2024 11:04:25 GMT  
		Size: 189.8 MB (189824612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7e39a67e545d21d8f3f87de8b89a94edc277cf523dcfb745febd8b8a5f1fd5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363380577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fde10daac6379bc4bfccf0270f2e63f0d6132a5dd5cb5c3106f78e245323ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:57:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a1d5bfc66cab4ba82e33b861964feadc27c2fc3ad6fbca3760a165bd4f3b385e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318773548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05aaec9dff1556f3677977bd7af301d5958a0841ed2a6b92fc7a543482763416`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:14:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:130fdd43b7f7182c2170e5be91becaa74d745454039e538299edf24e161fe59b
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
$ docker pull buildpack-deps@sha256:855e41565da34c0d899e593b4b65b2b1b3b63b04a0e5f434237629a7be422d9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280279727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec47e3865af2efe637625905d89dd33956fd36c929ce0e5e6d90ef8651b20af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:06:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f61a75956927ffbc601ace40bf7d9a2809e8f42f4b39f62b33f55508f1d0ad`  
		Last Modified: Wed, 02 Oct 2024 02:12:01 GMT  
		Size: 45.8 MB (45806658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec7556ce197095176d9c1c0a174299aa49154b2129be4a2b1c22f9702b9cb97`  
		Last Modified: Wed, 02 Oct 2024 02:12:33 GMT  
		Size: 190.2 MB (190244412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8beebc65116eed70f3d544e3e5352f798089b6589e8d0c88fa42ade8ccddb066
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240482827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40701d330116b48ea1af39e23e23e04c26ea4436a61bd0577d6796f6573a984d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:34:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:37:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb119f1d99566ed1f8d8fedaee28a2280adac0c223ce200e7777dcffec00164d`  
		Last Modified: Wed, 02 Oct 2024 01:44:03 GMT  
		Size: 49.3 MB (49298840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866fc43f033b51c1a06c3f6d07cf03de9e6190f7db0f4095112e514178858c1`  
		Last Modified: Wed, 02 Oct 2024 01:44:32 GMT  
		Size: 150.7 MB (150677473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e8de3ad24dac6c6cac494b4814e26aef75b307d664b6b2686340d9275cc9028
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271386929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258dd1dedbe32e7e1ece435c11db9077d0b9a7afcc0b020f4a760a4d2e608478`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:08:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:11:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6108651e89a3a91252dddfdeef0ab0fb469fb24f4de592a5944ffec8fb73f0`  
		Last Modified: Wed, 02 Oct 2024 01:18:24 GMT  
		Size: 45.8 MB (45769072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c427e7a315343f68b951b898d838e339e728f26647e6f21415d0406eb721ab29`  
		Last Modified: Wed, 02 Oct 2024 01:18:49 GMT  
		Size: 182.2 MB (182212309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3e6933bebca2224bdfb0f4848a3435f195e74753cab3f7ba314b32dab9fc60d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299165270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d25c8992edd3b648955db835b81ab65e652a274fb0f86f982ed29f0a0eb035`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:48:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e7171ec073330607865d4617beab15833dbc3b9a901748567e8cf863a6d11`  
		Last Modified: Wed, 02 Oct 2024 01:56:00 GMT  
		Size: 51.0 MB (51025292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bbb7d91dcba46580ae17389f5d59fa785af55f5c82e484aadbe29f242438b`  
		Last Modified: Wed, 02 Oct 2024 01:56:37 GMT  
		Size: 196.6 MB (196631172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:45f3312e6c2a729d57cb1f2b7610fb271b2c90321c7640ab9cbfb34346af7dd1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330651353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4858134d5a2db71f30a48e380017fb3484e7e002a7377773dca02c81f37d0bae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:59:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be136966d9b6f5be3f056d30013c4a4cb14f67709ef491a0319722e2e90095`  
		Last Modified: Wed, 02 Oct 2024 02:13:09 GMT  
		Size: 54.3 MB (54279540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df3932963d582081c4a83ba0f2ceac2157bf5102dbf61dc9d03b1bdd38f81a5`  
		Last Modified: Wed, 02 Oct 2024 02:17:20 GMT  
		Size: 230.1 MB (230105741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cc54f4891e70f65caced3604292265dad8d5946d65e7ffada45cbb26684ac156
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262342634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea52845d53e314e832d3d992b6a7e783c248355f8779bc05d15405210f16ab5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:32:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:34:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6058811ca71a5dbcf8603e3abea065f2302f30fff37e9cba98068af6b0b0fead`  
		Last Modified: Wed, 02 Oct 2024 01:39:42 GMT  
		Size: 47.4 MB (47408365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb7d36f8e577c791f1b0efcb5d6c1678e4a4d5c1b90122e5762820eb8b97405`  
		Last Modified: Wed, 02 Oct 2024 01:40:09 GMT  
		Size: 169.3 MB (169292965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:00ce9a522e9b96a06cf9c62ed5f886a086452de5fbe729817b22742d97ba27aa
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
$ docker pull buildpack-deps@sha256:2b5869019aea04face8fc1f58ac6e34aad6762c57822fd818b69b060bd4fc7ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44228657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be742ffca4dd43a363aac7275ebf6e97ac5547ed6bda6766fc42e2070e2b249b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eec735e64d7c2150361d844efc23d07624aa56d1a543ca65bf2fc0f9f675b905
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40506514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37404394553903d1b91235398803dd2638432faec207dfee4ba58a7fb09f956`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e020fee9857b1e24261121e651e2df6156cf76e644e80fb574a4ffc798975a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43405548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b9fe779bce78d95b027b243263b191a3715452165d409c2e1b55fbd47f6528`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eae46c940ffbdc3ac168d6be819cfc19265a43cbbc5748d4bd943f6cfac7ad19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51508806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640e48b20c33f7e1ca056bef068e19aa228353229d915df3c63db96930181b67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:96cca7615cf23168ee927a322ae7d73794d18881edcfaed32a1ecfc82b2bab1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46266072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb9816d3133f9b56df724c02667b50d24d340ed5af45ab422f3ac06a48bf4ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bb95a5db87c595c9980d507e5524a0725155d84f11fdc1a9d79ca26ff3c691a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45641304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe721fbe62ad193a72dce2096351fc2462cd3129a3257456d227bb4914b5df3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:43615a08e39277ab1351782e2eafc39ccd8f669aed6312ca55a1d6bca578bcda
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
$ docker pull buildpack-deps@sha256:c3466200f8283bade92b93dce4e91901b8ef6cfdc05358c7ff1b06693c13cdd3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90035315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cbeea6df9f212bbfbf2470c165d7e871b275988cedd5735ae00d4dc44a3cb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f61a75956927ffbc601ace40bf7d9a2809e8f42f4b39f62b33f55508f1d0ad`  
		Last Modified: Wed, 02 Oct 2024 02:12:01 GMT  
		Size: 45.8 MB (45806658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b6b8a896f838c1a87984cdd62955b1c525341af96890e86eba3c15087180f40
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89805354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91815d9b10848c23757aee3d650bc0cf88b678aec7aee46e0e467cbfa015cc1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:34:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb119f1d99566ed1f8d8fedaee28a2280adac0c223ce200e7777dcffec00164d`  
		Last Modified: Wed, 02 Oct 2024 01:44:03 GMT  
		Size: 49.3 MB (49298840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2752d5704eb5d48def6e45444720a7a6ecb74d065da6da9799f289d6248b01c4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89174620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b1d3be232034ff96943a9f18661af6bfd31326f0e935f3e664635ab3a2efb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:08:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6108651e89a3a91252dddfdeef0ab0fb469fb24f4de592a5944ffec8fb73f0`  
		Last Modified: Wed, 02 Oct 2024 01:18:24 GMT  
		Size: 45.8 MB (45769072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d4f2886afb48df4227a9956b4776266c0f8653040343fcab7d5f23716773d70e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102534098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301a9a27368e19914e3fc6387aef8995784aa499e48a3a361babba0a5d8e900c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e7171ec073330607865d4617beab15833dbc3b9a901748567e8cf863a6d11`  
		Last Modified: Wed, 02 Oct 2024 01:56:00 GMT  
		Size: 51.0 MB (51025292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:88f18425ee4d26a46b4c70662b1293ace4c09b92cc7c8f3ab90dd3e30352fc69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100545612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b14e8dfaa42499d53c1b9b3599066b7660fa86a25ec8cc641cd117ea3cf26a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be136966d9b6f5be3f056d30013c4a4cb14f67709ef491a0319722e2e90095`  
		Last Modified: Wed, 02 Oct 2024 02:13:09 GMT  
		Size: 54.3 MB (54279540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8ae431968b6acabe2bcd26a8779708c25071231c17e481cc27050296369575da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93049669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d350c9144d363bf55139acbd3c4c1c48dac3b6d07a535382311a763eaa4270`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:32:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6058811ca71a5dbcf8603e3abea065f2302f30fff37e9cba98068af6b0b0fead`  
		Last Modified: Wed, 02 Oct 2024 01:39:42 GMT  
		Size: 47.4 MB (47408365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:d84922a7e26145fa71ee524463d90cac8ce7acfd1eca06d55f24e298b3912a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8d488f71540922ed4e5ac79cc16948db7a8e27e55c36a59805e82701f9697f9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322638361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbc4f4afa7a42e85251fcc85d67762b540686b81e5e08338190a107e9b287db`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55229002f3e9c7812c0683243cb3c109a172685bc13b60c4a179ee19cb7532dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3a2ebcacccc6059614008b1907339ca81a687bf111616dc228adc76140a3ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:33:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1a2070b645c8a3f79ee80782704ed85243e8bf44babcae36a54f1853b0dcd51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314282508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b4370cefb3f07fe64cbde2b559cb8b3826c9de7e492b1498a01ce2ef4d1fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6100b530306a52fd78be9546745584313d9e86581e5aed21350078bb708c17a0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328344341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1c2768b4a90b2ddc66844478825f74ac75420e5b0339c6f1b07ca4fd77ef8a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:02:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93938e3248ca49e16485c4e39a8c601801fe32600e913ea08b6a71a42acd7759`  
		Last Modified: Fri, 27 Sep 2024 08:09:12 GMT  
		Size: 200.0 MB (199967470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:39e63076945fb9ae56fddca98857b36940023ba60be84b680722266bee8c6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:493c3a47ac40dfb1b98b81aa90975efaf13260da7541c93f07942965bdc90e80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa31de3a8326a44ac072e5b372515ac96493ac4f6d6f00204179bacdcf7b0400`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0f8ea823454d8e07af80adfe6fc4d2ece17f96c194bbd11f22b5d22e0073a656
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffd1af5abfc86f8ab9ad2686f3ebc030fe4608cdf6e6facd16ddfa2d99ea583`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:842922b68678f1fac48d835049726c5398604b702ee421f40636d9e459d56491
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69483562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e86dfc5995a61ab1d4efcd1df3d5327b56e7039fb319cc94e5e6684cba5247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3d8cb4112d4b04633bb393b5a807b261208d72c1a3b573b4a4bcdd6eccb2cd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5514e433d3d2c001a6ebd4510c3dc44fb6f0134f3609a97d5eb8d818ca95237`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:2150df029cc4842b260b4c20ad9d8efcf1c283618513a2cc9d0bb31293b3cf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:790a36dfc8741a87edf1b09c31ad50381dd38fba5cea5fc6a9b46cee906b2631
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125569359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3ba45f5d00b86b9115a49cb01f515d1d386648325df11100c565089533619e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9d6d31034a1a0cb48093f49f4b1a5783c35284c62f7527b98d0f539d406a4bc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115738618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98180b24df2dae8337b3c1769d35a6fd95901f5511bb29183c2d224404e04899`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df229d9fe9c016f00c1893313e285b7f7d9262d9b81cc8093b37019c1e77e9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124318256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62aed602c832fdcb32fae77caf1c392f521669b679f4e4fc4358f2b528c9cad3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:38f00700b5ccbfcaad7854588ea97bfac8e5cad9f0f95da5b5768e7a4ce43006
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128376871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a3cce83e8b5ea3db5e0f2381970ba23dd139640398efd21fc05885497d2ced`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:0b2a42bf0df7f6ae23c9bee2cbc5dbd11e492eec2f0a65488f49f2ca60278764
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
$ docker pull buildpack-deps@sha256:1f39714b7552ebbe1d80a542a4e764ec7fff0eeb5ff155e5305c836b8e1bde6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293595121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd75f501048aea4153cf8a32016424ad5641c82b7450e1e602fabfc68f972d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:07:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:10:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba6e5f3d90cff89eeec5ed07e205cd2b78e8e111454ee7cfcdf300bfd6122d`  
		Last Modified: Wed, 02 Oct 2024 02:12:59 GMT  
		Size: 46.5 MB (46504774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b191893e4ede174d5397194694c3780fcc1122cf4a6798dc746a28b5b8090ee`  
		Last Modified: Wed, 02 Oct 2024 02:13:35 GMT  
		Size: 194.0 MB (194039068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2085016390fa315d8ae35cb1d0896be3d5d902f2c7b553376d3e9a259df11c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257295116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b4c9ee67c97324ae0cba8cbe153b91c3452c4a67125059a3e3636c350f9aa9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:42:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf4c374ea7ab02bd9e1c077c3f4295612de66efa2c54b41fef14db04e0aead`  
		Last Modified: Wed, 02 Oct 2024 01:44:59 GMT  
		Size: 49.5 MB (49478102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a543e4a77995b18667e3ce720c44d3f0e07160a7e910559184a9dd7fe0bb9484`  
		Last Modified: Wed, 02 Oct 2024 01:45:28 GMT  
		Size: 157.6 MB (157603332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9080b3fa5c7e031077d09cd1aa67f9d05d99a53aed134674352053088aa37937
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287690780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a835fd6185ddf21f8309db2fbf6d7b6eececcda785fc939aa3f1dbf5a9fb2ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:16:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeccf52d0c7d95f1cd621b4538c19cfff5867e52d01d5a00f759a459ea28999`  
		Last Modified: Wed, 02 Oct 2024 01:19:14 GMT  
		Size: 46.4 MB (46434300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925c4202924345a21194a077f853b64ce8ee8e676a6e91001d61fbc28dad6ba0`  
		Last Modified: Wed, 02 Oct 2024 01:19:40 GMT  
		Size: 188.3 MB (188255082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d2786b9534cd8ff21466912c2ae42c51e750cf7793219433622506e44175cdb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309380326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bc9f5ab72cde0cb37715560656f77831a32ee257219f9c207b0ee8a3062492`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09f090381214fba1abf5d6db78c3189b6ac1fc85765a40e6be5d83b7160a433`  
		Last Modified: Wed, 02 Oct 2024 01:57:09 GMT  
		Size: 51.8 MB (51772787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce954ce4c7e576b190694854b8f4ad4e44769c2ab96b6082ebb32f9a11300207`  
		Last Modified: Wed, 02 Oct 2024 01:57:47 GMT  
		Size: 197.7 MB (197707907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5dbad1736e445c9255daedd2291c1ed47071678ec62d7597c9bfc2e6151dc4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387512083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d6847932498e61a798352ad0688d37e20d3985f1cf61de61ff856afb6b0c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:10:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b19496a8d9dc226b4d60c0384e37525cab9161d87adbd6637828dfdeb65fda`  
		Last Modified: Wed, 02 Oct 2024 02:18:51 GMT  
		Size: 54.6 MB (54636883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1257422a528ad068c80493bd9a6a64aeba863bbaf8a67d7570a247d274ff1c15`  
		Last Modified: Wed, 02 Oct 2024 02:24:08 GMT  
		Size: 276.1 MB (276124113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1b94bfaa2e56c7aeaff52679ff4779a169746a2e6cbb4def3d569a168e7f1f4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271908522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543c8cdf61067f50de3da9ea6a9ca70cb685f31fc28f2c8d4858b1aebc73e8ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:38:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f66afb7703de047378bbcd7202a18143aa8936962a5cb32c6625771ab85206`  
		Last Modified: Wed, 02 Oct 2024 01:40:31 GMT  
		Size: 47.9 MB (47891767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f9b9a4e4d09843427eb68bed83f636b885ed208222043fe011670735db076`  
		Last Modified: Wed, 02 Oct 2024 01:40:58 GMT  
		Size: 170.2 MB (170171054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:6499d16a7cda6edff74057981ea079f60738ad77655cd907049aeba1a3ae3ce8
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
$ docker pull buildpack-deps@sha256:43b36a5d4a544769e661359e4e9dede556771f8ac92c429a57dc62fa2cf69767
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53051279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cc0a3c2e25179d44f2a2b5542d854c52a61f5542608fc9a3b5f3c777ba83cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e5ef1ba7f72f74676ba3892c089ebd477003f69f394da04c2d5211aee345014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50213682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4120e010b3cf1347291742619438cd108a3202db2f105c8494bddcaa27fd5c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:14343f47d7690d366becb1a31403f2da6635e353263c0e0a268d6878b9d58eb9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53001398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e9a04501ce3c5ca1857dfcdab71868740920e9a238bf309f66560966c87ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0add5043015ef28f13bf6510cdd61812afcfe42c8f6c521ab9e9aad429887bc6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59899632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08108f3916d5257faed3846a0279abd43a4276137b0f83fcd33fafed745fcb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7ee40875c9bae0d9749f1240b3254b301a55e66e8f459064f75b40639506389c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56751087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2f966ccb05e961221b21a9db2d61c2a852abbe4fde1b1f73c04f1efe11b97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e0f1452312d316a117afce07d8b75245eb486a85fb8f35d4984727862a191429
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53845701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05be1340e4a56fff7138df8e2c81507408fe5ba9e4691ff6391d881041b7672`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:62089f7b5997f0efefe64e81ae10ac6b840033070da4112ba5a2bedf25238e2c
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
$ docker pull buildpack-deps@sha256:bd46e031aaa9c9f1dda73d5e59905fa47de82a688d385741a17fb1bddf9df407
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99556053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a96bdc66278035d3d259d9f0a207a9bb529132142715c1cf7f189e5332c574`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:07:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba6e5f3d90cff89eeec5ed07e205cd2b78e8e111454ee7cfcdf300bfd6122d`  
		Last Modified: Wed, 02 Oct 2024 02:12:59 GMT  
		Size: 46.5 MB (46504774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6d3a96e2c941240fc90a61957f6267394476b470a1cdb48c877d7f95a9dc9317
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99691784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442ea755cbf1609c90ef5c5ee53c31cdf810ba83d8bba6299b7bde26969b131d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf4c374ea7ab02bd9e1c077c3f4295612de66efa2c54b41fef14db04e0aead`  
		Last Modified: Wed, 02 Oct 2024 01:44:59 GMT  
		Size: 49.5 MB (49478102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb51fb2c38fa781af7438d1b645ce1dbfa44de5e86b8bd6104587e791d9984f3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99435698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090ce4830fc911c60fd6e58b546d0111feb03513dd571a5616c8630899a56cf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeccf52d0c7d95f1cd621b4538c19cfff5867e52d01d5a00f759a459ea28999`  
		Last Modified: Wed, 02 Oct 2024 01:19:14 GMT  
		Size: 46.4 MB (46434300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d7118aff43ad9d0f937e5d9dd9bdac8082f0fb7d8e7e84347b52699a42558bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111672419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576fa791aeee9f8936c231826235059e4e789e1c71a4429251055a9ebeea4e18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09f090381214fba1abf5d6db78c3189b6ac1fc85765a40e6be5d83b7160a433`  
		Last Modified: Wed, 02 Oct 2024 01:57:09 GMT  
		Size: 51.8 MB (51772787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3f5f0ead2ff3ee3b884d099a66b85cc8c837f0e4b36cb485e3af599fbca9e631
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111387970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64f56c2dd7d2477c02dbfa01deba2aa40ee679b53de609c730d2b0333d1bea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b19496a8d9dc226b4d60c0384e37525cab9161d87adbd6637828dfdeb65fda`  
		Last Modified: Wed, 02 Oct 2024 02:18:51 GMT  
		Size: 54.6 MB (54636883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e30a832eb8441f147f02a188f52ccfd9fd34cbd8cec1953bf685552cc4b5b3c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101737468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1955d1d0bc03b7553c28e79aa0e49d120e72888356f86b52e496ec4c280c05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f66afb7703de047378bbcd7202a18143aa8936962a5cb32c6625771ab85206`  
		Last Modified: Wed, 02 Oct 2024 01:40:31 GMT  
		Size: 47.9 MB (47891767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:e11f406032a4d2feb352cb67eafe24bef8fe34e694f598d0e89d27765a03bffd
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
$ docker pull buildpack-deps@sha256:cdeb27a4b786ecd529d4ba561a21636f9f2c12978106fdfd0c251e7688d4d4b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138000423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256f5d3f483568706fb9df2caac236da768819cf28455c6c0c0d557f6150d188`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b4bed19797b1a45bf83aed141a7c5c840df6e86c5b5df1fd5849547c160a11a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132059039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceee25cfa608bf7d28af66a01dd3514e68c871aeabb8dac1819da58adf72883c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f621479573c327a4dda6b206f9b47e39026965bfb7d15fce780cfaea574d3`  
		Last Modified: Fri, 27 Sep 2024 04:03:45 GMT  
		Size: 62.0 MB (61998895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69ffd73b6d892f801b4efa09c063974514dafeecfd976c74208a8adb37836678
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126745127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a860569244686aa20ef28222e3cf0f8a3f9a06115043280f1fadcdaf701f6d4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c511f0a2c78bfee9e532c0854584204b5613b96f7fa951fbc416612231899820
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efb79080b7192496c79c55cd230e6554a55fdf5b710985ebf7d23a7a7157ae4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9e62a82d839392f6e96187cbf80a16d2bc6b9f6ee69bb46eaf1f98e18441045a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141683005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68d5203ba4f8ccbd3a59b3be1d5e60b1507280d22bb4093074144b32149c527`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3ccc6ca2f3cd3da62fbba482ae0f7ab4b7e7762149fca5e0bac80c87f62a09e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136506258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4137a21de1b19963fef5cffdc14a7a26f7544ddc4bb934022ca9e06ee08cb8f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b13a20b76943a028b928f105a448b56054d5ecdf8e4df28aec30cb6350a673d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149094859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e8de729db2ff936bca848d32d17073a4be7b7485e28f2950fcb77c6d47b57d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0fca24d12422d5546ec9cf5d31171ea318913c4239a822ce12e7670da6286434
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9af3b078649bdc6f7a9a4152248dd30c88deea81edd802d617a2ad046ac482`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:f54c77ee8ad6e7825ffc8b0aee14317bc174132e793317459fe39d7c27e7c550
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
$ docker pull buildpack-deps@sha256:ee76f9c492d0f4072868e40d1250a1ce243aac136384fefc31fe01e9aeea11e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367357446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b457d4ee4cfc4ebb25157e51045e62481112e0746dfe3d9f2508e00b1f64c0e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d824605d3973d8333c12588307d4b7865a9d16a172cf713a69bed064281a179`  
		Last Modified: Fri, 27 Sep 2024 05:16:40 GMT  
		Size: 66.3 MB (66298648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e9cccb32adeb73089e38bb77d73d59c2177bbb495bbbc4bac305a228188d9`  
		Last Modified: Fri, 27 Sep 2024 05:17:14 GMT  
		Size: 227.4 MB (227404144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c37c2fe099ca8c852db765ea796c72a5565fce2c9957748d192a6d2330d45ce7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335802621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959ed346fcd14aab877dc44925c39b738c268a59db692c7ca7224cecb1a1c14a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:00:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03463b6c07bccc1364fec128e533c62c4e2533ee53250fc1153a70167b6f44b`  
		Last Modified: Fri, 27 Sep 2024 04:04:50 GMT  
		Size: 63.8 MB (63754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03773ce488248829376500af9b84cf97fcd39ed3242f9e2187079b56c71ea969`  
		Last Modified: Fri, 27 Sep 2024 04:05:25 GMT  
		Size: 202.5 MB (202482927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7dce74814ac71c3c1a030db777e581f1ccd7233b7ba27541b483b18f3662dbe4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317241853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e048cf3ab5d5edb6ad2b4ddbaaeaf5b699f98ca7db295e0a9416b4eacc47e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:35:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cad0c26ab0027c184690fde3603662a1fe5a37591c336a98696770ac66936e`  
		Last Modified: Fri, 27 Sep 2024 07:41:21 GMT  
		Size: 61.2 MB (61234643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e907df1326f4d0916b686b69508feaf27c5bfc2aa38710924f377f75b7fdbe09`  
		Last Modified: Fri, 27 Sep 2024 07:42:01 GMT  
		Size: 189.6 MB (189579676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2dcc03ae0e069e97bd427e3523013055888d7649c17b947c1770b684987e7b37
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361024922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34275d796bc4304378c9c4f5a93c485125d7f567b96e662711a64b21fef728bd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:22:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd393ac9d5f3e6f4ef01c240e4ee33361f9163326dc4fe0c98ca544756cddc12`  
		Last Modified: Fri, 27 Sep 2024 05:26:51 GMT  
		Size: 66.3 MB (66302891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac170a650f31dab130f92fb8708276d55343d8d7ee851c19b5b9f257acdd6f4`  
		Last Modified: Fri, 27 Sep 2024 05:27:19 GMT  
		Size: 221.0 MB (220988693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ded01fb58e652afea4c8e7094453b5af95454a57d274207a2bb3eb8d67ba93a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371902498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb6475fc00c3a209abc95fa65afc37a1ed13142d0bb884b32069569704b4147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:02:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:04:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71b0341053ee8776ca7ecfc201a051da349ec1f8e5c73b5d4a043fd3154532`  
		Last Modified: Fri, 27 Sep 2024 08:09:48 GMT  
		Size: 68.1 MB (68105180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f792864bd7cba3961b251eec2e1ee9f352895552addc1e17511d0c39b02e56ab`  
		Last Modified: Fri, 27 Sep 2024 08:10:36 GMT  
		Size: 228.2 MB (228233735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2cfdb4463136f7a7fd6a964fc3abeffe5f208f66260fd0eaf0c70642e5386419
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344950889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66d337adcb0f1ef97b6662438438bd5c5fdf7cf39e624d1a8af498fbb4b2d2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:51:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d0102a70641af727b17e4dda29d3e752776fe5f927c48dc6ba42534da6baf`  
		Last Modified: Fri, 27 Sep 2024 11:05:38 GMT  
		Size: 65.1 MB (65067190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3393aec747705ef0a675939b6f883a7ca72a36da98e766e42ca2a7286e7af3dc`  
		Last Modified: Fri, 27 Sep 2024 11:07:51 GMT  
		Size: 207.0 MB (207030957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:33011240df37cdf38b23d38f03d17a12051d05e4b3d94c36635ddd57eafd1713
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377881836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51344e88f1f121524c87aeabda4282378ca7a7659586aa483fb44b98340e72a2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:00:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83256233144f0df0689578c0a89c181e74e6ea6cc435661a805b2a60809bd43d`  
		Last Modified: Fri, 27 Sep 2024 06:05:59 GMT  
		Size: 71.6 MB (71626121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751e854e69a77c78cd9663a65ff9e955dcc052e392333a04a5bf6bd4c25ebb97`  
		Last Modified: Fri, 27 Sep 2024 06:06:39 GMT  
		Size: 226.1 MB (226106927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1e96e7d98bcaad26df0722874971218e5cf4a3a99c344592ce451798f947f237
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.2 MB (448211534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82239ca4ec79855f9c4e0b72e27e8d0bfa5763224bc3e1e71f6749abb66715f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:57:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9f4a99275f793e5c8e68b8d73f18d109d2b326d17fb8683a66ed765527984`  
		Last Modified: Fri, 27 Sep 2024 14:01:33 GMT  
		Size: 65.5 MB (65531769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7485ff1326cbcb09db2dd7bbb6906908774b101e4ad4c8f61975c7a8036b5490`  
		Last Modified: Fri, 27 Sep 2024 14:07:02 GMT  
		Size: 311.3 MB (311251420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:02d80f6064f4d0e45507e4fb2c58bcaea875e315d0609b0be609a084766835cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342486230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3180d78e39311bbb86438bcfae83a1c25a9665ba35a16eda55358e509b4479f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:16:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cedf4fdb3f455010b1f7eeb3d9f24a25a7fd469356a31a9f5f4de26d8238f1b`  
		Last Modified: Fri, 27 Sep 2024 03:21:27 GMT  
		Size: 67.3 MB (67330712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a95e4129bf276881f4c92fb92d3cf0bad3b55875c49bb65e8462f3ef6fecfb5`  
		Last Modified: Fri, 27 Sep 2024 03:21:55 GMT  
		Size: 200.9 MB (200921345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:586835792a6c444c692e1f1ba19d9e916fa326a26a1e5c46d92911025ce4a744
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
$ docker pull buildpack-deps@sha256:d4e775cb76782502bd02eece1eda4b0a8d55a4d3ee1dc17c14b09feafd209899
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73654654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bdfa4dad25173a03ab31b77b3e6e228879dd9ed3040b7767dff741d2e6ce27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:326c47ff85ea598c88a6373d582ef1c6de0eb3fc0b7f6a9fa9f59250ea5f813f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69564930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c238989bfbc727c388dd851fa69e387bedaa311f086ed31c2213d306af10bb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:087a4e515cf7a1f37454402410d12026217e390490710553bdd7b56bbe281d84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66427534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c64bff340794dad4d2c5fe7fde8be11e10f84ef198a2af322e27fbb2e8c5e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8400ef23e2bfc1cf7961db7e7fc5cc365c21fc94bd265e5586c1ac7001d823c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73733338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaa242a8c35f491600ed256f8fa81f930e3e3971e3b401d781772eabee39a12`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7802476f80697b0d8d2e5d71ab473170f26b519bb144992d6add93dd482b2718
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75563583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6442f8185858decdddf033823e4bf8efbf0c130cc1fa8d22fd5c1d3018536d6e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae678d42d522c5a885a907970dd730a90c8669064fda9c6bef043fa42739b6ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72852742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a62a61aa389cf6527efd964175baf68a829cb84e2d4cc5d3690fc671cec76e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7dfe7f2474c97c8c5c6c60643147edd25a2275ef8d96ac019c47a72b54bd5c51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80148788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125d9685f5ce2e879b85d739962910d5e860f1cbd233aec7a11ac062aa49456`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:be7a4796ea31bfba3509caac3d8e05901ce05dd65a120cc12a3dac0cc3c2be9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0809c76f2424482deec4c8cfcbd1845c22bd604642587f9913b0c256989079a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:32a8c0af96f9a31118c91a08bf2f2cf38dc4b986a325557d84203f43c7b6cdcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74234173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9eee7a70ef8c4b7ebb8b8e5353eb05a0035489844aa9fbd353097589d36973d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:6f73b50eb212126c3ddc1535f35589762e4465547b7daff38f81d11448ed92d8
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
$ docker pull buildpack-deps@sha256:ea2eee0ac8d30d5443afc420f583d8e8c912153fc14e9aa31f89dc0d9a5eb107
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139953302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4694df930c2fc62cefd789b61bf38323f8cabb232ac9eac2e10a8e2d93b50ab0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d824605d3973d8333c12588307d4b7865a9d16a172cf713a69bed064281a179`  
		Last Modified: Fri, 27 Sep 2024 05:16:40 GMT  
		Size: 66.3 MB (66298648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:01d2dd0dee2fd58f2253a6f26e754440b8c0515b6171462c890bfb5257a16def
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133319694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24d0b4c956ac03e07ee2103998239b5293708df10144188615f97ae3e5c8720`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03463b6c07bccc1364fec128e533c62c4e2533ee53250fc1153a70167b6f44b`  
		Last Modified: Fri, 27 Sep 2024 04:04:50 GMT  
		Size: 63.8 MB (63754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17cd05150504f279feed04079948b74f6e364d1682b04e9040e80caa426db01c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127662177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a55dab28cc2ae523f094e6efebc21ebe56b8b362c582c1c533e962dbed93e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cad0c26ab0027c184690fde3603662a1fe5a37591c336a98696770ac66936e`  
		Last Modified: Fri, 27 Sep 2024 07:41:21 GMT  
		Size: 61.2 MB (61234643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5f513a1c5f215d83b71b8cbd64ca21887cb12f01b07695a7ffdf01a67e2b0fd2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140036229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36031ec48fc57c491b354b9d8b65ff95c5876b9efaab45a0c871a1ece21d7b30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd393ac9d5f3e6f4ef01c240e4ee33361f9163326dc4fe0c98ca544756cddc12`  
		Last Modified: Fri, 27 Sep 2024 05:26:51 GMT  
		Size: 66.3 MB (66302891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:53e3eccac956f1d4ee4d99fcea327f66677b769148b25ae648c5a18bd6174a4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143668763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8798ca05e5b30c95dc243061792aee08c62c51f8c2a63aa060afaa288059e2ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:02:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71b0341053ee8776ca7ecfc201a051da349ec1f8e5c73b5d4a043fd3154532`  
		Last Modified: Fri, 27 Sep 2024 08:09:48 GMT  
		Size: 68.1 MB (68105180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:81b3eb351c29e1eee6d71447de5ff65324ab8ab5f47e41527137e7f86f17a573
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137919932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4aef28a5b9c90b1852dff723450b8f097427b7efea4336d6dc48df2542219a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d0102a70641af727b17e4dda29d3e752776fe5f927c48dc6ba42534da6baf`  
		Last Modified: Fri, 27 Sep 2024 11:05:38 GMT  
		Size: 65.1 MB (65067190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:41ea68f4856fcfc92d08450a4e126e0e2e50ddc67d7083e73f7989e8588b0c90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151774909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ff9635ca0f0e2eb1753e1b9d77119fe5100e04cb5dfa6565bf38e395943cc8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83256233144f0df0689578c0a89c181e74e6ea6cc435661a805b2a60809bd43d`  
		Last Modified: Fri, 27 Sep 2024 06:05:59 GMT  
		Size: 71.6 MB (71626121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0d34076051b03e658b59b9167c20d545d924469e7f2829509eceeb01e5b1f0c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136960114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122d6b276a8d897277117783348c16c5fb72421b777ea13632a0d12e90f081be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9f4a99275f793e5c8e68b8d73f18d109d2b326d17fb8683a66ed765527984`  
		Last Modified: Fri, 27 Sep 2024 14:01:33 GMT  
		Size: 65.5 MB (65531769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b141a1e4d3e090f1289387b4f386a06ff9a10536d71467dacc45743ffc85c099
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141564885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f6067781a4b36d561c120b2a47b037fb544c7e50607d9658b7102c0a97c16f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cedf4fdb3f455010b1f7eeb3d9f24a25a7fd469356a31a9f5f4de26d8238f1b`  
		Last Modified: Fri, 27 Sep 2024 03:21:27 GMT  
		Size: 67.3 MB (67330712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:b764e1843f0b1bd2c7b37890ecff7fde2e4029b5e0ec589a1b255c0aba14508d
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
$ docker pull buildpack-deps@sha256:844abe43b7f300a180baeac94b0c7249cdb2f9f8ff3a2dc57c9483c3f28cb2e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349266065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f0102621ef1c91910324aaf53c1ffd78d7e5603c2d04f1b764cbd4d8b129a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d76f36288a8f45e858f9fff3920870a2f9b74a14ca3b61e9a95b4b6527323a07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316614016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a232a96e83f21c88fb15629e06a0604433314593bf2627ed4ab05befb77d05e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:58:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f621479573c327a4dda6b206f9b47e39026965bfb7d15fce780cfaea574d3`  
		Last Modified: Fri, 27 Sep 2024 04:03:45 GMT  
		Size: 62.0 MB (61998895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cfed630bec1a9dd2e2066da3e9ed425e619a1f794f8d9fb007c9224e134110`  
		Last Modified: Fri, 27 Sep 2024 04:04:19 GMT  
		Size: 184.6 MB (184554977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f90161ac2d7576dc819ca336190bc7a58a30ed812ca9714aca4541cd7a68d039
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301953065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450d081e2a32fb58c4bfb86035712433090a7726b40c58fece913c5b45cc1fb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:31:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d1155f47c5da74e62e760752114224ea723a8e594aebd7127329bb894a726dc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340180343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5d6bbbc780759c6ab0b6e84df986cfc74fa4961041bf0199ed0251582056fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d9846aa188aeb883a2832cd89e18999cdd6729abc5b19b781876c770432efe1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351865345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d575f61783f4cdab2d23ccbc14b5610c09708882da9c57fbf8d6f98678356a27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:00:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8fd2b0b6bf6600df9bb4a82d28d3ada17089cf6f175d29438a9e261fad8beaaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326330870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50823257c59f5cfbaf625f86fa64f2884bff4c295bcd40d84fe24324b24f8a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:40:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d744aaf940b526bb655f61ce4b295946be2cf4f9cb1c458cfa98d78183b03f03`  
		Last Modified: Fri, 27 Sep 2024 11:04:25 GMT  
		Size: 189.8 MB (189824612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7e39a67e545d21d8f3f87de8b89a94edc277cf523dcfb745febd8b8a5f1fd5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363380577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fde10daac6379bc4bfccf0270f2e63f0d6132a5dd5cb5c3106f78e245323ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:57:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a1d5bfc66cab4ba82e33b861964feadc27c2fc3ad6fbca3760a165bd4f3b385e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318773548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05aaec9dff1556f3677977bd7af301d5958a0841ed2a6b92fc7a543482763416`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:14:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:d9e45b933e88fec1af990490ba945719590f1b2b8b42e0d5937fab474bfb95a8
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
$ docker pull buildpack-deps@sha256:7cd34f6aa61a3c733d424a74dd7d74f5ec07f352826096978c0caef6e00fc5a3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996740c38dff205ca2785ba2a036ac963aaaa228c7b151b7eb06b9510cfed533`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:55cb1e4c19e4ce0bf8befa213f443a1cb079258b37bd96fb93df8753f205a6d0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e100329f986eee8d9fd68f61fdb0de4b3022de29cc53aa9e11cc1ace15686c7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e0103df7597b5a1f58d3340652fd4e2ef182e6f3a4e6d50504141d699a85a95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20b8cd6905490f862d25ee649cef83b5c280b42c9b126a402618bb337a7d033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:07ef2b337dbaa3b24f512765d8647a4b18100d8c964ca1837bdc3c252771f671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0765495cc8e1d55218a919fa0964b0f2ba70d1835cd38dfbc39a578bb7eed8fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:357d8038f8b2afd5aa2ce4df26f984cfde01ceae64db1a57631d38c0ad688960
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75472063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4269028d3d3cec5a247eea96f8ebd805d13a843ef53aa83d7620a96109780c23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c27d7e6ddf0c975659df682da2dd95cbfd8d688c04bae878dc808ad8bc5473c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73208962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3bed2fbe01889b0dd4aa1472925c83f532d87d6ce064307fc1b580f104e8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2a34312a58e86dec2a572befc36ec41429bc23eddddee1f7df8a1397ea45568b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79265358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7d7ae581ca969b11912d5321c5bdb01df75c5a86ecd4ac4dff87aae8e55cd6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bc324164742dcb747c497b6e48d8e1b6525531ba158618a3ebc7811fee22e71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71990644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8261d005fafe79e46470e17827e8110c5b219222f828faf2c1bf3fb82e0a5575`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:e11f406032a4d2feb352cb67eafe24bef8fe34e694f598d0e89d27765a03bffd
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
$ docker pull buildpack-deps@sha256:cdeb27a4b786ecd529d4ba561a21636f9f2c12978106fdfd0c251e7688d4d4b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138000423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256f5d3f483568706fb9df2caac236da768819cf28455c6c0c0d557f6150d188`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b4bed19797b1a45bf83aed141a7c5c840df6e86c5b5df1fd5849547c160a11a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132059039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceee25cfa608bf7d28af66a01dd3514e68c871aeabb8dac1819da58adf72883c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414be7c785b0688eb9b0e4210d895699ad9cd75eca5449356af9cef980bd77ab`  
		Last Modified: Fri, 27 Sep 2024 04:03:19 GMT  
		Size: 22.7 MB (22729389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f621479573c327a4dda6b206f9b47e39026965bfb7d15fce780cfaea574d3`  
		Last Modified: Fri, 27 Sep 2024 04:03:45 GMT  
		Size: 62.0 MB (61998895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:69ffd73b6d892f801b4efa09c063974514dafeecfd976c74208a8adb37836678
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126745127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a860569244686aa20ef28222e3cf0f8a3f9a06115043280f1fadcdaf701f6d4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c511f0a2c78bfee9e532c0854584204b5613b96f7fa951fbc416612231899820
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efb79080b7192496c79c55cd230e6554a55fdf5b710985ebf7d23a7a7157ae4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9e62a82d839392f6e96187cbf80a16d2bc6b9f6ee69bb46eaf1f98e18441045a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141683005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68d5203ba4f8ccbd3a59b3be1d5e60b1507280d22bb4093074144b32149c527`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3ccc6ca2f3cd3da62fbba482ae0f7ab4b7e7762149fca5e0bac80c87f62a09e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136506258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4137a21de1b19963fef5cffdc14a7a26f7544ddc4bb934022ca9e06ee08cb8f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bb6c0f1b34dcdcd0b16bcd5637d2885844abedb2e641e353a1e5e633d9d40`  
		Last Modified: Fri, 27 Sep 2024 11:01:24 GMT  
		Size: 23.6 MB (23647347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e054123b78b936d75ee48cb51d153c75001aa8c7fee6cbc330793865d0faac`  
		Last Modified: Fri, 27 Sep 2024 11:02:17 GMT  
		Size: 63.3 MB (63297296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b13a20b76943a028b928f105a448b56054d5ecdf8e4df28aec30cb6350a673d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149094859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e8de729db2ff936bca848d32d17073a4be7b7485e28f2950fcb77c6d47b57d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0fca24d12422d5546ec9cf5d31171ea318913c4239a822ce12e7670da6286434
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9af3b078649bdc6f7a9a4152248dd30c88deea81edd802d617a2ad046ac482`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ae0cffdfd009583bacc47bb91fc2e7a2f7d0874d8895a3d690d4e5c9d055ebe6
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
$ docker pull buildpack-deps@sha256:8ef56987777fd5cc83b244bea06f71a52e067d4a3573dd4d9e46426da7e3b794
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366958012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc459e0d4b28f0722a6ad59e7d70cb78c0aa037d87666e9c2ee63e04085fe71e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:13:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271cd5a2233f0950e0047c5ef70615565f18b1eb82b465bd4022186677b3a0e3`  
		Last Modified: Fri, 27 Sep 2024 05:17:40 GMT  
		Size: 66.2 MB (66232209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caec85693b42c7320c4c42dad676e7729de43a3e75de092afc9069f0060a3e5`  
		Last Modified: Fri, 27 Sep 2024 05:18:14 GMT  
		Size: 227.3 MB (227253201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a702af9257ea6649053fdb5c5801607a829b7d01672205b726401c8128e958bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335462987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322342ca71be45e54db169d641b33b9049fb9f8e9e2db499781674dd529d1c99`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33a076b656ffa1590cb3af11ac35caa4cafc5418c987ee43ff730ce6667124`  
		Last Modified: Fri, 27 Sep 2024 04:05:55 GMT  
		Size: 63.7 MB (63678959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b391cda3e9681d641f974d78e09b872a28e4dbbc868b58887bc63c79773685ef`  
		Last Modified: Fri, 27 Sep 2024 04:06:30 GMT  
		Size: 202.4 MB (202371033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cf5f7f2b3d1e7e053937847cd1d54aae5660d0b109ec06b1e37407c516026f08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316886587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908e66f98eb6616f1e3e4995f88f43cac97b623cdf136f562ae4b5605d03b26d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:37:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985eaffb50a16b04f512a5978f60707cec0ee2ee400d8df8eed0a4f2ae4e7bb`  
		Last Modified: Fri, 27 Sep 2024 07:43:04 GMT  
		Size: 189.5 MB (189463031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6eb1f5a4d0fbaa0738de62ec4ce5cad85bc0deab8318212832033be1d4e44227
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.8 MB (360841180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5170670a1b59e433d47ac1c2f5b6cbd4cb569be345029c90a37adc178439fa3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46608e24e871aeb173029569f11931335886e512f79bc654f51a4aa982f67d8`  
		Last Modified: Fri, 27 Sep 2024 05:28:17 GMT  
		Size: 220.9 MB (220936291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2decb729ef9d6a3e32c10577537efc0add6e5f9df995fee2a00a1b3319c51a6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371489677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd72c109ae60fdf2258bd4f815f9c581638526f9fc3d6087eb2a165550b20fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:06:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146c248c1b9df1279d1bc34451bbfaa5ca72d7e3bf28372ac12a9ce2a2af65ad`  
		Last Modified: Fri, 27 Sep 2024 08:11:09 GMT  
		Size: 68.0 MB (68023503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358825efffd1f6da3c20226a36432d1a31ff644b5ead94b4a2cca864377e042f`  
		Last Modified: Fri, 27 Sep 2024 08:11:57 GMT  
		Size: 228.1 MB (228096516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e8b34340c491b168793c8194cf3ba79c7c8f75ea8811169bd87769e85581458f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345169031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b036904e38b7604d964773dc03770759f4897eb01f8881dc506b7ed1a27a90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 11:00:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816183487bc68f313f38e3315ac6bc39afe27875baa50865d4d9f7b974ebbe24`  
		Last Modified: Fri, 27 Sep 2024 11:09:04 GMT  
		Size: 65.0 MB (64999739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a51967b8f4cf1b2d850d26a139c5f1d7e8e41b709c161d9eee6061bc4dc74f3`  
		Last Modified: Fri, 27 Sep 2024 11:11:17 GMT  
		Size: 207.5 MB (207461682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7436b5b7db65cd5a624600a1deeef5c873d96bdad3f435f9fef4b991fa46a014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377576280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3c82a2612f21cfb3e020d6a1179a1339b2674541a1bdbe7f3aae822f6e52ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:01:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:03:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c552054a471b4255e6efa87c7bc0c63ba0466655c5644bfdade3677310ec65c`  
		Last Modified: Fri, 27 Sep 2024 06:07:11 GMT  
		Size: 71.6 MB (71553163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f28b4807d4b640478c00c941befcc03e7516d529f7038a9e613825c62ecd05`  
		Last Modified: Fri, 27 Sep 2024 06:07:52 GMT  
		Size: 226.0 MB (225981559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d5b8b5e2291d7c8cc065f3f18775309ccd2ba7d9bd1efaa8de0eb044d6793b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342226166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ef9bf1106f34529cc7819079b623b933e37a3488161ce834b76eec5ab53c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f620222e1943a71639f47a8405e2a62c61af833945aaefd53d6e4523b5853a8`  
		Last Modified: Fri, 27 Sep 2024 03:22:45 GMT  
		Size: 200.8 MB (200803778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:a2865529aa6ef65d66c43f5e91d94a93e7aec1217db37aa0a6a0f4ec0a896de1
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
$ docker pull buildpack-deps@sha256:4c612a64fbbedd375ae2f6a13caabb608d2b14d46ea4474fbba5acb84f08f2dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73472602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dc983b92201256daec01ef64b348f51b2d5cc274b81ffe01a795142a064737`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:511848f89ac6a9a59f3a996fa2313c2388ad6d9586959bfe53c4efb8360c0b0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69412995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebd13eb50f8d1965d055ddc0a5075c31cd7dd24537c24838d2f298c9407d8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98d0d2d989c716ceacab3193640a9356b37fa827f72314d00a0270c8006197f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66262823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7602a452f4245dfc17d03f43f1bc3130eebba36523027d5e4c9116d704a13c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9aef11957c014ee01c467128ef31a08b32c6953f31ab48378266d1d08cfb0599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830955de46667fa98d512e386318f49ac6b2fe117dbdd5900d9bcc4c8945eefd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d689396f888b6815f6a9d0f7298fd242f2f77cafac80321b1642a05eb661a39a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75369658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0043e8cc00bd545c060f11bb04b7fc66ce057873e9d3f026858abe4b01a466`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b0efa492445a57ae8f018beda4851659a8e6053a22551603bc71c032105227f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a371a0285e3282b682d0fbe1dd7641d3091c0f79793691f7a9a26b96272421dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67b5d9ed541257d6e7b0df6d704b584840267e267ce4aca7916a91445998a679
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80041558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9902d8e9389a2a68eb6148b4670a752f6b44e04ea16d3fda06e7857e2a42494`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4e5a879b654c7c746335d5c86a83cb9cf26be40ec7ff2bc53b6e28d0ad3f6463
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71302497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7431eff14b4cf260214e2c7494998e25d9583b82cbc1558c76e490b08c437b30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:27:18 GMT
ADD file:da1da406a30d8c871e2184104ce67d821e790fe334361223691352f3f2de2066 in / 
# Fri, 27 Sep 2024 12:27:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:58:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0a4dce9b327b8993d0aa8d580f47160e8320c3015f48472eedbf0d06fbb649df`  
		Last Modified: Fri, 27 Sep 2024 12:33:20 GMT  
		Size: 51.5 MB (51492798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dbfe1ea856752f068e2a64375dcf7a47fa54aacb79b8eb7df476c2bc442322`  
		Last Modified: Fri, 27 Sep 2024 14:07:27 GMT  
		Size: 19.8 MB (19809699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7a815adf7f34038e8af8937945bc9715fd6dd87d23264894e5b58ec62369aef2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74165458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab392593f47f6c95908f64b1886eabaf06a961df79034a9462742eeb8dfbaca8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:da029e35ebef371b4dfbf55861183bc9f0c002e69d234ebb09991c96ce0f9331
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
$ docker pull buildpack-deps@sha256:c13a1297fba054038daa3f04fe6f0c1af2a9796e83d088dd727fbd7301352bb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139704811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206c77e128bfb0edf1840489b8633d92a43ba52ba83e197190a701037e74e75b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271cd5a2233f0950e0047c5ef70615565f18b1eb82b465bd4022186677b3a0e3`  
		Last Modified: Fri, 27 Sep 2024 05:17:40 GMT  
		Size: 66.2 MB (66232209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3932ab202661f88e73ea8b94d7dd6c72cbc894f448b48ed04dc86d6e1d438084
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133091954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c5e5de1eaff0c2ae5aaa3629a26ab3ee8f288eb02c0fcc2d338c4c1b2c6142`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33a076b656ffa1590cb3af11ac35caa4cafc5418c987ee43ff730ce6667124`  
		Last Modified: Fri, 27 Sep 2024 04:05:55 GMT  
		Size: 63.7 MB (63678959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:053ee781c68e0d80fbcad4bb1fc6ef24f20705f8a43c45be1e9ede6bb990e7be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127423556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526062e2e04d2ddd719664f3e5b2a4dc4611137832180752268433ca2ae0913f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37dd52fd002bb99bd49c9bed7893185cc0dba9fb61e6876b290d76592b7648bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139904889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83450b181a65930ccb9e202233c0b03c9eb558bb321fe45618331e73373d36`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ae5803a1a5ced75a83b41fa2bd6fb91c53487f277d030f7f641a4e2b913cefb7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143393161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49f482ee10753303cfa3809f15a43f63ee996510bd4197e3b7dd4f1e9947fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146c248c1b9df1279d1bc34451bbfaa5ca72d7e3bf28372ac12a9ce2a2af65ad`  
		Last Modified: Fri, 27 Sep 2024 08:11:09 GMT  
		Size: 68.0 MB (68023503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3691559da49439229feea5bab817f8029db0c10bdfee4b38a8373d6e29afc97d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137707349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6fd827349d7fd9979ff9a67e9afcba00400eb9c8e6e13123a6a70343b205c1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816183487bc68f313f38e3315ac6bc39afe27875baa50865d4d9f7b974ebbe24`  
		Last Modified: Fri, 27 Sep 2024 11:09:04 GMT  
		Size: 65.0 MB (64999739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2772a28b7eb1d6e53a6cb834c6ef3a79c3f548c44304a822bce9b6c698a29b2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151594721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29765f2f199783688b590749bbbe932a80af79ad26f06459fab3d9496f7aed62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:01:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c552054a471b4255e6efa87c7bc0c63ba0466655c5644bfdade3677310ec65c`  
		Last Modified: Fri, 27 Sep 2024 06:07:11 GMT  
		Size: 71.6 MB (71553163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4737253869238b730cc24ce2a1c76597f79bd78f9e3d303b975e12b3f058c433
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141422388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fdc194f0364e41cbd14b2f7c0f6922ee0c388c0f15df6c99eee1ea6933947`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:ae0cffdfd009583bacc47bb91fc2e7a2f7d0874d8895a3d690d4e5c9d055ebe6
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
$ docker pull buildpack-deps@sha256:8ef56987777fd5cc83b244bea06f71a52e067d4a3573dd4d9e46426da7e3b794
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366958012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc459e0d4b28f0722a6ad59e7d70cb78c0aa037d87666e9c2ee63e04085fe71e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:13:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271cd5a2233f0950e0047c5ef70615565f18b1eb82b465bd4022186677b3a0e3`  
		Last Modified: Fri, 27 Sep 2024 05:17:40 GMT  
		Size: 66.2 MB (66232209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caec85693b42c7320c4c42dad676e7729de43a3e75de092afc9069f0060a3e5`  
		Last Modified: Fri, 27 Sep 2024 05:18:14 GMT  
		Size: 227.3 MB (227253201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a702af9257ea6649053fdb5c5801607a829b7d01672205b726401c8128e958bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335462987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322342ca71be45e54db169d641b33b9049fb9f8e9e2db499781674dd529d1c99`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33a076b656ffa1590cb3af11ac35caa4cafc5418c987ee43ff730ce6667124`  
		Last Modified: Fri, 27 Sep 2024 04:05:55 GMT  
		Size: 63.7 MB (63678959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b391cda3e9681d641f974d78e09b872a28e4dbbc868b58887bc63c79773685ef`  
		Last Modified: Fri, 27 Sep 2024 04:06:30 GMT  
		Size: 202.4 MB (202371033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cf5f7f2b3d1e7e053937847cd1d54aae5660d0b109ec06b1e37407c516026f08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316886587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908e66f98eb6616f1e3e4995f88f43cac97b623cdf136f562ae4b5605d03b26d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:37:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985eaffb50a16b04f512a5978f60707cec0ee2ee400d8df8eed0a4f2ae4e7bb`  
		Last Modified: Fri, 27 Sep 2024 07:43:04 GMT  
		Size: 189.5 MB (189463031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6eb1f5a4d0fbaa0738de62ec4ce5cad85bc0deab8318212832033be1d4e44227
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.8 MB (360841180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5170670a1b59e433d47ac1c2f5b6cbd4cb569be345029c90a37adc178439fa3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46608e24e871aeb173029569f11931335886e512f79bc654f51a4aa982f67d8`  
		Last Modified: Fri, 27 Sep 2024 05:28:17 GMT  
		Size: 220.9 MB (220936291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2decb729ef9d6a3e32c10577537efc0add6e5f9df995fee2a00a1b3319c51a6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371489677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd72c109ae60fdf2258bd4f815f9c581638526f9fc3d6087eb2a165550b20fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:06:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146c248c1b9df1279d1bc34451bbfaa5ca72d7e3bf28372ac12a9ce2a2af65ad`  
		Last Modified: Fri, 27 Sep 2024 08:11:09 GMT  
		Size: 68.0 MB (68023503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358825efffd1f6da3c20226a36432d1a31ff644b5ead94b4a2cca864377e042f`  
		Last Modified: Fri, 27 Sep 2024 08:11:57 GMT  
		Size: 228.1 MB (228096516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e8b34340c491b168793c8194cf3ba79c7c8f75ea8811169bd87769e85581458f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345169031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b036904e38b7604d964773dc03770759f4897eb01f8881dc506b7ed1a27a90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 11:00:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816183487bc68f313f38e3315ac6bc39afe27875baa50865d4d9f7b974ebbe24`  
		Last Modified: Fri, 27 Sep 2024 11:09:04 GMT  
		Size: 65.0 MB (64999739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a51967b8f4cf1b2d850d26a139c5f1d7e8e41b709c161d9eee6061bc4dc74f3`  
		Last Modified: Fri, 27 Sep 2024 11:11:17 GMT  
		Size: 207.5 MB (207461682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7436b5b7db65cd5a624600a1deeef5c873d96bdad3f435f9fef4b991fa46a014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377576280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3c82a2612f21cfb3e020d6a1179a1339b2674541a1bdbe7f3aae822f6e52ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:01:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:03:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c552054a471b4255e6efa87c7bc0c63ba0466655c5644bfdade3677310ec65c`  
		Last Modified: Fri, 27 Sep 2024 06:07:11 GMT  
		Size: 71.6 MB (71553163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f28b4807d4b640478c00c941befcc03e7516d529f7038a9e613825c62ecd05`  
		Last Modified: Fri, 27 Sep 2024 06:07:52 GMT  
		Size: 226.0 MB (225981559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d5b8b5e2291d7c8cc065f3f18775309ccd2ba7d9bd1efaa8de0eb044d6793b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342226166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ef9bf1106f34529cc7819079b623b933e37a3488161ce834b76eec5ab53c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f620222e1943a71639f47a8405e2a62c61af833945aaefd53d6e4523b5853a8`  
		Last Modified: Fri, 27 Sep 2024 03:22:45 GMT  
		Size: 200.8 MB (200803778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:a2865529aa6ef65d66c43f5e91d94a93e7aec1217db37aa0a6a0f4ec0a896de1
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
$ docker pull buildpack-deps@sha256:4c612a64fbbedd375ae2f6a13caabb608d2b14d46ea4474fbba5acb84f08f2dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73472602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dc983b92201256daec01ef64b348f51b2d5cc274b81ffe01a795142a064737`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:511848f89ac6a9a59f3a996fa2313c2388ad6d9586959bfe53c4efb8360c0b0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69412995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebd13eb50f8d1965d055ddc0a5075c31cd7dd24537c24838d2f298c9407d8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98d0d2d989c716ceacab3193640a9356b37fa827f72314d00a0270c8006197f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66262823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7602a452f4245dfc17d03f43f1bc3130eebba36523027d5e4c9116d704a13c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9aef11957c014ee01c467128ef31a08b32c6953f31ab48378266d1d08cfb0599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830955de46667fa98d512e386318f49ac6b2fe117dbdd5900d9bcc4c8945eefd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d689396f888b6815f6a9d0f7298fd242f2f77cafac80321b1642a05eb661a39a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75369658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0043e8cc00bd545c060f11bb04b7fc66ce057873e9d3f026858abe4b01a466`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b0efa492445a57ae8f018beda4851659a8e6053a22551603bc71c032105227f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a371a0285e3282b682d0fbe1dd7641d3091c0f79793691f7a9a26b96272421dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67b5d9ed541257d6e7b0df6d704b584840267e267ce4aca7916a91445998a679
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80041558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9902d8e9389a2a68eb6148b4670a752f6b44e04ea16d3fda06e7857e2a42494`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4e5a879b654c7c746335d5c86a83cb9cf26be40ec7ff2bc53b6e28d0ad3f6463
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71302497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7431eff14b4cf260214e2c7494998e25d9583b82cbc1558c76e490b08c437b30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:27:18 GMT
ADD file:da1da406a30d8c871e2184104ce67d821e790fe334361223691352f3f2de2066 in / 
# Fri, 27 Sep 2024 12:27:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:58:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0a4dce9b327b8993d0aa8d580f47160e8320c3015f48472eedbf0d06fbb649df`  
		Last Modified: Fri, 27 Sep 2024 12:33:20 GMT  
		Size: 51.5 MB (51492798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dbfe1ea856752f068e2a64375dcf7a47fa54aacb79b8eb7df476c2bc442322`  
		Last Modified: Fri, 27 Sep 2024 14:07:27 GMT  
		Size: 19.8 MB (19809699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7a815adf7f34038e8af8937945bc9715fd6dd87d23264894e5b58ec62369aef2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74165458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab392593f47f6c95908f64b1886eabaf06a961df79034a9462742eeb8dfbaca8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:da029e35ebef371b4dfbf55861183bc9f0c002e69d234ebb09991c96ce0f9331
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
$ docker pull buildpack-deps@sha256:c13a1297fba054038daa3f04fe6f0c1af2a9796e83d088dd727fbd7301352bb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139704811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206c77e128bfb0edf1840489b8633d92a43ba52ba83e197190a701037e74e75b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271cd5a2233f0950e0047c5ef70615565f18b1eb82b465bd4022186677b3a0e3`  
		Last Modified: Fri, 27 Sep 2024 05:17:40 GMT  
		Size: 66.2 MB (66232209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3932ab202661f88e73ea8b94d7dd6c72cbc894f448b48ed04dc86d6e1d438084
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133091954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c5e5de1eaff0c2ae5aaa3629a26ab3ee8f288eb02c0fcc2d338c4c1b2c6142`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33a076b656ffa1590cb3af11ac35caa4cafc5418c987ee43ff730ce6667124`  
		Last Modified: Fri, 27 Sep 2024 04:05:55 GMT  
		Size: 63.7 MB (63678959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:053ee781c68e0d80fbcad4bb1fc6ef24f20705f8a43c45be1e9ede6bb990e7be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127423556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526062e2e04d2ddd719664f3e5b2a4dc4611137832180752268433ca2ae0913f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37dd52fd002bb99bd49c9bed7893185cc0dba9fb61e6876b290d76592b7648bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139904889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83450b181a65930ccb9e202233c0b03c9eb558bb321fe45618331e73373d36`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ae5803a1a5ced75a83b41fa2bd6fb91c53487f277d030f7f641a4e2b913cefb7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143393161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49f482ee10753303cfa3809f15a43f63ee996510bd4197e3b7dd4f1e9947fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146c248c1b9df1279d1bc34451bbfaa5ca72d7e3bf28372ac12a9ce2a2af65ad`  
		Last Modified: Fri, 27 Sep 2024 08:11:09 GMT  
		Size: 68.0 MB (68023503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3691559da49439229feea5bab817f8029db0c10bdfee4b38a8373d6e29afc97d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137707349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6fd827349d7fd9979ff9a67e9afcba00400eb9c8e6e13123a6a70343b205c1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816183487bc68f313f38e3315ac6bc39afe27875baa50865d4d9f7b974ebbe24`  
		Last Modified: Fri, 27 Sep 2024 11:09:04 GMT  
		Size: 65.0 MB (64999739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2772a28b7eb1d6e53a6cb834c6ef3a79c3f548c44304a822bce9b6c698a29b2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151594721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29765f2f199783688b590749bbbe932a80af79ad26f06459fab3d9496f7aed62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:01:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c552054a471b4255e6efa87c7bc0c63ba0466655c5644bfdade3677310ec65c`  
		Last Modified: Fri, 27 Sep 2024 06:07:11 GMT  
		Size: 71.6 MB (71553163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4737253869238b730cc24ce2a1c76597f79bd78f9e3d303b975e12b3f058c433
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141422388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fdc194f0364e41cbd14b2f7c0f6922ee0c388c0f15df6c99eee1ea6933947`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:f54c77ee8ad6e7825ffc8b0aee14317bc174132e793317459fe39d7c27e7c550
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
$ docker pull buildpack-deps@sha256:ee76f9c492d0f4072868e40d1250a1ce243aac136384fefc31fe01e9aeea11e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367357446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b457d4ee4cfc4ebb25157e51045e62481112e0746dfe3d9f2508e00b1f64c0e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d824605d3973d8333c12588307d4b7865a9d16a172cf713a69bed064281a179`  
		Last Modified: Fri, 27 Sep 2024 05:16:40 GMT  
		Size: 66.3 MB (66298648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e9cccb32adeb73089e38bb77d73d59c2177bbb495bbbc4bac305a228188d9`  
		Last Modified: Fri, 27 Sep 2024 05:17:14 GMT  
		Size: 227.4 MB (227404144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c37c2fe099ca8c852db765ea796c72a5565fce2c9957748d192a6d2330d45ce7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335802621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959ed346fcd14aab877dc44925c39b738c268a59db692c7ca7224cecb1a1c14a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:00:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03463b6c07bccc1364fec128e533c62c4e2533ee53250fc1153a70167b6f44b`  
		Last Modified: Fri, 27 Sep 2024 04:04:50 GMT  
		Size: 63.8 MB (63754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03773ce488248829376500af9b84cf97fcd39ed3242f9e2187079b56c71ea969`  
		Last Modified: Fri, 27 Sep 2024 04:05:25 GMT  
		Size: 202.5 MB (202482927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7dce74814ac71c3c1a030db777e581f1ccd7233b7ba27541b483b18f3662dbe4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317241853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e048cf3ab5d5edb6ad2b4ddbaaeaf5b699f98ca7db295e0a9416b4eacc47e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:35:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cad0c26ab0027c184690fde3603662a1fe5a37591c336a98696770ac66936e`  
		Last Modified: Fri, 27 Sep 2024 07:41:21 GMT  
		Size: 61.2 MB (61234643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e907df1326f4d0916b686b69508feaf27c5bfc2aa38710924f377f75b7fdbe09`  
		Last Modified: Fri, 27 Sep 2024 07:42:01 GMT  
		Size: 189.6 MB (189579676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2dcc03ae0e069e97bd427e3523013055888d7649c17b947c1770b684987e7b37
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361024922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34275d796bc4304378c9c4f5a93c485125d7f567b96e662711a64b21fef728bd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:22:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd393ac9d5f3e6f4ef01c240e4ee33361f9163326dc4fe0c98ca544756cddc12`  
		Last Modified: Fri, 27 Sep 2024 05:26:51 GMT  
		Size: 66.3 MB (66302891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac170a650f31dab130f92fb8708276d55343d8d7ee851c19b5b9f257acdd6f4`  
		Last Modified: Fri, 27 Sep 2024 05:27:19 GMT  
		Size: 221.0 MB (220988693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ded01fb58e652afea4c8e7094453b5af95454a57d274207a2bb3eb8d67ba93a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371902498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb6475fc00c3a209abc95fa65afc37a1ed13142d0bb884b32069569704b4147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:02:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:04:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71b0341053ee8776ca7ecfc201a051da349ec1f8e5c73b5d4a043fd3154532`  
		Last Modified: Fri, 27 Sep 2024 08:09:48 GMT  
		Size: 68.1 MB (68105180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f792864bd7cba3961b251eec2e1ee9f352895552addc1e17511d0c39b02e56ab`  
		Last Modified: Fri, 27 Sep 2024 08:10:36 GMT  
		Size: 228.2 MB (228233735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2cfdb4463136f7a7fd6a964fc3abeffe5f208f66260fd0eaf0c70642e5386419
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344950889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66d337adcb0f1ef97b6662438438bd5c5fdf7cf39e624d1a8af498fbb4b2d2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:51:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d0102a70641af727b17e4dda29d3e752776fe5f927c48dc6ba42534da6baf`  
		Last Modified: Fri, 27 Sep 2024 11:05:38 GMT  
		Size: 65.1 MB (65067190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3393aec747705ef0a675939b6f883a7ca72a36da98e766e42ca2a7286e7af3dc`  
		Last Modified: Fri, 27 Sep 2024 11:07:51 GMT  
		Size: 207.0 MB (207030957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:33011240df37cdf38b23d38f03d17a12051d05e4b3d94c36635ddd57eafd1713
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377881836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51344e88f1f121524c87aeabda4282378ca7a7659586aa483fb44b98340e72a2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:00:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83256233144f0df0689578c0a89c181e74e6ea6cc435661a805b2a60809bd43d`  
		Last Modified: Fri, 27 Sep 2024 06:05:59 GMT  
		Size: 71.6 MB (71626121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751e854e69a77c78cd9663a65ff9e955dcc052e392333a04a5bf6bd4c25ebb97`  
		Last Modified: Fri, 27 Sep 2024 06:06:39 GMT  
		Size: 226.1 MB (226106927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1e96e7d98bcaad26df0722874971218e5cf4a3a99c344592ce451798f947f237
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.2 MB (448211534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82239ca4ec79855f9c4e0b72e27e8d0bfa5763224bc3e1e71f6749abb66715f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:57:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9f4a99275f793e5c8e68b8d73f18d109d2b326d17fb8683a66ed765527984`  
		Last Modified: Fri, 27 Sep 2024 14:01:33 GMT  
		Size: 65.5 MB (65531769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7485ff1326cbcb09db2dd7bbb6906908774b101e4ad4c8f61975c7a8036b5490`  
		Last Modified: Fri, 27 Sep 2024 14:07:02 GMT  
		Size: 311.3 MB (311251420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:02d80f6064f4d0e45507e4fb2c58bcaea875e315d0609b0be609a084766835cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342486230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3180d78e39311bbb86438bcfae83a1c25a9665ba35a16eda55358e509b4479f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:16:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cedf4fdb3f455010b1f7eeb3d9f24a25a7fd469356a31a9f5f4de26d8238f1b`  
		Last Modified: Fri, 27 Sep 2024 03:21:27 GMT  
		Size: 67.3 MB (67330712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a95e4129bf276881f4c92fb92d3cf0bad3b55875c49bb65e8462f3ef6fecfb5`  
		Last Modified: Fri, 27 Sep 2024 03:21:55 GMT  
		Size: 200.9 MB (200921345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:586835792a6c444c692e1f1ba19d9e916fa326a26a1e5c46d92911025ce4a744
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
$ docker pull buildpack-deps@sha256:d4e775cb76782502bd02eece1eda4b0a8d55a4d3ee1dc17c14b09feafd209899
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73654654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bdfa4dad25173a03ab31b77b3e6e228879dd9ed3040b7767dff741d2e6ce27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:326c47ff85ea598c88a6373d582ef1c6de0eb3fc0b7f6a9fa9f59250ea5f813f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69564930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c238989bfbc727c388dd851fa69e387bedaa311f086ed31c2213d306af10bb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:087a4e515cf7a1f37454402410d12026217e390490710553bdd7b56bbe281d84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66427534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c64bff340794dad4d2c5fe7fde8be11e10f84ef198a2af322e27fbb2e8c5e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8400ef23e2bfc1cf7961db7e7fc5cc365c21fc94bd265e5586c1ac7001d823c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73733338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaa242a8c35f491600ed256f8fa81f930e3e3971e3b401d781772eabee39a12`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7802476f80697b0d8d2e5d71ab473170f26b519bb144992d6add93dd482b2718
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75563583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6442f8185858decdddf033823e4bf8efbf0c130cc1fa8d22fd5c1d3018536d6e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae678d42d522c5a885a907970dd730a90c8669064fda9c6bef043fa42739b6ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72852742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a62a61aa389cf6527efd964175baf68a829cb84e2d4cc5d3690fc671cec76e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7dfe7f2474c97c8c5c6c60643147edd25a2275ef8d96ac019c47a72b54bd5c51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80148788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125d9685f5ce2e879b85d739962910d5e860f1cbd233aec7a11ac062aa49456`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:be7a4796ea31bfba3509caac3d8e05901ce05dd65a120cc12a3dac0cc3c2be9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0809c76f2424482deec4c8cfcbd1845c22bd604642587f9913b0c256989079a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:32a8c0af96f9a31118c91a08bf2f2cf38dc4b986a325557d84203f43c7b6cdcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74234173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9eee7a70ef8c4b7ebb8b8e5353eb05a0035489844aa9fbd353097589d36973d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:6f73b50eb212126c3ddc1535f35589762e4465547b7daff38f81d11448ed92d8
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
$ docker pull buildpack-deps@sha256:ea2eee0ac8d30d5443afc420f583d8e8c912153fc14e9aa31f89dc0d9a5eb107
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139953302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4694df930c2fc62cefd789b61bf38323f8cabb232ac9eac2e10a8e2d93b50ab0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d824605d3973d8333c12588307d4b7865a9d16a172cf713a69bed064281a179`  
		Last Modified: Fri, 27 Sep 2024 05:16:40 GMT  
		Size: 66.3 MB (66298648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:01d2dd0dee2fd58f2253a6f26e754440b8c0515b6171462c890bfb5257a16def
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133319694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24d0b4c956ac03e07ee2103998239b5293708df10144188615f97ae3e5c8720`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03463b6c07bccc1364fec128e533c62c4e2533ee53250fc1153a70167b6f44b`  
		Last Modified: Fri, 27 Sep 2024 04:04:50 GMT  
		Size: 63.8 MB (63754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17cd05150504f279feed04079948b74f6e364d1682b04e9040e80caa426db01c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127662177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a55dab28cc2ae523f094e6efebc21ebe56b8b362c582c1c533e962dbed93e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cad0c26ab0027c184690fde3603662a1fe5a37591c336a98696770ac66936e`  
		Last Modified: Fri, 27 Sep 2024 07:41:21 GMT  
		Size: 61.2 MB (61234643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5f513a1c5f215d83b71b8cbd64ca21887cb12f01b07695a7ffdf01a67e2b0fd2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140036229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36031ec48fc57c491b354b9d8b65ff95c5876b9efaab45a0c871a1ece21d7b30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd393ac9d5f3e6f4ef01c240e4ee33361f9163326dc4fe0c98ca544756cddc12`  
		Last Modified: Fri, 27 Sep 2024 05:26:51 GMT  
		Size: 66.3 MB (66302891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:53e3eccac956f1d4ee4d99fcea327f66677b769148b25ae648c5a18bd6174a4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143668763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8798ca05e5b30c95dc243061792aee08c62c51f8c2a63aa060afaa288059e2ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:02:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71b0341053ee8776ca7ecfc201a051da349ec1f8e5c73b5d4a043fd3154532`  
		Last Modified: Fri, 27 Sep 2024 08:09:48 GMT  
		Size: 68.1 MB (68105180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:81b3eb351c29e1eee6d71447de5ff65324ab8ab5f47e41527137e7f86f17a573
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137919932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4aef28a5b9c90b1852dff723450b8f097427b7efea4336d6dc48df2542219a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d0102a70641af727b17e4dda29d3e752776fe5f927c48dc6ba42534da6baf`  
		Last Modified: Fri, 27 Sep 2024 11:05:38 GMT  
		Size: 65.1 MB (65067190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:41ea68f4856fcfc92d08450a4e126e0e2e50ddc67d7083e73f7989e8588b0c90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151774909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ff9635ca0f0e2eb1753e1b9d77119fe5100e04cb5dfa6565bf38e395943cc8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83256233144f0df0689578c0a89c181e74e6ea6cc435661a805b2a60809bd43d`  
		Last Modified: Fri, 27 Sep 2024 06:05:59 GMT  
		Size: 71.6 MB (71626121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0d34076051b03e658b59b9167c20d545d924469e7f2829509eceeb01e5b1f0c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136960114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122d6b276a8d897277117783348c16c5fb72421b777ea13632a0d12e90f081be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9f4a99275f793e5c8e68b8d73f18d109d2b326d17fb8683a66ed765527984`  
		Last Modified: Fri, 27 Sep 2024 14:01:33 GMT  
		Size: 65.5 MB (65531769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b141a1e4d3e090f1289387b4f386a06ff9a10536d71467dacc45743ffc85c099
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141564885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f6067781a4b36d561c120b2a47b037fb544c7e50607d9658b7102c0a97c16f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cedf4fdb3f455010b1f7eeb3d9f24a25a7fd469356a31a9f5f4de26d8238f1b`  
		Last Modified: Fri, 27 Sep 2024 03:21:27 GMT  
		Size: 67.3 MB (67330712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
