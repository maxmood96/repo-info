<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rust`

-	[`rust:1`](#rust1)
-	[`rust:1-alpine`](#rust1-alpine)
-	[`rust:1-alpine3.20`](#rust1-alpine320)
-	[`rust:1-alpine3.21`](#rust1-alpine321)
-	[`rust:1-bookworm`](#rust1-bookworm)
-	[`rust:1-bullseye`](#rust1-bullseye)
-	[`rust:1-slim`](#rust1-slim)
-	[`rust:1-slim-bookworm`](#rust1-slim-bookworm)
-	[`rust:1-slim-bullseye`](#rust1-slim-bullseye)
-	[`rust:1.84`](#rust184)
-	[`rust:1.84-alpine`](#rust184-alpine)
-	[`rust:1.84-alpine3.20`](#rust184-alpine320)
-	[`rust:1.84-alpine3.21`](#rust184-alpine321)
-	[`rust:1.84-bookworm`](#rust184-bookworm)
-	[`rust:1.84-bullseye`](#rust184-bullseye)
-	[`rust:1.84-slim`](#rust184-slim)
-	[`rust:1.84-slim-bookworm`](#rust184-slim-bookworm)
-	[`rust:1.84-slim-bullseye`](#rust184-slim-bullseye)
-	[`rust:1.84.0`](#rust1840)
-	[`rust:1.84.0-alpine`](#rust1840-alpine)
-	[`rust:1.84.0-alpine3.20`](#rust1840-alpine320)
-	[`rust:1.84.0-alpine3.21`](#rust1840-alpine321)
-	[`rust:1.84.0-bookworm`](#rust1840-bookworm)
-	[`rust:1.84.0-bullseye`](#rust1840-bullseye)
-	[`rust:1.84.0-slim`](#rust1840-slim)
-	[`rust:1.84.0-slim-bookworm`](#rust1840-slim-bookworm)
-	[`rust:1.84.0-slim-bullseye`](#rust1840-slim-bullseye)
-	[`rust:alpine`](#rustalpine)
-	[`rust:alpine3.20`](#rustalpine320)
-	[`rust:alpine3.21`](#rustalpine321)
-	[`rust:bookworm`](#rustbookworm)
-	[`rust:bullseye`](#rustbullseye)
-	[`rust:latest`](#rustlatest)
-	[`rust:slim`](#rustslim)
-	[`rust:slim-bookworm`](#rustslim-bookworm)
-	[`rust:slim-bullseye`](#rustslim-bullseye)

## `rust:1`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:8b2e66b58b7b5a0181019e2ac12d6b4c2e550b2e6889ecfc2a12d10f4579894a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:1a866b68d2adb80492e3e996f84999d692c20a34c3ca1a21d8bd2b448993a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298337931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7ee796e3d6fa94b33642d35bf166294523ccf3a26389f8228de309940821`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ff15df1191be1ba73e0551f9604556c59601352359b9ddcd56df3db87838e3`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 55.3 MB (55315358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cfb1a53cd02005ecbbef1bf5c7908122591c89f17c20073a82364a982bddf`  
		Last Modified: Thu, 09 Jan 2025 22:29:55 GMT  
		Size: 239.4 MB (239396313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:609a9e76a5909373fe3ed8f7b522150f67e80681ceb707ea9a5677692d239a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46a007e2e5a282e2ab6fe96bec9e3e15b65a8a803bd9c29e506a009e90910d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c6a5a2ada3ef89e80c205bc878b8be8f529a5f096b1dc60fd7a94db1b6442c`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd25cef9e4659903109b2c2b5cef038ae26f5cad4d5ca689fc8b7aaf77ca5fd`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8d98865f36d4249e0faa69209325e70adc561ac43355de0a1469cbb04b12479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300990769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d1fb945f7649689a77349b66020e055e8362f207aa387c94cb30a12d615de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b4f23fe7caefa44f7fedf6c6ad6331c9647daa81ec320381013cb4987762a`  
		Last Modified: Thu, 09 Jan 2025 05:56:18 GMT  
		Size: 53.0 MB (52951004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f078a134c6d3bfbf3e51f6cf7d7215b3b9a168bfc794609656888a9123c68f5`  
		Last Modified: Thu, 09 Jan 2025 22:46:24 GMT  
		Size: 243.9 MB (243948996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:8eb282a9a9f00e4c2eafa1071b34f2dae2b421ae503a972eb948197a6b0d89f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a939431982c0dbaf5b921fb551b6df6df396a5d3ad4341bdb440eb5c687fb9`

```dockerfile
```

-	Layers:
	-	`sha256:131c73a03f3ebbeb19acca7099852ab177e0165420ebbdfad542fa4fcae54f98`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083bff1fc4a6ac0159bd3b6bfb7e2529474fd78d774f9e70650e53a48ac7aaca`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:eaa0847dbdd260f39213a70fe9016ab83c2f4f4a1148ed53e3447b131b42fe22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2fd89ac12ed4061cb5a73c7809aa788c6f6b126e1d654295bce5ac00d14dfa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516059596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef02c2c79b9b8cc8dc8bb0644931dccb3de60a205fd7951b6b41c6e3eff3d23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff86202e7c3afa44ea1524a6f7520668801c0913bb650d2d105f267afcdc35`  
		Last Modified: Tue, 14 Jan 2025 04:16:44 GMT  
		Size: 197.1 MB (197073993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69f21d4b6500dd2eb40bcff9c3d8c70e4cdcbf23ee32f669a2b231dfca18a7`  
		Last Modified: Tue, 14 Jan 2025 05:23:32 GMT  
		Size: 194.9 MB (194934543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ce3fa42f06b943caa59c9b80a065e42cc262a4633c82c416b335d62c68b870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e297baa62e0bb3b5a8eb2383a802b7efd5ef65911e6208865778cbdd8053fcc5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae86dc6fc207bf2ebdc0b702ecb77c987cbaeb4c0469429240f5a890f310daa`  
		Last Modified: Tue, 14 Jan 2025 05:23:29 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57bd9b7bcc0f4ca719b900dd7f0cd81e77842afa77b0396d199b838fa62f07c5`  
		Last Modified: Tue, 14 Jan 2025 05:23:28 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:871ce791ca420097d2b8e1571fe2b84be3eaaa86316bff514741c433e05d5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded8b95ced658873224c8659cfee475812a31a6cb020639ad1fbc8b484c679d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a2aea83640d58c933777151ebe00fe790d8b0869986ddef8f4b6657086f68c`  
		Last Modified: Wed, 15 Jan 2025 10:20:35 GMT  
		Size: 230.9 MB (230905635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4dac81db1f486e0d9fef1804f4140b13067f799718646f509ee347517ccf48c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700f82deebaf5c4590fd6ed7bd33c0a729a0145d786ba8a37b610b9d6a891745`

```dockerfile
```

-	Layers:
	-	`sha256:5c10cc2f9a1c2deb3a8f87a4c032bdf4a30de750cb5657582f58569ba166bfa8`  
		Last Modified: Wed, 15 Jan 2025 10:20:30 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8452084868fd89c612737f9f5e7dba6b8e34f92e251a0d54ca7efb1ff85a867d`  
		Last Modified: Wed, 15 Jan 2025 10:20:29 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b7e64ab71f5f86b3d836e9f516d8cd4bfaeba11f1903846278a9a02ed3c7c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570920449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa52a0eb5f79f7fbe1c417685d7720e09508920730b7617d35cced393b3d85cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8fbaa7907ee22571084279c601f14a265f51a5d724c32c5998a32a816fee1`  
		Last Modified: Thu, 09 Jan 2025 22:40:57 GMT  
		Size: 258.3 MB (258298411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c43a6c324bee7339a01235ae3f8add2d90fe7af6242a5baff29d13fdda43375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f1d8728f1c6c83d7d6e362f2a188a4c1798a757f6d2d265a4c9aeefa9918a6`

```dockerfile
```

-	Layers:
	-	`sha256:3ef50a7c55f348deb0ca7fbb92416cbf3dba64a6c873d5e6f36841c131b898d4`  
		Last Modified: Thu, 09 Jan 2025 22:40:51 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beaa953ff4cf7058098ec1d47f065d3f98b7409d9348fdbbddee897bcf48efc3`  
		Last Modified: Thu, 09 Jan 2025 22:40:50 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c17640850a0134370e2362bf3b7f6ab71f51d41886631847c98bd5360880f6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538184584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf739b3ee6543078b71a4bc2af3bae848066814306dc1b8057a587188caa49a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d0c381a5fdef1263d351e698c4afefeb15eebaa7c61c01a804b75362d039c4`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 16.1 MB (16061977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411024e8ae7dadedef448d7486b9035f3faedd43c62d2f773ed5d8f87362be0`  
		Last Modified: Tue, 14 Jan 2025 03:18:01 GMT  
		Size: 56.0 MB (56027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84d528e2732f18fed0f874f321917023842dc0f688eba487bec08562c3d8257`  
		Last Modified: Tue, 14 Jan 2025 04:16:55 GMT  
		Size: 200.0 MB (199979639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1890215ad1b9e7b795b8c3bcfdfa6316e86672addf33781986c40986200b30b3`  
		Last Modified: Tue, 14 Jan 2025 05:22:51 GMT  
		Size: 211.4 MB (211439547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dc095e114c22f2ea16954569e0b3e7765be2d40adcdcb4d45f9f40cf79ab9d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925afed10c23ff4c08e6186896e33df867a7a335d40a7af668b88b57afd5974f`

```dockerfile
```

-	Layers:
	-	`sha256:5e768d69c73b3c337285285f38146e2bc44606db37942e086b9711d44782c464`  
		Last Modified: Tue, 14 Jan 2025 05:22:47 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376e21ec95e43ad873259ff922b786ef57ca85f59549c2c6f80037dc438c5e78`  
		Last Modified: Tue, 14 Jan 2025 05:22:45 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:249b2de69e9d46230a225a71cb6bc166bb121acf2d66a6a23e0541154982c0df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2b5612d7b9c4331afe31226f40ba0a93d0b4fc349613bd282fe24b9715588827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285135891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db4d4004f1e1ff5c8c9551e91a98e6f155d5ff00c2b07338bae2a07cbff3ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea54e8ff51c7c9836420c4c189bd6a92a86a6332b2a3060cc3c2723a971d0b2`  
		Last Modified: Tue, 14 Jan 2025 02:19:50 GMT  
		Size: 254.9 MB (254883226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9071d1169765fbe1a946e7d8bbe3c0e268d6936be6e583409abe80c66aa9c58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dfad0599bcb2789ec36960f9099a91ab54a88652d8732322a8435f369e0e70`

```dockerfile
```

-	Layers:
	-	`sha256:4ad821a5ac880981ec294fc435d2b2c5848d3ba8e664a0e75a6462c57d3db34a`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e7375df865f0e28c4d31d09cc67995b4f1f8cfce180e9a33689a2112549a63`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:de6279776a815580500fb609083c2fe02117485aafbea7ae03aadbb8a7176afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c11918617732fd8c3c49a3f81e21b4815ff2b57a74e651127956f808aa43a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc52732c036f97c2f7f57efb3ab6d3b390481ece5426c086be618f7944a27b53`  
		Last Modified: Tue, 14 Jan 2025 15:20:06 GMT  
		Size: 273.0 MB (272976225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e51a8477401fca0e43abaa887b84f40e08d5f30f1a980b525ceda02765cbb605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f82a5f3c6e2a39d9e7a7fb173aefd11ccf832dcc5c6f0606cc049549d5fc60e`

```dockerfile
```

-	Layers:
	-	`sha256:00ced8b920f88eaa1366c355470398754dfeb0653ac7a01525e62c80e3089f19`  
		Last Modified: Tue, 14 Jan 2025 15:20:00 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fc47c5382a1d1130089734018473e6152bb094a90e0dae788cd7475498dc21`  
		Last Modified: Tue, 14 Jan 2025 15:19:59 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5260ecf55f369662a15414ec3490df728a5a9755414ab642127a4a7958d5ddbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0ff0c34b7a526ead79d15589f4fc07f3ec64f3d04300a5d275208e2e6ae2a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f28991d37cc716e65fa31b32b0fadfe580f4a6c8fb373e8c17cff772becc8f`  
		Last Modified: Tue, 14 Jan 2025 11:46:07 GMT  
		Size: 313.8 MB (313801833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbdbed22362995bd837fcde74928fe4dec4352f3837df2b1a2c761592e0b992d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1a00040c42b0220bbe52afa8c18ee0595d5b1a0d0bd9d752c015601f68115`

```dockerfile
```

-	Layers:
	-	`sha256:92ccf2fa5de715523928957650c60ed97ba3b7ce6d7c3d8a705b364f2db8f37d`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40f83054b032a48a466def65ad7b6e6897eca06a5a69341b41a338c5b405cd1`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:65319b92e9b07d523850dc0e024c02d094460fc9061acaef0ec20f218bf97af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303174112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b1fe80f5100fd17367b5b11b0ca2877dd39015304816091c7710e3a4f3491`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a84d82f065bab8e92c2a584d90458a0108031daee4f6472d0761cb90d24a70`  
		Last Modified: Tue, 14 Jan 2025 02:38:03 GMT  
		Size: 272.0 MB (271995083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0ab56bb29ff52bd366bbc16f121e03e7f0976940ba70eb96d23eacdddbb9e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1830bdadf3b01511162f732ad1247b47cc02c8d7000895c2445f7a3d58a8000b`

```dockerfile
```

-	Layers:
	-	`sha256:bcc431f2d4567a9a6f678bf9b1b4039c259b1f7fca00cb8227397fd6869fccbe`  
		Last Modified: Tue, 14 Jan 2025 02:37:57 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af005555ed40dc6af87e07ec4f6b9f51ec5cb79c36ebb870a18f02cdcdb8eb51`  
		Last Modified: Tue, 14 Jan 2025 02:37:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-alpine`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84-alpine` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-alpine3.20`

```console
$ docker pull rust@sha256:8b2e66b58b7b5a0181019e2ac12d6b4c2e550b2e6889ecfc2a12d10f4579894a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:1a866b68d2adb80492e3e996f84999d692c20a34c3ca1a21d8bd2b448993a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298337931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7ee796e3d6fa94b33642d35bf166294523ccf3a26389f8228de309940821`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ff15df1191be1ba73e0551f9604556c59601352359b9ddcd56df3db87838e3`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 55.3 MB (55315358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cfb1a53cd02005ecbbef1bf5c7908122591c89f17c20073a82364a982bddf`  
		Last Modified: Thu, 09 Jan 2025 22:29:55 GMT  
		Size: 239.4 MB (239396313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:609a9e76a5909373fe3ed8f7b522150f67e80681ceb707ea9a5677692d239a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46a007e2e5a282e2ab6fe96bec9e3e15b65a8a803bd9c29e506a009e90910d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c6a5a2ada3ef89e80c205bc878b8be8f529a5f096b1dc60fd7a94db1b6442c`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd25cef9e4659903109b2c2b5cef038ae26f5cad4d5ca689fc8b7aaf77ca5fd`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8d98865f36d4249e0faa69209325e70adc561ac43355de0a1469cbb04b12479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300990769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d1fb945f7649689a77349b66020e055e8362f207aa387c94cb30a12d615de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b4f23fe7caefa44f7fedf6c6ad6331c9647daa81ec320381013cb4987762a`  
		Last Modified: Thu, 09 Jan 2025 05:56:18 GMT  
		Size: 53.0 MB (52951004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f078a134c6d3bfbf3e51f6cf7d7215b3b9a168bfc794609656888a9123c68f5`  
		Last Modified: Thu, 09 Jan 2025 22:46:24 GMT  
		Size: 243.9 MB (243948996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:8eb282a9a9f00e4c2eafa1071b34f2dae2b421ae503a972eb948197a6b0d89f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a939431982c0dbaf5b921fb551b6df6df396a5d3ad4341bdb440eb5c687fb9`

```dockerfile
```

-	Layers:
	-	`sha256:131c73a03f3ebbeb19acca7099852ab177e0165420ebbdfad542fa4fcae54f98`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083bff1fc4a6ac0159bd3b6bfb7e2529474fd78d774f9e70650e53a48ac7aaca`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-alpine3.21`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-bookworm`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-bullseye`

```console
$ docker pull rust@sha256:eaa0847dbdd260f39213a70fe9016ab83c2f4f4a1148ed53e3447b131b42fe22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.84-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2fd89ac12ed4061cb5a73c7809aa788c6f6b126e1d654295bce5ac00d14dfa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516059596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef02c2c79b9b8cc8dc8bb0644931dccb3de60a205fd7951b6b41c6e3eff3d23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff86202e7c3afa44ea1524a6f7520668801c0913bb650d2d105f267afcdc35`  
		Last Modified: Tue, 14 Jan 2025 04:16:44 GMT  
		Size: 197.1 MB (197073993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69f21d4b6500dd2eb40bcff9c3d8c70e4cdcbf23ee32f669a2b231dfca18a7`  
		Last Modified: Tue, 14 Jan 2025 05:23:32 GMT  
		Size: 194.9 MB (194934543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ce3fa42f06b943caa59c9b80a065e42cc262a4633c82c416b335d62c68b870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e297baa62e0bb3b5a8eb2383a802b7efd5ef65911e6208865778cbdd8053fcc5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae86dc6fc207bf2ebdc0b702ecb77c987cbaeb4c0469429240f5a890f310daa`  
		Last Modified: Tue, 14 Jan 2025 05:23:29 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57bd9b7bcc0f4ca719b900dd7f0cd81e77842afa77b0396d199b838fa62f07c5`  
		Last Modified: Tue, 14 Jan 2025 05:23:28 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:871ce791ca420097d2b8e1571fe2b84be3eaaa86316bff514741c433e05d5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded8b95ced658873224c8659cfee475812a31a6cb020639ad1fbc8b484c679d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a2aea83640d58c933777151ebe00fe790d8b0869986ddef8f4b6657086f68c`  
		Last Modified: Wed, 15 Jan 2025 10:20:35 GMT  
		Size: 230.9 MB (230905635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4dac81db1f486e0d9fef1804f4140b13067f799718646f509ee347517ccf48c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700f82deebaf5c4590fd6ed7bd33c0a729a0145d786ba8a37b610b9d6a891745`

```dockerfile
```

-	Layers:
	-	`sha256:5c10cc2f9a1c2deb3a8f87a4c032bdf4a30de750cb5657582f58569ba166bfa8`  
		Last Modified: Wed, 15 Jan 2025 10:20:30 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8452084868fd89c612737f9f5e7dba6b8e34f92e251a0d54ca7efb1ff85a867d`  
		Last Modified: Wed, 15 Jan 2025 10:20:29 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b7e64ab71f5f86b3d836e9f516d8cd4bfaeba11f1903846278a9a02ed3c7c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570920449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa52a0eb5f79f7fbe1c417685d7720e09508920730b7617d35cced393b3d85cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8fbaa7907ee22571084279c601f14a265f51a5d724c32c5998a32a816fee1`  
		Last Modified: Thu, 09 Jan 2025 22:40:57 GMT  
		Size: 258.3 MB (258298411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c43a6c324bee7339a01235ae3f8add2d90fe7af6242a5baff29d13fdda43375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f1d8728f1c6c83d7d6e362f2a188a4c1798a757f6d2d265a4c9aeefa9918a6`

```dockerfile
```

-	Layers:
	-	`sha256:3ef50a7c55f348deb0ca7fbb92416cbf3dba64a6c873d5e6f36841c131b898d4`  
		Last Modified: Thu, 09 Jan 2025 22:40:51 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beaa953ff4cf7058098ec1d47f065d3f98b7409d9348fdbbddee897bcf48efc3`  
		Last Modified: Thu, 09 Jan 2025 22:40:50 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c17640850a0134370e2362bf3b7f6ab71f51d41886631847c98bd5360880f6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538184584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf739b3ee6543078b71a4bc2af3bae848066814306dc1b8057a587188caa49a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d0c381a5fdef1263d351e698c4afefeb15eebaa7c61c01a804b75362d039c4`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 16.1 MB (16061977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411024e8ae7dadedef448d7486b9035f3faedd43c62d2f773ed5d8f87362be0`  
		Last Modified: Tue, 14 Jan 2025 03:18:01 GMT  
		Size: 56.0 MB (56027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84d528e2732f18fed0f874f321917023842dc0f688eba487bec08562c3d8257`  
		Last Modified: Tue, 14 Jan 2025 04:16:55 GMT  
		Size: 200.0 MB (199979639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1890215ad1b9e7b795b8c3bcfdfa6316e86672addf33781986c40986200b30b3`  
		Last Modified: Tue, 14 Jan 2025 05:22:51 GMT  
		Size: 211.4 MB (211439547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dc095e114c22f2ea16954569e0b3e7765be2d40adcdcb4d45f9f40cf79ab9d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925afed10c23ff4c08e6186896e33df867a7a335d40a7af668b88b57afd5974f`

```dockerfile
```

-	Layers:
	-	`sha256:5e768d69c73b3c337285285f38146e2bc44606db37942e086b9711d44782c464`  
		Last Modified: Tue, 14 Jan 2025 05:22:47 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376e21ec95e43ad873259ff922b786ef57ca85f59549c2c6f80037dc438c5e78`  
		Last Modified: Tue, 14 Jan 2025 05:22:45 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-slim`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84-slim` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-slim-bookworm`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-slim-bullseye`

```console
$ docker pull rust@sha256:249b2de69e9d46230a225a71cb6bc166bb121acf2d66a6a23e0541154982c0df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.84-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2b5612d7b9c4331afe31226f40ba0a93d0b4fc349613bd282fe24b9715588827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285135891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db4d4004f1e1ff5c8c9551e91a98e6f155d5ff00c2b07338bae2a07cbff3ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea54e8ff51c7c9836420c4c189bd6a92a86a6332b2a3060cc3c2723a971d0b2`  
		Last Modified: Tue, 14 Jan 2025 02:19:50 GMT  
		Size: 254.9 MB (254883226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9071d1169765fbe1a946e7d8bbe3c0e268d6936be6e583409abe80c66aa9c58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dfad0599bcb2789ec36960f9099a91ab54a88652d8732322a8435f369e0e70`

```dockerfile
```

-	Layers:
	-	`sha256:4ad821a5ac880981ec294fc435d2b2c5848d3ba8e664a0e75a6462c57d3db34a`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e7375df865f0e28c4d31d09cc67995b4f1f8cfce180e9a33689a2112549a63`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:de6279776a815580500fb609083c2fe02117485aafbea7ae03aadbb8a7176afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c11918617732fd8c3c49a3f81e21b4815ff2b57a74e651127956f808aa43a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc52732c036f97c2f7f57efb3ab6d3b390481ece5426c086be618f7944a27b53`  
		Last Modified: Tue, 14 Jan 2025 15:20:06 GMT  
		Size: 273.0 MB (272976225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e51a8477401fca0e43abaa887b84f40e08d5f30f1a980b525ceda02765cbb605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f82a5f3c6e2a39d9e7a7fb173aefd11ccf832dcc5c6f0606cc049549d5fc60e`

```dockerfile
```

-	Layers:
	-	`sha256:00ced8b920f88eaa1366c355470398754dfeb0653ac7a01525e62c80e3089f19`  
		Last Modified: Tue, 14 Jan 2025 15:20:00 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fc47c5382a1d1130089734018473e6152bb094a90e0dae788cd7475498dc21`  
		Last Modified: Tue, 14 Jan 2025 15:19:59 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5260ecf55f369662a15414ec3490df728a5a9755414ab642127a4a7958d5ddbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0ff0c34b7a526ead79d15589f4fc07f3ec64f3d04300a5d275208e2e6ae2a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f28991d37cc716e65fa31b32b0fadfe580f4a6c8fb373e8c17cff772becc8f`  
		Last Modified: Tue, 14 Jan 2025 11:46:07 GMT  
		Size: 313.8 MB (313801833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbdbed22362995bd837fcde74928fe4dec4352f3837df2b1a2c761592e0b992d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1a00040c42b0220bbe52afa8c18ee0595d5b1a0d0bd9d752c015601f68115`

```dockerfile
```

-	Layers:
	-	`sha256:92ccf2fa5de715523928957650c60ed97ba3b7ce6d7c3d8a705b364f2db8f37d`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40f83054b032a48a466def65ad7b6e6897eca06a5a69341b41a338c5b405cd1`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:65319b92e9b07d523850dc0e024c02d094460fc9061acaef0ec20f218bf97af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303174112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b1fe80f5100fd17367b5b11b0ca2877dd39015304816091c7710e3a4f3491`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a84d82f065bab8e92c2a584d90458a0108031daee4f6472d0761cb90d24a70`  
		Last Modified: Tue, 14 Jan 2025 02:38:03 GMT  
		Size: 272.0 MB (271995083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0ab56bb29ff52bd366bbc16f121e03e7f0976940ba70eb96d23eacdddbb9e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1830bdadf3b01511162f732ad1247b47cc02c8d7000895c2445f7a3d58a8000b`

```dockerfile
```

-	Layers:
	-	`sha256:bcc431f2d4567a9a6f678bf9b1b4039c259b1f7fca00cb8227397fd6869fccbe`  
		Last Modified: Tue, 14 Jan 2025 02:37:57 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af005555ed40dc6af87e07ec4f6b9f51ec5cb79c36ebb870a18f02cdcdb8eb51`  
		Last Modified: Tue, 14 Jan 2025 02:37:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84.0` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-alpine`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-alpine3.20`

```console
$ docker pull rust@sha256:8b2e66b58b7b5a0181019e2ac12d6b4c2e550b2e6889ecfc2a12d10f4579894a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:1a866b68d2adb80492e3e996f84999d692c20a34c3ca1a21d8bd2b448993a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298337931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7ee796e3d6fa94b33642d35bf166294523ccf3a26389f8228de309940821`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ff15df1191be1ba73e0551f9604556c59601352359b9ddcd56df3db87838e3`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 55.3 MB (55315358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cfb1a53cd02005ecbbef1bf5c7908122591c89f17c20073a82364a982bddf`  
		Last Modified: Thu, 09 Jan 2025 22:29:55 GMT  
		Size: 239.4 MB (239396313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:609a9e76a5909373fe3ed8f7b522150f67e80681ceb707ea9a5677692d239a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46a007e2e5a282e2ab6fe96bec9e3e15b65a8a803bd9c29e506a009e90910d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c6a5a2ada3ef89e80c205bc878b8be8f529a5f096b1dc60fd7a94db1b6442c`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd25cef9e4659903109b2c2b5cef038ae26f5cad4d5ca689fc8b7aaf77ca5fd`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8d98865f36d4249e0faa69209325e70adc561ac43355de0a1469cbb04b12479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300990769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d1fb945f7649689a77349b66020e055e8362f207aa387c94cb30a12d615de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b4f23fe7caefa44f7fedf6c6ad6331c9647daa81ec320381013cb4987762a`  
		Last Modified: Thu, 09 Jan 2025 05:56:18 GMT  
		Size: 53.0 MB (52951004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f078a134c6d3bfbf3e51f6cf7d7215b3b9a168bfc794609656888a9123c68f5`  
		Last Modified: Thu, 09 Jan 2025 22:46:24 GMT  
		Size: 243.9 MB (243948996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:8eb282a9a9f00e4c2eafa1071b34f2dae2b421ae503a972eb948197a6b0d89f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a939431982c0dbaf5b921fb551b6df6df396a5d3ad4341bdb440eb5c687fb9`

```dockerfile
```

-	Layers:
	-	`sha256:131c73a03f3ebbeb19acca7099852ab177e0165420ebbdfad542fa4fcae54f98`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083bff1fc4a6ac0159bd3b6bfb7e2529474fd78d774f9e70650e53a48ac7aaca`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-alpine3.21`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84.0-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-bookworm`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-bullseye`

```console
$ docker pull rust@sha256:eaa0847dbdd260f39213a70fe9016ab83c2f4f4a1148ed53e3447b131b42fe22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.84.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2fd89ac12ed4061cb5a73c7809aa788c6f6b126e1d654295bce5ac00d14dfa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516059596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef02c2c79b9b8cc8dc8bb0644931dccb3de60a205fd7951b6b41c6e3eff3d23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff86202e7c3afa44ea1524a6f7520668801c0913bb650d2d105f267afcdc35`  
		Last Modified: Tue, 14 Jan 2025 04:16:44 GMT  
		Size: 197.1 MB (197073993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69f21d4b6500dd2eb40bcff9c3d8c70e4cdcbf23ee32f669a2b231dfca18a7`  
		Last Modified: Tue, 14 Jan 2025 05:23:32 GMT  
		Size: 194.9 MB (194934543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ce3fa42f06b943caa59c9b80a065e42cc262a4633c82c416b335d62c68b870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e297baa62e0bb3b5a8eb2383a802b7efd5ef65911e6208865778cbdd8053fcc5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae86dc6fc207bf2ebdc0b702ecb77c987cbaeb4c0469429240f5a890f310daa`  
		Last Modified: Tue, 14 Jan 2025 05:23:29 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57bd9b7bcc0f4ca719b900dd7f0cd81e77842afa77b0396d199b838fa62f07c5`  
		Last Modified: Tue, 14 Jan 2025 05:23:28 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:871ce791ca420097d2b8e1571fe2b84be3eaaa86316bff514741c433e05d5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded8b95ced658873224c8659cfee475812a31a6cb020639ad1fbc8b484c679d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a2aea83640d58c933777151ebe00fe790d8b0869986ddef8f4b6657086f68c`  
		Last Modified: Wed, 15 Jan 2025 10:20:35 GMT  
		Size: 230.9 MB (230905635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4dac81db1f486e0d9fef1804f4140b13067f799718646f509ee347517ccf48c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700f82deebaf5c4590fd6ed7bd33c0a729a0145d786ba8a37b610b9d6a891745`

```dockerfile
```

-	Layers:
	-	`sha256:5c10cc2f9a1c2deb3a8f87a4c032bdf4a30de750cb5657582f58569ba166bfa8`  
		Last Modified: Wed, 15 Jan 2025 10:20:30 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8452084868fd89c612737f9f5e7dba6b8e34f92e251a0d54ca7efb1ff85a867d`  
		Last Modified: Wed, 15 Jan 2025 10:20:29 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b7e64ab71f5f86b3d836e9f516d8cd4bfaeba11f1903846278a9a02ed3c7c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570920449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa52a0eb5f79f7fbe1c417685d7720e09508920730b7617d35cced393b3d85cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8fbaa7907ee22571084279c601f14a265f51a5d724c32c5998a32a816fee1`  
		Last Modified: Thu, 09 Jan 2025 22:40:57 GMT  
		Size: 258.3 MB (258298411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c43a6c324bee7339a01235ae3f8add2d90fe7af6242a5baff29d13fdda43375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f1d8728f1c6c83d7d6e362f2a188a4c1798a757f6d2d265a4c9aeefa9918a6`

```dockerfile
```

-	Layers:
	-	`sha256:3ef50a7c55f348deb0ca7fbb92416cbf3dba64a6c873d5e6f36841c131b898d4`  
		Last Modified: Thu, 09 Jan 2025 22:40:51 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beaa953ff4cf7058098ec1d47f065d3f98b7409d9348fdbbddee897bcf48efc3`  
		Last Modified: Thu, 09 Jan 2025 22:40:50 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c17640850a0134370e2362bf3b7f6ab71f51d41886631847c98bd5360880f6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538184584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf739b3ee6543078b71a4bc2af3bae848066814306dc1b8057a587188caa49a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d0c381a5fdef1263d351e698c4afefeb15eebaa7c61c01a804b75362d039c4`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 16.1 MB (16061977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411024e8ae7dadedef448d7486b9035f3faedd43c62d2f773ed5d8f87362be0`  
		Last Modified: Tue, 14 Jan 2025 03:18:01 GMT  
		Size: 56.0 MB (56027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84d528e2732f18fed0f874f321917023842dc0f688eba487bec08562c3d8257`  
		Last Modified: Tue, 14 Jan 2025 04:16:55 GMT  
		Size: 200.0 MB (199979639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1890215ad1b9e7b795b8c3bcfdfa6316e86672addf33781986c40986200b30b3`  
		Last Modified: Tue, 14 Jan 2025 05:22:51 GMT  
		Size: 211.4 MB (211439547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dc095e114c22f2ea16954569e0b3e7765be2d40adcdcb4d45f9f40cf79ab9d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925afed10c23ff4c08e6186896e33df867a7a335d40a7af668b88b57afd5974f`

```dockerfile
```

-	Layers:
	-	`sha256:5e768d69c73b3c337285285f38146e2bc44606db37942e086b9711d44782c464`  
		Last Modified: Tue, 14 Jan 2025 05:22:47 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376e21ec95e43ad873259ff922b786ef57ca85f59549c2c6f80037dc438c5e78`  
		Last Modified: Tue, 14 Jan 2025 05:22:45 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-slim`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-slim-bookworm`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.84.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-slim-bullseye`

```console
$ docker pull rust@sha256:249b2de69e9d46230a225a71cb6bc166bb121acf2d66a6a23e0541154982c0df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.84.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2b5612d7b9c4331afe31226f40ba0a93d0b4fc349613bd282fe24b9715588827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285135891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db4d4004f1e1ff5c8c9551e91a98e6f155d5ff00c2b07338bae2a07cbff3ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea54e8ff51c7c9836420c4c189bd6a92a86a6332b2a3060cc3c2723a971d0b2`  
		Last Modified: Tue, 14 Jan 2025 02:19:50 GMT  
		Size: 254.9 MB (254883226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9071d1169765fbe1a946e7d8bbe3c0e268d6936be6e583409abe80c66aa9c58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dfad0599bcb2789ec36960f9099a91ab54a88652d8732322a8435f369e0e70`

```dockerfile
```

-	Layers:
	-	`sha256:4ad821a5ac880981ec294fc435d2b2c5848d3ba8e664a0e75a6462c57d3db34a`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e7375df865f0e28c4d31d09cc67995b4f1f8cfce180e9a33689a2112549a63`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:de6279776a815580500fb609083c2fe02117485aafbea7ae03aadbb8a7176afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c11918617732fd8c3c49a3f81e21b4815ff2b57a74e651127956f808aa43a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc52732c036f97c2f7f57efb3ab6d3b390481ece5426c086be618f7944a27b53`  
		Last Modified: Tue, 14 Jan 2025 15:20:06 GMT  
		Size: 273.0 MB (272976225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e51a8477401fca0e43abaa887b84f40e08d5f30f1a980b525ceda02765cbb605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f82a5f3c6e2a39d9e7a7fb173aefd11ccf832dcc5c6f0606cc049549d5fc60e`

```dockerfile
```

-	Layers:
	-	`sha256:00ced8b920f88eaa1366c355470398754dfeb0653ac7a01525e62c80e3089f19`  
		Last Modified: Tue, 14 Jan 2025 15:20:00 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fc47c5382a1d1130089734018473e6152bb094a90e0dae788cd7475498dc21`  
		Last Modified: Tue, 14 Jan 2025 15:19:59 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5260ecf55f369662a15414ec3490df728a5a9755414ab642127a4a7958d5ddbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0ff0c34b7a526ead79d15589f4fc07f3ec64f3d04300a5d275208e2e6ae2a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f28991d37cc716e65fa31b32b0fadfe580f4a6c8fb373e8c17cff772becc8f`  
		Last Modified: Tue, 14 Jan 2025 11:46:07 GMT  
		Size: 313.8 MB (313801833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbdbed22362995bd837fcde74928fe4dec4352f3837df2b1a2c761592e0b992d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1a00040c42b0220bbe52afa8c18ee0595d5b1a0d0bd9d752c015601f68115`

```dockerfile
```

-	Layers:
	-	`sha256:92ccf2fa5de715523928957650c60ed97ba3b7ce6d7c3d8a705b364f2db8f37d`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40f83054b032a48a466def65ad7b6e6897eca06a5a69341b41a338c5b405cd1`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:65319b92e9b07d523850dc0e024c02d094460fc9061acaef0ec20f218bf97af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303174112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b1fe80f5100fd17367b5b11b0ca2877dd39015304816091c7710e3a4f3491`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a84d82f065bab8e92c2a584d90458a0108031daee4f6472d0761cb90d24a70`  
		Last Modified: Tue, 14 Jan 2025 02:38:03 GMT  
		Size: 272.0 MB (271995083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0ab56bb29ff52bd366bbc16f121e03e7f0976940ba70eb96d23eacdddbb9e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1830bdadf3b01511162f732ad1247b47cc02c8d7000895c2445f7a3d58a8000b`

```dockerfile
```

-	Layers:
	-	`sha256:bcc431f2d4567a9a6f678bf9b1b4039c259b1f7fca00cb8227397fd6869fccbe`  
		Last Modified: Tue, 14 Jan 2025 02:37:57 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af005555ed40dc6af87e07ec4f6b9f51ec5cb79c36ebb870a18f02cdcdb8eb51`  
		Last Modified: Tue, 14 Jan 2025 02:37:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:8b2e66b58b7b5a0181019e2ac12d6b4c2e550b2e6889ecfc2a12d10f4579894a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:1a866b68d2adb80492e3e996f84999d692c20a34c3ca1a21d8bd2b448993a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298337931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7ee796e3d6fa94b33642d35bf166294523ccf3a26389f8228de309940821`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ff15df1191be1ba73e0551f9604556c59601352359b9ddcd56df3db87838e3`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 55.3 MB (55315358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cfb1a53cd02005ecbbef1bf5c7908122591c89f17c20073a82364a982bddf`  
		Last Modified: Thu, 09 Jan 2025 22:29:55 GMT  
		Size: 239.4 MB (239396313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:609a9e76a5909373fe3ed8f7b522150f67e80681ceb707ea9a5677692d239a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46a007e2e5a282e2ab6fe96bec9e3e15b65a8a803bd9c29e506a009e90910d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c6a5a2ada3ef89e80c205bc878b8be8f529a5f096b1dc60fd7a94db1b6442c`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd25cef9e4659903109b2c2b5cef038ae26f5cad4d5ca689fc8b7aaf77ca5fd`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8d98865f36d4249e0faa69209325e70adc561ac43355de0a1469cbb04b12479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300990769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d1fb945f7649689a77349b66020e055e8362f207aa387c94cb30a12d615de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b4f23fe7caefa44f7fedf6c6ad6331c9647daa81ec320381013cb4987762a`  
		Last Modified: Thu, 09 Jan 2025 05:56:18 GMT  
		Size: 53.0 MB (52951004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f078a134c6d3bfbf3e51f6cf7d7215b3b9a168bfc794609656888a9123c68f5`  
		Last Modified: Thu, 09 Jan 2025 22:46:24 GMT  
		Size: 243.9 MB (243948996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:8eb282a9a9f00e4c2eafa1071b34f2dae2b421ae503a972eb948197a6b0d89f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a939431982c0dbaf5b921fb551b6df6df396a5d3ad4341bdb440eb5c687fb9`

```dockerfile
```

-	Layers:
	-	`sha256:131c73a03f3ebbeb19acca7099852ab177e0165420ebbdfad542fa4fcae54f98`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083bff1fc4a6ac0159bd3b6bfb7e2529474fd78d774f9e70650e53a48ac7aaca`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:0cfc78e96e5314e8279cec9faf3067744764ff58cc6a87a3f9c89217f8c4aa16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dab5479b8785807a1b4530386c9028e26744218c72c175b1a066164a96c74c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a300ac5faa8ac048c0371b415927330515bba9d6e4693266af235e70a366b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b163768f3d081b3ac07f6fe8f8c69646962c08618d7de8bb87cb35fbef03e70f`  
		Last Modified: Thu, 09 Jan 2025 23:11:01 GMT  
		Size: 243.9 MB (243949010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:94511259b2d809e8e779bdd057fc78710ab2682f27b88277f82d95754c8147e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b78015e466aa68564fd93b0a69a13a776e7f06ad35c96fa1a7be68fc62b7f16`

```dockerfile
```

-	Layers:
	-	`sha256:ca775ed51fb778dcfc4a898abd32149b7f19e558867063c6899aeefcf2019314`  
		Last Modified: Thu, 09 Jan 2025 23:10:56 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bf96ca82a2d79eb75f4d242c1cf1d3f760c27f716a9d932b94bade83f9bae7`  
		Last Modified: Thu, 09 Jan 2025 23:10:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:bookworm` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:eaa0847dbdd260f39213a70fe9016ab83c2f4f4a1148ed53e3447b131b42fe22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2fd89ac12ed4061cb5a73c7809aa788c6f6b126e1d654295bce5ac00d14dfa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516059596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef02c2c79b9b8cc8dc8bb0644931dccb3de60a205fd7951b6b41c6e3eff3d23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff86202e7c3afa44ea1524a6f7520668801c0913bb650d2d105f267afcdc35`  
		Last Modified: Tue, 14 Jan 2025 04:16:44 GMT  
		Size: 197.1 MB (197073993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69f21d4b6500dd2eb40bcff9c3d8c70e4cdcbf23ee32f669a2b231dfca18a7`  
		Last Modified: Tue, 14 Jan 2025 05:23:32 GMT  
		Size: 194.9 MB (194934543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ce3fa42f06b943caa59c9b80a065e42cc262a4633c82c416b335d62c68b870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e297baa62e0bb3b5a8eb2383a802b7efd5ef65911e6208865778cbdd8053fcc5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae86dc6fc207bf2ebdc0b702ecb77c987cbaeb4c0469429240f5a890f310daa`  
		Last Modified: Tue, 14 Jan 2025 05:23:29 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57bd9b7bcc0f4ca719b900dd7f0cd81e77842afa77b0396d199b838fa62f07c5`  
		Last Modified: Tue, 14 Jan 2025 05:23:28 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:871ce791ca420097d2b8e1571fe2b84be3eaaa86316bff514741c433e05d5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded8b95ced658873224c8659cfee475812a31a6cb020639ad1fbc8b484c679d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a2aea83640d58c933777151ebe00fe790d8b0869986ddef8f4b6657086f68c`  
		Last Modified: Wed, 15 Jan 2025 10:20:35 GMT  
		Size: 230.9 MB (230905635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4dac81db1f486e0d9fef1804f4140b13067f799718646f509ee347517ccf48c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700f82deebaf5c4590fd6ed7bd33c0a729a0145d786ba8a37b610b9d6a891745`

```dockerfile
```

-	Layers:
	-	`sha256:5c10cc2f9a1c2deb3a8f87a4c032bdf4a30de750cb5657582f58569ba166bfa8`  
		Last Modified: Wed, 15 Jan 2025 10:20:30 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8452084868fd89c612737f9f5e7dba6b8e34f92e251a0d54ca7efb1ff85a867d`  
		Last Modified: Wed, 15 Jan 2025 10:20:29 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b7e64ab71f5f86b3d836e9f516d8cd4bfaeba11f1903846278a9a02ed3c7c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570920449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa52a0eb5f79f7fbe1c417685d7720e09508920730b7617d35cced393b3d85cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8fbaa7907ee22571084279c601f14a265f51a5d724c32c5998a32a816fee1`  
		Last Modified: Thu, 09 Jan 2025 22:40:57 GMT  
		Size: 258.3 MB (258298411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c43a6c324bee7339a01235ae3f8add2d90fe7af6242a5baff29d13fdda43375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f1d8728f1c6c83d7d6e362f2a188a4c1798a757f6d2d265a4c9aeefa9918a6`

```dockerfile
```

-	Layers:
	-	`sha256:3ef50a7c55f348deb0ca7fbb92416cbf3dba64a6c873d5e6f36841c131b898d4`  
		Last Modified: Thu, 09 Jan 2025 22:40:51 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beaa953ff4cf7058098ec1d47f065d3f98b7409d9348fdbbddee897bcf48efc3`  
		Last Modified: Thu, 09 Jan 2025 22:40:50 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:c17640850a0134370e2362bf3b7f6ab71f51d41886631847c98bd5360880f6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538184584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf739b3ee6543078b71a4bc2af3bae848066814306dc1b8057a587188caa49a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d0c381a5fdef1263d351e698c4afefeb15eebaa7c61c01a804b75362d039c4`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 16.1 MB (16061977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411024e8ae7dadedef448d7486b9035f3faedd43c62d2f773ed5d8f87362be0`  
		Last Modified: Tue, 14 Jan 2025 03:18:01 GMT  
		Size: 56.0 MB (56027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84d528e2732f18fed0f874f321917023842dc0f688eba487bec08562c3d8257`  
		Last Modified: Tue, 14 Jan 2025 04:16:55 GMT  
		Size: 200.0 MB (199979639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1890215ad1b9e7b795b8c3bcfdfa6316e86672addf33781986c40986200b30b3`  
		Last Modified: Tue, 14 Jan 2025 05:22:51 GMT  
		Size: 211.4 MB (211439547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dc095e114c22f2ea16954569e0b3e7765be2d40adcdcb4d45f9f40cf79ab9d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925afed10c23ff4c08e6186896e33df867a7a335d40a7af668b88b57afd5974f`

```dockerfile
```

-	Layers:
	-	`sha256:5e768d69c73b3c337285285f38146e2bc44606db37942e086b9711d44782c464`  
		Last Modified: Tue, 14 Jan 2025 05:22:47 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376e21ec95e43ad873259ff922b786ef57ca85f59549c2c6f80037dc438c5e78`  
		Last Modified: Tue, 14 Jan 2025 05:22:45 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:1857878204898d076c8b2d21380736d812f630a9c8a269f4f39ccd741ffe6efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:latest` - linux; amd64

```console
$ docker pull rust@sha256:12b68bb84516779d910706fb80f1705777459c1e5f6c7c0118c2fb4256d9ec3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543197998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daff99931169078c58538c42c9a375a4db5113374ecd5a0750ee82ff487d9a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf93b646d6b4d6612a25d50599f4d8e3c7785f83c6ba085219f9d4d334e8aa3`  
		Last Modified: Tue, 14 Jan 2025 04:16:48 GMT  
		Size: 211.3 MB (211326155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c58ae477c23b828871f755fa3f521704ef9e9491ed0c8adecbee4f102fb88a`  
		Last Modified: Tue, 14 Jan 2025 05:24:04 GMT  
		Size: 194.9 MB (194934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:be97e18bd3d704d4ae963f368d8737ed3bea0e46d85667e08848b03a6d174594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da79d61bd9de99982a542c73c846946b35b30fe95a3a189c56364d446695e6`

```dockerfile
```

-	Layers:
	-	`sha256:f977e2a8509c4f54a2ec617f55fce368980de47081b720129f289e12e6b385da`  
		Last Modified: Tue, 14 Jan 2025 05:24:00 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b91103792cfcdedd8b6fdb41dcaa084537a69bc2d01c9eea79263816e23b9a`  
		Last Modified: Tue, 14 Jan 2025 05:23:59 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:d345e8f05b89dbf2c68f67f5653b36dc172d3501ff2298a097fd411741e2823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (531970431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b5d84c2826f2c0a27e8d2429c29425f0c011e590386a5d9b05eff51bccc62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59b52470b6df1933ab45c306d8bd9231dfebc0257817ef86c7fd89763c6bab`  
		Last Modified: Wed, 15 Jan 2025 10:22:40 GMT  
		Size: 230.9 MB (230905556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a9df17f7e5f9215bbcbbb0db82fdbacc9a8cd43aebf933af0cd6ff467df9860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ffefdd22c28013ce571f2ef071507c6f8c2b621088d1489748f94effed0b5`

```dockerfile
```

-	Layers:
	-	`sha256:73acd30ad2d4800e44b522f1a0169fff1b72808506101beb0b3d13747ed588bd`  
		Last Modified: Wed, 15 Jan 2025 10:22:35 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0525d1a808268dea273a3af70baaf3ce5e546a14239e3615a22dc98870591ac`  
		Last Modified: Wed, 15 Jan 2025 10:22:34 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:271923eca4ca8fe547a0d8aa5136259bbc248db3632633662bc1a10406bba25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597063444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47031fd312d1adf727d3d5af9a8a075a9ecf13c974eda12058c0acbaaf543844`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9866ea7d4e8ecd3c5afc5755c250a066147e33162dc459ec0a88abf7543b50c`  
		Last Modified: Thu, 09 Jan 2025 22:43:56 GMT  
		Size: 258.3 MB (258298342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:9007cd4fe93494965307da20b93153939926bfd60c06c4d144946544392d15ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c54602640157e76e8749fea436f3efa48c67a9ed35d1ba5c670ae98be35ee90`

```dockerfile
```

-	Layers:
	-	`sha256:16ce0ac93cbbc8fea6caa2c245c4e32ec67a800d169aa4776c537d223a333979`  
		Last Modified: Thu, 09 Jan 2025 22:43:52 GMT  
		Size: 15.5 MB (15502741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c522f221077b09730b193175a4a49b99c8f0ad40330f47ca92a254d77f06c350`  
		Last Modified: Thu, 09 Jan 2025 22:43:51 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:d9039cc93853df2e1c70225f8c57bbbb6942a96214dfb72ce311f520f57da1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562270956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080963ccb807f633a92e3daf3c6f21d8673aab16931a4c32cc1ef1924d46db09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca7246923216a4e316eadc3f970df39358c7542d23510efc12fe89116a5fe2`  
		Last Modified: Tue, 14 Jan 2025 04:17:01 GMT  
		Size: 210.2 MB (210241848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d3e21837a3d7d4f5ee6325dd96973774771699c871cfd7297f064dc73a116`  
		Last Modified: Tue, 14 Jan 2025 05:22:46 GMT  
		Size: 211.4 MB (211439504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:e35ca3b03df5d91abe4e2df0ddce97395ff603abb90266651c8f72f8aabee92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7014b2e964c7af568d87951dc67840b708ae6c6db40971f72217cc5bfccab2`

```dockerfile
```

-	Layers:
	-	`sha256:5f430c093ac7608e8aa9c03b3f27f22e6d7c67f8c7be51943f79441fc1dc84fb`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5070015b2683724208dd7461d88f2a483616f473c64412d44fbafdce6c5d0`  
		Last Modified: Tue, 14 Jan 2025 05:22:41 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:195e94e96e1d5b845eca821735f054e284dcf0cfb573306aeee042259cfe68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617088507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5f205ae0ceedeb1dea22b6dc5456bf7119dedfbc80b6fce1abd1942fc0c24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b998e1991a76def5190c0e6172bdf14895d776134e8a9db4642a777b7fdde`  
		Last Modified: Tue, 14 Jan 2025 19:19:40 GMT  
		Size: 254.8 MB (254849137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:7c0fe47e0a4ec595f328f1df0b84cd0228b5db51498d043161db1ce06723d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f501c912c22ad4636e237f8b006ba65b0c378404aa7e4b9ec65542b4fed32`

```dockerfile
```

-	Layers:
	-	`sha256:f0faa4c7e2729f483a9221205983b95d76917d01a9b9ca0fccbd43646f49ea25`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc41a3a08f22a31972d9b14ddefebea63551ddd728e3c22c0d59f506b917a594`  
		Last Modified: Tue, 14 Jan 2025 19:19:31 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:b40298474812e48edaee2bbb6fc8b17b61ca01e0feae7bbd0417fd3e0131b561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599996590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472cc92cea2ff82d6f2767b41f69c6747e7f1869b839f7732e443d56be3cc99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f487c890334cba7d6bb843f534084444d859c1a287b244890381657408f3e61`  
		Last Modified: Tue, 14 Jan 2025 18:41:03 GMT  
		Size: 281.9 MB (281949990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:245311777c0e9cf0323b7f0022d896cfff1170532c1942097af6ffb3ccf1ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df031880850b871bdb265b0f76fdc887bc51517666c87c88057cb01ed11cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cf31327f973c2330c05cb07d15ef46fe5621f5f165b2d1da647e89941f6b5d77`  
		Last Modified: Tue, 14 Jan 2025 18:40:59 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eff5be952ca64200c2f8fd505ad34404ba881f2b4fbe1c7707c874999c66a5`  
		Last Modified: Tue, 14 Jan 2025 18:40:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:0ec205a9abb049604cb085f2fdf7630f1a31dad1f7ad4986154a56501fb7ca77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:ee30f3ef0d91379f751ebb8a9431c160d3b2ed9f49e0a291b6447393fd0bbbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293912669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923e09865051b614c45d90a5726475bd8a6ebb3c54562654fcd31a67544480f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4e536813410a73cde92b76c8d36e395c728c71c0e71fdb868f74072cf3d9`  
		Last Modified: Tue, 14 Jan 2025 02:19:49 GMT  
		Size: 265.7 MB (265700252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3468ad1173f23dce731257730c90f2e17c5d590d9eb08d84aeec00d2c7ecabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12bfd6a457072a3be6a5eb80b026c2a456a608e7193c464a042138597755c0`

```dockerfile
```

-	Layers:
	-	`sha256:7ae10fdd3382bd702b459ffc12aa8c9a8ecfc755af460f6e88fa67e8e65bbd38`  
		Last Modified: Tue, 14 Jan 2025 02:19:44 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2902b552c56d75ebbaea1ed4d254165697a2cad6708bf55092f7da20c4c4a531`  
		Last Modified: Tue, 14 Jan 2025 02:19:43 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:dcf97e6078e640618f5ed78933dd1797adcf0d6d15473d26cf0132b170a68c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302663541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd263de66415e15b1ac816afa7a20e75f07d2d711746c51801b3789372f765b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799754163eac13f1a51e44c94b12425116a5a4760acfacf5e16483fae18e945`  
		Last Modified: Tue, 14 Jan 2025 15:22:07 GMT  
		Size: 278.7 MB (278748941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:28e56267526d338aa26d0976bcf13df079b1c87e100f01074a1c108a65ec01d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e17a1bf7df1621b84a0cb9cf9e927773b64475e63c9ef7e5e44488eb680f4`

```dockerfile
```

-	Layers:
	-	`sha256:1b1eee558820267df2a24092e1cc10f2fe30b93967243106f74b295d2a7dcd5e`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64034917e9a404f5c87d8fb77eab46ed77a035c54f09bda5c4e542f006b2c3`  
		Last Modified: Tue, 14 Jan 2025 15:21:59 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ab25608b48ef385d1b7250e25189725364a20d1d41439b11bbf52a6b158c673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f7d07d218ef3a43528061a1a3b2075a299c2fded04cd8bc2252fc484f3191e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3091c27d724889b14b97a8397534e2888af68e9c11fb98d6fe7c0738f984a7`  
		Last Modified: Tue, 14 Jan 2025 11:47:33 GMT  
		Size: 324.2 MB (324153255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:13950c12dd33f5039f3bedd475b89d4452072f65b2720349b932e3b8f382e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27eb9f1675f6ee2d40729e4e26d226f12ba08aaf01e38cd5ec8f5818fda161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a97df7ca6d89a5a3d24196cb128dc592658b1f338c41ae21abe3e07679036a`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1d636c18871b55540e21cee9403bd366b50f91680bbd385b443ea136c17621`  
		Last Modified: Tue, 14 Jan 2025 11:47:25 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6105f1834d991da6985b8f4bbd234a57ff156fcaf41e97aeec1eae35c082276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308222374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d041b883c64a2b0aa302549543fa51d5d6e0ae0d1a1bcee636a51fb1a7727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa5de1a6ef472f2c59cbca3cc2dd04ca9bb566b5985cb10ce693a9bb11706`  
		Last Modified: Tue, 14 Jan 2025 02:37:55 GMT  
		Size: 279.0 MB (279034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6513c11c85b3d8537c1872ddf9cb315f916a42cf8227d8f058d0d03360cf6d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c06e33928ea4ccea2020350d2fded131d9c3ad5ee411e7cfa3847319a5ac0`

```dockerfile
```

-	Layers:
	-	`sha256:b478a4277d51ea024749623b6a3fcafaf773ea37bce39b92f81e37baa5066e69`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f73eadc50bad878adb766864d24c4188b15dbe632dd8802125816d6a14edf1`  
		Last Modified: Tue, 14 Jan 2025 02:37:48 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:06ab83c1731186e1fa28cff2039c32091dc109dcfd49a733970357e7ad4bc936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355653432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a036213195bff712ac85fbfe4151baa4c4722cadb92f426cb36eaf0aed8adadf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5323b2fc71e139b890833ffb127f6ed00033780c99eaa3f1f6d4ad7a10bbe`  
		Last Modified: Tue, 14 Jan 2025 08:39:07 GMT  
		Size: 323.6 MB (323608585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:300aaea78b7a9c1a608dd2246c8f3cf149b42b26df9a7e2ddd85a9e49d4a78b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6cf18914131dc314f9c9c4f2c6cbfd218a9243055b5df2434ae2b0aa968a3`

```dockerfile
```

-	Layers:
	-	`sha256:e8478a79b564e0e388960b74de8fa68d6bcfff682fd8b8b6bee42daa4d1daca4`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd400081443133fe10eff1ffbd3cd18d420fdb89e841269bc408a84e7c59a4f`  
		Last Modified: Tue, 14 Jan 2025 08:38:59 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:94b8f5e646b5d20d065087e2720e1558111cf694942a30c67d6cbdb2835f7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358924811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bca79ece0475fc559078171a2b45dee9bc9d8c39f80583745316bbfa46d861`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00e20ef5f06b610c8c7b0f1d9d619dd77f6a0bea7938243db4f1823dee104c`  
		Last Modified: Tue, 14 Jan 2025 08:06:21 GMT  
		Size: 332.1 MB (332066073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25a08c31200849ef7e7485847964438879000eefe6b87a248b7667637095f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cce28db024a7ce69fee177c0d778fcf977c14aee70f0e337d395a30731e93`

```dockerfile
```

-	Layers:
	-	`sha256:609ecf7910dabf63f9144cc261cd67be64344bec15ed4e5513b6cdc93e23f0ae`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b1cc1718719d765df22aff3eee249ee755a55f89fd3a6b82fad7414c8f6bdd`  
		Last Modified: Tue, 14 Jan 2025 08:06:16 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:249b2de69e9d46230a225a71cb6bc166bb121acf2d66a6a23e0541154982c0df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2b5612d7b9c4331afe31226f40ba0a93d0b4fc349613bd282fe24b9715588827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285135891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db4d4004f1e1ff5c8c9551e91a98e6f155d5ff00c2b07338bae2a07cbff3ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea54e8ff51c7c9836420c4c189bd6a92a86a6332b2a3060cc3c2723a971d0b2`  
		Last Modified: Tue, 14 Jan 2025 02:19:50 GMT  
		Size: 254.9 MB (254883226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9071d1169765fbe1a946e7d8bbe3c0e268d6936be6e583409abe80c66aa9c58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dfad0599bcb2789ec36960f9099a91ab54a88652d8732322a8435f369e0e70`

```dockerfile
```

-	Layers:
	-	`sha256:4ad821a5ac880981ec294fc435d2b2c5848d3ba8e664a0e75a6462c57d3db34a`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e7375df865f0e28c4d31d09cc67995b4f1f8cfce180e9a33689a2112549a63`  
		Last Modified: Tue, 14 Jan 2025 02:19:45 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:de6279776a815580500fb609083c2fe02117485aafbea7ae03aadbb8a7176afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c11918617732fd8c3c49a3f81e21b4815ff2b57a74e651127956f808aa43a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc52732c036f97c2f7f57efb3ab6d3b390481ece5426c086be618f7944a27b53`  
		Last Modified: Tue, 14 Jan 2025 15:20:06 GMT  
		Size: 273.0 MB (272976225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e51a8477401fca0e43abaa887b84f40e08d5f30f1a980b525ceda02765cbb605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f82a5f3c6e2a39d9e7a7fb173aefd11ccf832dcc5c6f0606cc049549d5fc60e`

```dockerfile
```

-	Layers:
	-	`sha256:00ced8b920f88eaa1366c355470398754dfeb0653ac7a01525e62c80e3089f19`  
		Last Modified: Tue, 14 Jan 2025 15:20:00 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fc47c5382a1d1130089734018473e6152bb094a90e0dae788cd7475498dc21`  
		Last Modified: Tue, 14 Jan 2025 15:19:59 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5260ecf55f369662a15414ec3490df728a5a9755414ab642127a4a7958d5ddbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0ff0c34b7a526ead79d15589f4fc07f3ec64f3d04300a5d275208e2e6ae2a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f28991d37cc716e65fa31b32b0fadfe580f4a6c8fb373e8c17cff772becc8f`  
		Last Modified: Tue, 14 Jan 2025 11:46:07 GMT  
		Size: 313.8 MB (313801833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbdbed22362995bd837fcde74928fe4dec4352f3837df2b1a2c761592e0b992d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1a00040c42b0220bbe52afa8c18ee0595d5b1a0d0bd9d752c015601f68115`

```dockerfile
```

-	Layers:
	-	`sha256:92ccf2fa5de715523928957650c60ed97ba3b7ce6d7c3d8a705b364f2db8f37d`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40f83054b032a48a466def65ad7b6e6897eca06a5a69341b41a338c5b405cd1`  
		Last Modified: Tue, 14 Jan 2025 11:45:59 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:65319b92e9b07d523850dc0e024c02d094460fc9061acaef0ec20f218bf97af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303174112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b1fe80f5100fd17367b5b11b0ca2877dd39015304816091c7710e3a4f3491`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Jan 2025 15:52:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a84d82f065bab8e92c2a584d90458a0108031daee4f6472d0761cb90d24a70`  
		Last Modified: Tue, 14 Jan 2025 02:38:03 GMT  
		Size: 272.0 MB (271995083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0ab56bb29ff52bd366bbc16f121e03e7f0976940ba70eb96d23eacdddbb9e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1830bdadf3b01511162f732ad1247b47cc02c8d7000895c2445f7a3d58a8000b`

```dockerfile
```

-	Layers:
	-	`sha256:bcc431f2d4567a9a6f678bf9b1b4039c259b1f7fca00cb8227397fd6869fccbe`  
		Last Modified: Tue, 14 Jan 2025 02:37:57 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af005555ed40dc6af87e07ec4f6b9f51ec5cb79c36ebb870a18f02cdcdb8eb51`  
		Last Modified: Tue, 14 Jan 2025 02:37:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
