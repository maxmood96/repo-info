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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:b2d330ca0e4ef66798a61e4deb333a0b38d1ff89e6cd7e24a72210ad791c9e71
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
$ docker pull rust@sha256:0c8ef21098b2fe26dbe27245b880cff1783c61797ce7c3be4439e8821e6d03bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20324960d5bd49cef0397aae01c4d1dfe13dfdfa0290058f0422fe00be7ce468`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ceb953441df71e06cff2748ecdd8e6f1a88d8237bb1c52a18a2bd69529dcd3`  
		Last Modified: Thu, 09 Jan 2025 22:44:27 GMT  
		Size: 230.9 MB (230905569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2c9be0c39a11358bdd1cd407b54c6bf22059ba2e1addb3c42a0cbf21e50bfdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feed8f035ac9f426deb877b63cc7ffdc57c2c7744ed2d2c38b059e2a00a45d7`

```dockerfile
```

-	Layers:
	-	`sha256:43d3ea4f99e4b87a2cf917ae97d374a9bfe8f8f12c72b01e4123174faae8c8a2`  
		Last Modified: Thu, 09 Jan 2025 22:44:21 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb789d97c20fc3b57ceed945e52333794c709058117190929cf75bb065a5fbf`  
		Last Modified: Thu, 09 Jan 2025 22:44:20 GMT  
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
$ docker pull rust@sha256:89e23177021d16bf959bf2c591f75bc5284a503bc35256e41f514dd58a4327f4
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:89e23177021d16bf959bf2c591f75bc5284a503bc35256e41f514dd58a4327f4
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:7eebe9862287fec6f2292acb17737062307083055ef75e2258bf90659d7a055f
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
$ docker pull rust@sha256:b353124551697953231aae2dd92f3a5eda8c03a3e1b048072a9d61a03a9c9f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7babd70875fa12e2f93e1bc32d8ca9c726a8c14f071b223e56f845152c19d98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055223b0c039c674a4a693ec584cd007a130abd127cde1a0be4c49fe58130afc`  
		Last Modified: Thu, 09 Jan 2025 22:46:19 GMT  
		Size: 273.0 MB (272976369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6388b285ba27595142573262570e5ca18d895aae7d60f19837c1cba43b11a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9571fdce4d22641e3a35297c07093ee0cc97650ffbe26d24713306c5468ce`

```dockerfile
```

-	Layers:
	-	`sha256:0716fc41687ba3e147ca7206a8fd91f3c5f17c5430b8e653b156fdfb46dbc53e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8c507f8775c0076fe162fc578a130d6262b7014621a0b92ae31b8cff2c1a0e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:6838e9cb67fe860cf4ad579d801f09eb72b899df748b91bb3e1ba947cdb5c979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7fe2a30e41bb1d4d966f5b6a0cbdc31a46b84d9a227a358e95e693891bda3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e967efca0462a2558586cfab92f23d28881b414fe0c7b86e1c99f3e4bf0c49`  
		Last Modified: Thu, 09 Jan 2025 22:42:19 GMT  
		Size: 313.8 MB (313802017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80d00667a000d9ae64cb0812d0ef0ccab2d02238b8a9564135e5bec0b673927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb9f7bb392b3cb19a42b4cba5e1b19c3c42f45d36d1408be47bfba5a8143f63`

```dockerfile
```

-	Layers:
	-	`sha256:60af30b4a5d8fb3668a08606db9b1bb98c6fbedb83c115d098a33ab49a7c9bef`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4fda87e5ad2ebdb737f190a34737c9aec3b0dc4c82f6a52c808a64aab05552`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-bullseye`

```console
$ docker pull rust@sha256:b2d330ca0e4ef66798a61e4deb333a0b38d1ff89e6cd7e24a72210ad791c9e71
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
$ docker pull rust@sha256:0c8ef21098b2fe26dbe27245b880cff1783c61797ce7c3be4439e8821e6d03bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20324960d5bd49cef0397aae01c4d1dfe13dfdfa0290058f0422fe00be7ce468`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ceb953441df71e06cff2748ecdd8e6f1a88d8237bb1c52a18a2bd69529dcd3`  
		Last Modified: Thu, 09 Jan 2025 22:44:27 GMT  
		Size: 230.9 MB (230905569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2c9be0c39a11358bdd1cd407b54c6bf22059ba2e1addb3c42a0cbf21e50bfdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feed8f035ac9f426deb877b63cc7ffdc57c2c7744ed2d2c38b059e2a00a45d7`

```dockerfile
```

-	Layers:
	-	`sha256:43d3ea4f99e4b87a2cf917ae97d374a9bfe8f8f12c72b01e4123174faae8c8a2`  
		Last Modified: Thu, 09 Jan 2025 22:44:21 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb789d97c20fc3b57ceed945e52333794c709058117190929cf75bb065a5fbf`  
		Last Modified: Thu, 09 Jan 2025 22:44:20 GMT  
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
$ docker pull rust@sha256:89e23177021d16bf959bf2c591f75bc5284a503bc35256e41f514dd58a4327f4
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:89e23177021d16bf959bf2c591f75bc5284a503bc35256e41f514dd58a4327f4
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:7eebe9862287fec6f2292acb17737062307083055ef75e2258bf90659d7a055f
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
$ docker pull rust@sha256:b353124551697953231aae2dd92f3a5eda8c03a3e1b048072a9d61a03a9c9f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7babd70875fa12e2f93e1bc32d8ca9c726a8c14f071b223e56f845152c19d98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055223b0c039c674a4a693ec584cd007a130abd127cde1a0be4c49fe58130afc`  
		Last Modified: Thu, 09 Jan 2025 22:46:19 GMT  
		Size: 273.0 MB (272976369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6388b285ba27595142573262570e5ca18d895aae7d60f19837c1cba43b11a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9571fdce4d22641e3a35297c07093ee0cc97650ffbe26d24713306c5468ce`

```dockerfile
```

-	Layers:
	-	`sha256:0716fc41687ba3e147ca7206a8fd91f3c5f17c5430b8e653b156fdfb46dbc53e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8c507f8775c0076fe162fc578a130d6262b7014621a0b92ae31b8cff2c1a0e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:6838e9cb67fe860cf4ad579d801f09eb72b899df748b91bb3e1ba947cdb5c979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7fe2a30e41bb1d4d966f5b6a0cbdc31a46b84d9a227a358e95e693891bda3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e967efca0462a2558586cfab92f23d28881b414fe0c7b86e1c99f3e4bf0c49`  
		Last Modified: Thu, 09 Jan 2025 22:42:19 GMT  
		Size: 313.8 MB (313802017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80d00667a000d9ae64cb0812d0ef0ccab2d02238b8a9564135e5bec0b673927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb9f7bb392b3cb19a42b4cba5e1b19c3c42f45d36d1408be47bfba5a8143f63`

```dockerfile
```

-	Layers:
	-	`sha256:60af30b4a5d8fb3668a08606db9b1bb98c6fbedb83c115d098a33ab49a7c9bef`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4fda87e5ad2ebdb737f190a34737c9aec3b0dc4c82f6a52c808a64aab05552`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.0-bullseye`

```console
$ docker pull rust@sha256:b2d330ca0e4ef66798a61e4deb333a0b38d1ff89e6cd7e24a72210ad791c9e71
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
$ docker pull rust@sha256:0c8ef21098b2fe26dbe27245b880cff1783c61797ce7c3be4439e8821e6d03bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20324960d5bd49cef0397aae01c4d1dfe13dfdfa0290058f0422fe00be7ce468`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ceb953441df71e06cff2748ecdd8e6f1a88d8237bb1c52a18a2bd69529dcd3`  
		Last Modified: Thu, 09 Jan 2025 22:44:27 GMT  
		Size: 230.9 MB (230905569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2c9be0c39a11358bdd1cd407b54c6bf22059ba2e1addb3c42a0cbf21e50bfdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feed8f035ac9f426deb877b63cc7ffdc57c2c7744ed2d2c38b059e2a00a45d7`

```dockerfile
```

-	Layers:
	-	`sha256:43d3ea4f99e4b87a2cf917ae97d374a9bfe8f8f12c72b01e4123174faae8c8a2`  
		Last Modified: Thu, 09 Jan 2025 22:44:21 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb789d97c20fc3b57ceed945e52333794c709058117190929cf75bb065a5fbf`  
		Last Modified: Thu, 09 Jan 2025 22:44:20 GMT  
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
$ docker pull rust@sha256:89e23177021d16bf959bf2c591f75bc5284a503bc35256e41f514dd58a4327f4
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:89e23177021d16bf959bf2c591f75bc5284a503bc35256e41f514dd58a4327f4
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:7eebe9862287fec6f2292acb17737062307083055ef75e2258bf90659d7a055f
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
$ docker pull rust@sha256:b353124551697953231aae2dd92f3a5eda8c03a3e1b048072a9d61a03a9c9f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7babd70875fa12e2f93e1bc32d8ca9c726a8c14f071b223e56f845152c19d98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055223b0c039c674a4a693ec584cd007a130abd127cde1a0be4c49fe58130afc`  
		Last Modified: Thu, 09 Jan 2025 22:46:19 GMT  
		Size: 273.0 MB (272976369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6388b285ba27595142573262570e5ca18d895aae7d60f19837c1cba43b11a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9571fdce4d22641e3a35297c07093ee0cc97650ffbe26d24713306c5468ce`

```dockerfile
```

-	Layers:
	-	`sha256:0716fc41687ba3e147ca7206a8fd91f3c5f17c5430b8e653b156fdfb46dbc53e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8c507f8775c0076fe162fc578a130d6262b7014621a0b92ae31b8cff2c1a0e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:6838e9cb67fe860cf4ad579d801f09eb72b899df748b91bb3e1ba947cdb5c979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7fe2a30e41bb1d4d966f5b6a0cbdc31a46b84d9a227a358e95e693891bda3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e967efca0462a2558586cfab92f23d28881b414fe0c7b86e1c99f3e4bf0c49`  
		Last Modified: Thu, 09 Jan 2025 22:42:19 GMT  
		Size: 313.8 MB (313802017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80d00667a000d9ae64cb0812d0ef0ccab2d02238b8a9564135e5bec0b673927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb9f7bb392b3cb19a42b4cba5e1b19c3c42f45d36d1408be47bfba5a8143f63`

```dockerfile
```

-	Layers:
	-	`sha256:60af30b4a5d8fb3668a08606db9b1bb98c6fbedb83c115d098a33ab49a7c9bef`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4fda87e5ad2ebdb737f190a34737c9aec3b0dc4c82f6a52c808a64aab05552`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
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
$ docker pull rust@sha256:f9ca146cb48a9074fc329cb4172c9bc27c4e1cefe1ab8e3ee91952c4a5aaa9bc
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
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:3fd50c6595ac668f97f0251e5f60f186155221f305223bc7ba8cfbea2aeee5d0
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
$ docker pull rust@sha256:197907590781d1bff52f88ff561c74da31657661437941b75ca91a27d278b54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516059357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06081ecc425b7ee4cb02941e1b408a80da8785d28244369750d5be88067d9e84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020df7deb9275b61ce28217dd066157be28a4f471a1f20f4ca1249f0d46d671`  
		Last Modified: Thu, 09 Jan 2025 22:30:04 GMT  
		Size: 194.9 MB (194934510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e13bb82df140da6886189d5c923c9d62121584a30550580e8042c0b1c0ab80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f632d1680769617f00696af7aab550d0193ee792a6bdc176d8d547b5f7ece6d5`

```dockerfile
```

-	Layers:
	-	`sha256:321d0765cdb0b7e87cf7e69804e78ed8cd7b2a942baa786b7e32b5e7fc8270d0`  
		Last Modified: Thu, 09 Jan 2025 22:29:59 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a89be5a5d9b0202dc4a6918a71d1059f99e8cf63aacb0e570fac4438cd3e5c`  
		Last Modified: Thu, 09 Jan 2025 22:29:59 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:0c8ef21098b2fe26dbe27245b880cff1783c61797ce7c3be4439e8821e6d03bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512770575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20324960d5bd49cef0397aae01c4d1dfe13dfdfa0290058f0422fe00be7ce468`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ceb953441df71e06cff2748ecdd8e6f1a88d8237bb1c52a18a2bd69529dcd3`  
		Last Modified: Thu, 09 Jan 2025 22:44:27 GMT  
		Size: 230.9 MB (230905569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2c9be0c39a11358bdd1cd407b54c6bf22059ba2e1addb3c42a0cbf21e50bfdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feed8f035ac9f426deb877b63cc7ffdc57c2c7744ed2d2c38b059e2a00a45d7`

```dockerfile
```

-	Layers:
	-	`sha256:43d3ea4f99e4b87a2cf917ae97d374a9bfe8f8f12c72b01e4123174faae8c8a2`  
		Last Modified: Thu, 09 Jan 2025 22:44:21 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb789d97c20fc3b57ceed945e52333794c709058117190929cf75bb065a5fbf`  
		Last Modified: Thu, 09 Jan 2025 22:44:20 GMT  
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
$ docker pull rust@sha256:aab0a9c7cbfc945613c3ce9aa0a16830f4de7f8c99b2aa047e9716374aabf9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538184174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c447c9b1570d63d14452f7c4d6ae80d9265510af13a9bc4ed16ab751a87b7393`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
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
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dbafd387d6cf7dca0cba801014dfc88c332f292f85b4301993e1b537d5b89c`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 211.4 MB (211439568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:28d890a892be4f61ca859b83ae7c7e87177823834c878cd58f8c1804d335c292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c904cc164a5b7fe3026caf96c0d82059cfe884912f50e73a2fc4a4eeab2753`

```dockerfile
```

-	Layers:
	-	`sha256:7d55dc7c165343a6fdd1b763a921b192b85c0279232436a3a575a5f452697f6e`  
		Last Modified: Thu, 09 Jan 2025 22:29:39 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedb06d9c2b29052d74afb059763d90fd82e256bc5724dfdd29dc44d6748fbef`  
		Last Modified: Thu, 09 Jan 2025 22:29:39 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:f7cbb35003d4ffb5543f8ad6480c1e36bbae5c3609523c9f0c2e223668ee9c1a
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
$ docker pull rust@sha256:b8624e2f3798a7747e0c271ba28143bcf8c6102ac7b9f93359a88fb7c5762318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (542994688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e579fdc67efcd51366cad94f6e05232c49f5b3deec384194e99e5f10e3f805c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4b5920f29d0d9c86d561d6afc39ec39f943c4163b42d8c0145f2a047020c6d`  
		Last Modified: Thu, 09 Jan 2025 22:30:07 GMT  
		Size: 194.9 MB (194934530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:7525c6e5fdaf8e84471b126ee760caeed800be2eb75bf0b29d1acb4a8d073bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b00805d403654e0ab8dbd6ec3b00bf6168eaea9395ac64f4bcb0821b7852f4`

```dockerfile
```

-	Layers:
	-	`sha256:f12b0654fb071b110313b362adf2899158c321b35998a641286feafd76132072`  
		Last Modified: Thu, 09 Jan 2025 22:30:03 GMT  
		Size: 15.5 MB (15474166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf4af630cec97a3ea2e7f01f10b3c2f0f2424f71eb48dc8ff12bc13f82a255b`  
		Last Modified: Thu, 09 Jan 2025 22:30:02 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:3d7249b301397ddc895a64333dd82e61e72cff9e5d6d3b5d0e120434f55b7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531754873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06514c83ed40b61eac37c8f3b4fb77f07fabb6eff33e37db00421a580a313a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1464670bcd9eb505f7b4872f0e39e68de2743b5495146740f66eefed978acf`  
		Last Modified: Thu, 09 Jan 2025 22:48:30 GMT  
		Size: 230.9 MB (230905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:2fdce30e3203734acd5d0ec1972b6b49e578400d9419edfa9efce3519818cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641e2a566929555463df6568420b2046e2739b1c113a9c74306548fca42f0b7`

```dockerfile
```

-	Layers:
	-	`sha256:81ab39f4b54346938a8cf1106585d637e254da5742de0043a2c9df132415f5c9`  
		Last Modified: Thu, 09 Jan 2025 22:48:25 GMT  
		Size: 15.3 MB (15278608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceba2485a35d937ed1ab66415eafcc288e70fba11fdedb60e088eccb3ad242`  
		Last Modified: Thu, 09 Jan 2025 22:48:24 GMT  
		Size: 13.2 KB (13246 bytes)  
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
$ docker pull rust@sha256:ac7e3e1c3c2a49df0a676c18dcfe48c0ee1c7f78d88dedd3529a5af2aeb7714e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562056925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454205eeccc1137bdbe0087841778f951370cb3109a28dda6981282f0101a9df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
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
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Last Modified: Wed, 25 Dec 2024 00:14:13 GMT  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394a7841c668d2444860f5bc9b8a5dd53c3858bd4f14ce87b9e95143f9c24b2e`  
		Last Modified: Thu, 09 Jan 2025 22:30:06 GMT  
		Size: 211.4 MB (211439523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:28b9d76584cfac33aa714961bb18cd1ab336a825ada3829f4579319caccc9685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4759a535523830e03f09fec64793abe44610fd5dcaad6c2b7a03252b55cea211`

```dockerfile
```

-	Layers:
	-	`sha256:44afa84018b93356b1c38c6b0d0b5a4eb7f6df0caadee2a621148b0b332397d4`  
		Last Modified: Thu, 09 Jan 2025 22:30:01 GMT  
		Size: 15.5 MB (15451428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dfac1485849c5e156f9d8c106763230e32a6e419d310f1cebd65fb29bdb3df`  
		Last Modified: Thu, 09 Jan 2025 22:30:00 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:0fdbe908df0a3ef12c4e2959c839906fb6e61de010d7ff13afae968d3f12ff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616852334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff36cf1d64d29fdb23d449ab845f679e788cb9d1689b9a802469d5b5b0205ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6515e3b2b44af3e974fddff91e63d603985980d955c79fa24985f464a3a49cd`  
		Last Modified: Thu, 09 Jan 2025 22:57:24 GMT  
		Size: 254.8 MB (254849169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:4a8ed5f0ceeb8e647257e187f1bb8529d73b07c8010f982e0a4069b330e6e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efc9e138b61f4479a8ee5367863897f43a2837134854a3fdde90cade9b1e69`

```dockerfile
```

-	Layers:
	-	`sha256:ceb3c019c0ad120cbbd83402800664264c5539bbcb5d257ffac5b90b5b128f77`  
		Last Modified: Thu, 09 Jan 2025 22:57:18 GMT  
		Size: 15.4 MB (15449272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76312d42514c0492464666b1a38e5e32abb8746c15e3f7a7c078918936731dd6`  
		Last Modified: Thu, 09 Jan 2025 22:57:17 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:3f4941f68d058f99c55bbf93f9d93ad735186b1d760332c0752a0c71c3b4222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 MB (599763046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7271b63034f0576b3652ca2ee0b4893f0c4a6ca150ae2ab9209dd0695791344`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c71bb3b82b956333fff3dc58e6a6466294b8cadf9af86cc4442311d6ef2a8d`  
		Last Modified: Thu, 09 Jan 2025 23:12:29 GMT  
		Size: 281.9 MB (281949952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:10728d946f437cc8726b8f8e3eca17e9c20fe4fbdaf5905152d006753cfb136e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b4ff81867c46b3ba2b248f8e577e80bf0d562400d7cbf30348bff8422ec6`

```dockerfile
```

-	Layers:
	-	`sha256:7cb1afa0ebf20690ef746bfa538a8bd454f1ea1fb9740266271759ca77e1e6e5`  
		Last Modified: Thu, 09 Jan 2025 23:12:25 GMT  
		Size: 15.3 MB (15286854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e722c0a62d9f02738ce2c05f54877dfff35e02564450b312c6ad5df5ff223112`  
		Last Modified: Thu, 09 Jan 2025 23:12:24 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:7cf7b873aefa40dbb7d40ea754550724effb2097b453820d6116a81787b9f75f
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:06297d7eba80f5953667461271f5e01615e756e34ac51cde54d98995db98ad01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355478217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a936dd761d59e8cbcc8476243ae61e7ab093d022f3b89f38d866d54163aef6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d6f617289490567ba886177f6914a2e3e40057fa717000944f48c3b2920b4d`  
		Last Modified: Thu, 09 Jan 2025 23:00:10 GMT  
		Size: 323.4 MB (323414977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4aee72daa79957e42d597d8bbda50b39be63653a7ce557d06a5d76511627d27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3220f6b29839ee6e81204fc05c147a8452d64a764b56f37306d17e7f1f9c85b5`

```dockerfile
```

-	Layers:
	-	`sha256:6cd30e046bd77a10cf1513d23d3f71d474ce5896d8df4d91adaa27df84ae450b`  
		Last Modified: Thu, 09 Jan 2025 22:59:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c2ae224b2c02a53b6dab829dd95a705f28da43fa6de6124e5d63105a546ff1`  
		Last Modified: Thu, 09 Jan 2025 22:59:58 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:0879c48ff3b004978c1b0733531c5ae312a394cc208d588cbb702689653e9329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358749704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbef53fe3abaa46ce09afd181d343b2c6bb297d42641f842d27083f5ac3fce54`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5287839d50805bc43b56d02f493940ce0c58fdb497162e727702879d04d1c`  
		Last Modified: Thu, 09 Jan 2025 22:34:24 GMT  
		Size: 331.9 MB (331870803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:afc68166b91c01caf824560436fd2fd43efcf383f9573df997f3f972ae0ea89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611314384161f9e181e852385c035a1b48f313e3e8182a0f8e6f18d0ab084097`

```dockerfile
```

-	Layers:
	-	`sha256:b70a26ea4ccde6b0ac595a2342b6d3290a4b4e534a3c3f604160219fecb4d076`  
		Last Modified: Thu, 09 Jan 2025 22:34:19 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6dfa6dc6c3e208755e993841bed1274f8a1c5d2384db33751190f28ccfc2de8`  
		Last Modified: Thu, 09 Jan 2025 22:34:19 GMT  
		Size: 13.3 KB (13270 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:7cf7b873aefa40dbb7d40ea754550724effb2097b453820d6116a81787b9f75f
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
$ docker pull rust@sha256:eef35a5a2d22ae3b28a84e4cbc92c0708ffb29776ae08455ce2c4163400f558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302487046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dda71558bb77e1c85dd920ceee83dab97fe752ee62be981f94430d969e4f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5263ef81284882fd7e7bb3ce7cdf66faa65fd2cd755c49857c096cd1c031b7`  
		Last Modified: Thu, 09 Jan 2025 22:50:23 GMT  
		Size: 278.6 MB (278553524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:641a02990c3a2e1b5e3368b01c6901e92597397d02f5b234b7133bb96cb5c80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844150a2373e63156c9b83590fd4721d56decce2c2efe82ba753fe9a264dcd94`

```dockerfile
```

-	Layers:
	-	`sha256:b2201bd10c8b638fcf4cd50c7191d6eb951decbd0323f6955b6b4ae57ce13803`  
		Last Modified: Thu, 09 Jan 2025 22:50:16 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f5079c54750c5822070eca5c418cbf0639d69239ca5712c5e0eae7c638d04`  
		Last Modified: Thu, 09 Jan 2025 22:50:15 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bc740ef98e8b9cd7bda7cd7040c9895fea3bd8c68833b58026434408f0435074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352017861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fde31c7bf056aa378808e10134be875cf4a5708f827a3bdcca43b3b37e9be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97482f119c8540c16267e790d74033821fc90d537052b7ed196f9cea1fce032`  
		Last Modified: Thu, 09 Jan 2025 22:45:22 GMT  
		Size: 324.0 MB (323959138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d801c5c10fc472b03b10508615950574d821abd28527b62337a2c7b8342baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2a9956d85454811f6213cd7a59cae1b7de547f5117271852f66f57425d1496`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3fc7bbd2529fc491ffd1e41cd86fab148bbee4b4abe2cf7c5f132bec8d72c`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585e10f585f5cba1c7f13baf8bfee09e2ca48235cc7bac08e907eafa1e2e928`  
		Last Modified: Thu, 09 Jan 2025 22:45:15 GMT  
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
$ docker pull rust@sha256:06297d7eba80f5953667461271f5e01615e756e34ac51cde54d98995db98ad01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355478217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a936dd761d59e8cbcc8476243ae61e7ab093d022f3b89f38d866d54163aef6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d6f617289490567ba886177f6914a2e3e40057fa717000944f48c3b2920b4d`  
		Last Modified: Thu, 09 Jan 2025 23:00:10 GMT  
		Size: 323.4 MB (323414977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4aee72daa79957e42d597d8bbda50b39be63653a7ce557d06a5d76511627d27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3220f6b29839ee6e81204fc05c147a8452d64a764b56f37306d17e7f1f9c85b5`

```dockerfile
```

-	Layers:
	-	`sha256:6cd30e046bd77a10cf1513d23d3f71d474ce5896d8df4d91adaa27df84ae450b`  
		Last Modified: Thu, 09 Jan 2025 22:59:59 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c2ae224b2c02a53b6dab829dd95a705f28da43fa6de6124e5d63105a546ff1`  
		Last Modified: Thu, 09 Jan 2025 22:59:58 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:0879c48ff3b004978c1b0733531c5ae312a394cc208d588cbb702689653e9329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358749704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbef53fe3abaa46ce09afd181d343b2c6bb297d42641f842d27083f5ac3fce54`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5287839d50805bc43b56d02f493940ce0c58fdb497162e727702879d04d1c`  
		Last Modified: Thu, 09 Jan 2025 22:34:24 GMT  
		Size: 331.9 MB (331870803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:afc68166b91c01caf824560436fd2fd43efcf383f9573df997f3f972ae0ea89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611314384161f9e181e852385c035a1b48f313e3e8182a0f8e6f18d0ab084097`

```dockerfile
```

-	Layers:
	-	`sha256:b70a26ea4ccde6b0ac595a2342b6d3290a4b4e534a3c3f604160219fecb4d076`  
		Last Modified: Thu, 09 Jan 2025 22:34:19 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6dfa6dc6c3e208755e993841bed1274f8a1c5d2384db33751190f28ccfc2de8`  
		Last Modified: Thu, 09 Jan 2025 22:34:19 GMT  
		Size: 13.3 KB (13270 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:7eebe9862287fec6f2292acb17737062307083055ef75e2258bf90659d7a055f
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
$ docker pull rust@sha256:b353124551697953231aae2dd92f3a5eda8c03a3e1b048072a9d61a03a9c9f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7babd70875fa12e2f93e1bc32d8ca9c726a8c14f071b223e56f845152c19d98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055223b0c039c674a4a693ec584cd007a130abd127cde1a0be4c49fe58130afc`  
		Last Modified: Thu, 09 Jan 2025 22:46:19 GMT  
		Size: 273.0 MB (272976369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6388b285ba27595142573262570e5ca18d895aae7d60f19837c1cba43b11a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9571fdce4d22641e3a35297c07093ee0cc97650ffbe26d24713306c5468ce`

```dockerfile
```

-	Layers:
	-	`sha256:0716fc41687ba3e147ca7206a8fd91f3c5f17c5430b8e653b156fdfb46dbc53e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8c507f8775c0076fe162fc578a130d6262b7014621a0b92ae31b8cff2c1a0e`  
		Last Modified: Thu, 09 Jan 2025 22:46:12 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:6838e9cb67fe860cf4ad579d801f09eb72b899df748b91bb3e1ba947cdb5c979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342546870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7fe2a30e41bb1d4d966f5b6a0cbdc31a46b84d9a227a358e95e693891bda3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e967efca0462a2558586cfab92f23d28881b414fe0c7b86e1c99f3e4bf0c49`  
		Last Modified: Thu, 09 Jan 2025 22:42:19 GMT  
		Size: 313.8 MB (313802017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80d00667a000d9ae64cb0812d0ef0ccab2d02238b8a9564135e5bec0b673927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb9f7bb392b3cb19a42b4cba5e1b19c3c42f45d36d1408be47bfba5a8143f63`

```dockerfile
```

-	Layers:
	-	`sha256:60af30b4a5d8fb3668a08606db9b1bb98c6fbedb83c115d098a33ab49a7c9bef`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4fda87e5ad2ebdb737f190a34737c9aec3b0dc4c82f6a52c808a64aab05552`  
		Last Modified: Thu, 09 Jan 2025 22:42:13 GMT  
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
