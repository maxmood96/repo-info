<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rust`

-	[`rust:1`](#rust1)
-	[`rust:1-alpine`](#rust1-alpine)
-	[`rust:1-alpine3.19`](#rust1-alpine319)
-	[`rust:1-alpine3.20`](#rust1-alpine320)
-	[`rust:1-bookworm`](#rust1-bookworm)
-	[`rust:1-bullseye`](#rust1-bullseye)
-	[`rust:1-slim`](#rust1-slim)
-	[`rust:1-slim-bookworm`](#rust1-slim-bookworm)
-	[`rust:1-slim-bullseye`](#rust1-slim-bullseye)
-	[`rust:1.82`](#rust182)
-	[`rust:1.82-alpine`](#rust182-alpine)
-	[`rust:1.82-alpine3.19`](#rust182-alpine319)
-	[`rust:1.82-alpine3.20`](#rust182-alpine320)
-	[`rust:1.82-bookworm`](#rust182-bookworm)
-	[`rust:1.82-bullseye`](#rust182-bullseye)
-	[`rust:1.82-slim`](#rust182-slim)
-	[`rust:1.82-slim-bookworm`](#rust182-slim-bookworm)
-	[`rust:1.82-slim-bullseye`](#rust182-slim-bullseye)
-	[`rust:1.82.0`](#rust1820)
-	[`rust:1.82.0-alpine`](#rust1820-alpine)
-	[`rust:1.82.0-alpine3.19`](#rust1820-alpine319)
-	[`rust:1.82.0-alpine3.20`](#rust1820-alpine320)
-	[`rust:1.82.0-bookworm`](#rust1820-bookworm)
-	[`rust:1.82.0-bullseye`](#rust1820-bullseye)
-	[`rust:1.82.0-slim`](#rust1820-slim)
-	[`rust:1.82.0-slim-bookworm`](#rust1820-slim-bookworm)
-	[`rust:1.82.0-slim-bullseye`](#rust1820-slim-bullseye)
-	[`rust:alpine`](#rustalpine)
-	[`rust:alpine3.19`](#rustalpine319)
-	[`rust:alpine3.20`](#rustalpine320)
-	[`rust:bookworm`](#rustbookworm)
-	[`rust:bullseye`](#rustbullseye)
-	[`rust:latest`](#rustlatest)
-	[`rust:slim`](#rustslim)
-	[`rust:slim-bookworm`](#rustslim-bookworm)
-	[`rust:slim-bullseye`](#rustslim-bullseye)

## `rust:1`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:97f288e992a424decbe9615f79e3c30a00e402d9ad1c51d17b801d9101ae1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:cd6e942d21a09065bb77508e0652cad35ef32938cee4727f8e00c4ef3ae4f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291926676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52bab6d057387ec516cb502d1d9be60aaa9ae67f887fa4204ad3778c824deef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7f9aa2a63c77c6dfea9a616ba8de311167963accbb062595e525a14855dd77`  
		Last Modified: Tue, 12 Nov 2024 02:49:15 GMT  
		Size: 55.3 MB (55346808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e15e1bb1f3d07546e99251b81032a4a9038fadbf9b9ebd27e2afbf930429d`  
		Last Modified: Tue, 12 Nov 2024 02:49:19 GMT  
		Size: 233.2 MB (233160140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7dbbbafbd89f297fdf36b0e0086b8d676e024539d52d541582c9f41e063ed24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.5 KB (724455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8758812fd52c11e30054af7f1f6afd3dc1d32b6bffee934556cc4642587c469e`

```dockerfile
```

-	Layers:
	-	`sha256:30f938cb5f53250c3b423cd92520cd8df1cd4fbbc6f7610f85795ac313fbb787`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 713.7 KB (713741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ec1f9818cc762ca92550827ee60d791ab5ba54775746c16d27c288d6446876`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee73aa941f7f42a52806c7623cb5b5271b90181aa05abaf14151a2320c9491b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9fd4d3a567c83547ff5ee24912a3772e77b46a60ca37f8b1c3c499f99ef27f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebc171e95d6bf960ff3cf365c04babb4ca82931639761616e97fc9f7699ba75`  
		Last Modified: Wed, 13 Nov 2024 00:35:25 GMT  
		Size: 53.0 MB (52995408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae93b63d515bac85a5051eab1aacd3ca57f69ea278af4f11e768c8134d6c6a1`  
		Last Modified: Wed, 13 Nov 2024 00:35:29 GMT  
		Size: 241.8 MB (241799098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:45f9c9f8dc8a5dd916bf7e5e98fca928095ec5e91f383dde541787d0b64d4f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.6 KB (760560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a5caaf1b41326160ade3e1bac141e929552ae2120a7d52fa9a8bd4e1b8581`

```dockerfile
```

-	Layers:
	-	`sha256:ecc6747c67076702a78a1077b6c1658fc362defe289e25d04437932f7de077d0`  
		Last Modified: Wed, 13 Nov 2024 00:35:24 GMT  
		Size: 749.7 KB (749728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5adc7278371532a6e6c52aa5a4f51f4408fc55e2fd059c1d42c48f0eec6b3a0`  
		Last Modified: Wed, 13 Nov 2024 00:35:23 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:821c41ed8d70347b32c2a3e4779fa0f05354773adf627aa388d0904494e0d21f
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
$ docker pull rust@sha256:ac7fe7b0c9429313c0fe87d3a8993998d1fe2be9e3e91b5e2ec05d3a09d87128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515318572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3a03a3335d927012667a8b813477a2783f016be5e4a6ae0a648e64402f08b7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf13695a4667af089ddeff6d2392e21ee9a9600a153405de88278675194f82`  
		Last Modified: Tue, 12 Nov 2024 04:58:34 GMT  
		Size: 192.8 MB (192841813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dbf4f736b889695983fe0f74ac4895df43b1ddba6c62c09ca12b4c7042c4b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc97b7bb10c521654d8058f494bdccbbe29e6b0c72d47b53c1f54f075404c0a`

```dockerfile
```

-	Layers:
	-	`sha256:8c22210fba04d18da54e27688ea2ebc19dc1495b47987f7d8e2473f924c87de6`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 15.1 MB (15100321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834cec5d6d5bd036412098f75fdff73b866b61622fe68d26312d54769721b4be`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:db7987a6a911e3886d3cb8f0b9d8f8b1964a38a6657964856baaea66d98941c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.0 MB (512008019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2c0509b956e675536faf99961931c405854d284801b023610ba3b6c1660a19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b22721db94b1c5fff4e7c6f09aa650c06de76f3b42c9ec977d76b8bf11c268`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 50.6 MB (50624136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb575aeaeee118c4f0db03d2fd601e49cd3f7cc07844c7bc2872425a446e4581`  
		Last Modified: Wed, 13 Nov 2024 15:27:10 GMT  
		Size: 167.5 MB (167519575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4061e9ce1ac5c8ce1e6c1271fd215f85fd0caebf6a11b4bf5a559a169ead00e5`  
		Last Modified: Thu, 14 Nov 2024 01:11:49 GMT  
		Size: 228.9 MB (228918662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f4c0fd57647af42bfd08c8162dfa75b9f36e0a793e947b5d3dc941013f0fdb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deef6ec419164cf481190c3102f81bf86ad0d0352e7347206b514f9fd7b48911`

```dockerfile
```

-	Layers:
	-	`sha256:a8eaf9bf0d7f500e7114791b6823f3b1b42423249f2e4cf95802db52cbe532a1`  
		Last Modified: Thu, 14 Nov 2024 01:11:45 GMT  
		Size: 14.9 MB (14900833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa22d22ca7c1e99c5fb92ba9ffd957995e50b04e0e5d965fd84e8196fded821`  
		Last Modified: Thu, 14 Nov 2024 01:11:44 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3c1b8b6487513ad4e753d008b960260f5bcc81bf110883460f6ed3cd72bf439b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570127971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c848f57e79cdedc6cd3735c641da59e5b67b257ee5e425a3bbed79e4bac60e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8ab89b79ca6b4fbc5b7006d242a238846ed57f82ebef3fc069e6bb0aa0532`  
		Last Modified: Wed, 13 Nov 2024 08:04:21 GMT  
		Size: 190.0 MB (189977453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc648336fb27f4a381de2ee878010c61a10dfff0f5076696589bb3f361cd0d`  
		Last Modified: Wed, 13 Nov 2024 16:38:36 GMT  
		Size: 256.0 MB (256007774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a55d070e2b801c4e7b3f26c4a383d1f5eddb1e4b258528e346640a42320bfccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05549fa930481c360c81fafd9e514010d1691a05f4944fe6edcd4d7d1afd2ead`

```dockerfile
```

-	Layers:
	-	`sha256:efc4fe85574fe6d885a0135708bfd7d7542ae71f6c6575075661d61cbe0231ae`  
		Last Modified: Wed, 13 Nov 2024 16:38:31 GMT  
		Size: 15.1 MB (15102584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b2c9fefb8cc2c49cbf1fbcf62430363a686afb9b8f600552b5a21c42078ae7`  
		Last Modified: Wed, 13 Nov 2024 16:38:30 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:bb93303cbbf2a6f13285a70752f54d8a38bef5bcb3062466b9e1f989017fe702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 MB (533944108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f612b8e9426a4b0877d8ab94ea3f429c9e0bf9b77f33be696a50599b2596a247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd146822c599cb06a479cc8a6b587e7e18c5d0a349e0ff98559b0f8ef702bff7`  
		Last Modified: Tue, 12 Nov 2024 05:00:40 GMT  
		Size: 205.8 MB (205777260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:57a1081dab6ba9c47e9f720f8173aede6afd9004489dd73aaf8cccc3924c05e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b58c341cb8c133e64f996d0142603f99482f576f3e5f87f06556d9ca780e2`

```dockerfile
```

-	Layers:
	-	`sha256:24739993ed260b2f5d9fed21b83b4cee87d793c1bd2be864e0f4c6e5eb64f04b`  
		Last Modified: Tue, 12 Nov 2024 05:00:36 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba69b43f8ff46a09b75e788fc87bf05a66f1f3cb8d09342462ffbc2be63eb180`  
		Last Modified: Tue, 12 Nov 2024 05:00:35 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:426a0b287a98f7410fb4d84e5401d6ea65b75689ba10954dc73fc1fcee1ae578
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
$ docker pull rust@sha256:46bad2a122975b3d3f7443e137015e0567bc4c63e467a818d9b92517def5f4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284233275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20005414bebc60c5e0e08412413bebf1a7a9685c7ae5411b6e0fd371eed0c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ca049328c7f2e77bd9aafe9ffb887994cf0637a356d52b36402517bb8ff41`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 252.8 MB (252781714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b24a3c097f184d33a580a49ae0f91e1f5ac1b3c79149c3cd79217d518767f2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1192d242e71bdf8d75dc252c942825e2d222c60589b4126b05d82300741bd98e`

```dockerfile
```

-	Layers:
	-	`sha256:c286e2858ed675836066788d3c16ed369b62052679d7642f2742efdad5df00b3`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 4.2 MB (4180445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8ffaaca173ca6838a3831e1eea198848e426424e8bceb80bb4731eafb5114a`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:76576a36e6ad266cccfa0044392a83b85fca6968b6f07fd76236d8603b4afb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297576818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68c6648bd2f42e819f5b39f925030ed571d2650c70c2f07280aca4f332620b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf03adada101d85359afaebfbc1d698d434dad47cf1a9dafcb16911b27c4b867`  
		Last Modified: Wed, 13 Nov 2024 06:45:26 GMT  
		Size: 271.0 MB (270967561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c575f6124afb181b7f79518350ff888d118fcbc148de5d2e0b391dab13df7b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c08ed3ad7250cd9730a1c4fb8455c796f0de9238b7b4ae900823d05fb6d7a6`

```dockerfile
```

-	Layers:
	-	`sha256:12e739030d49ed6aacd7db0ddedd88fa58c190294ad641a4ce3b5f9e5e3ef8d7`  
		Last Modified: Wed, 13 Nov 2024 06:45:20 GMT  
		Size: 4.0 MB (3989372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248b0521bdab09596cf4057ce0d64b69c8a46f51da17be753b2931a5043a6461`  
		Last Modified: Wed, 13 Nov 2024 06:45:19 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d1b01f909e5ba4510de1683935432ae49a4cc229593f2e2db5515ed7a142c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341577259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3624a5f3bf954bd9d6cbfd3daaf86be98102d31aa008ef0197e584f3fb1abdf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3a97815435189dd53bc1eb929e5332889ac83992be4a9447a0003d6cb04e6f`  
		Last Modified: Wed, 13 Nov 2024 00:32:40 GMT  
		Size: 311.5 MB (311485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fb8084595c3540aacedd7c1ce79105f1ac40be4b59940a81eafa9ec2622edf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adfc1595344e5ac0cabc50fe5884d5188f86429a0f0a0b5ecdbe65d43d9001c`

```dockerfile
```

-	Layers:
	-	`sha256:f57e0e66aad4bb0ea22da924e559e24e7f91b79738fee570bb47625815ef277f`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 4.2 MB (4177121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea60ed2a103340d5408146aac5f4caa9f1930e826771dd79d6a19aa6637b5545`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 11.5 KB (11459 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3bdeb9e24e380d38f6a23d0c9782a72e34654b369e55453c9dd16117cbdd0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298773484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c62dd3561fec89c84a360fab38b6e9e8003d483764def127392706f674a1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3673d63c7e778356d62082b73f2357833a19e623f528d8e62dac957eda0b1`  
		Last Modified: Tue, 12 Nov 2024 02:21:10 GMT  
		Size: 266.4 MB (266350133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:267b340e78c456f02251bc3627d2d7de83ef717be46dc8058590516f34fee8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5484b707a28f321ab31fe64503300cd90613dbb93744d2cac76d4130d5989177`

```dockerfile
```

-	Layers:
	-	`sha256:1bee8187641b794234139ce1a879c7fc7c8213884bc1e7a71f0cf257c38e00bb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccf11ed2511f7334e4dbabbd3d36b7bb3df5f402a672da7b8ac3616d0397aa`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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

### `rust:1.82` - linux; amd64

```console
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-alpine`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.82-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-alpine3.19`

```console
$ docker pull rust@sha256:97f288e992a424decbe9615f79e3c30a00e402d9ad1c51d17b801d9101ae1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.82-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:cd6e942d21a09065bb77508e0652cad35ef32938cee4727f8e00c4ef3ae4f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291926676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52bab6d057387ec516cb502d1d9be60aaa9ae67f887fa4204ad3778c824deef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7f9aa2a63c77c6dfea9a616ba8de311167963accbb062595e525a14855dd77`  
		Last Modified: Tue, 12 Nov 2024 02:49:15 GMT  
		Size: 55.3 MB (55346808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e15e1bb1f3d07546e99251b81032a4a9038fadbf9b9ebd27e2afbf930429d`  
		Last Modified: Tue, 12 Nov 2024 02:49:19 GMT  
		Size: 233.2 MB (233160140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7dbbbafbd89f297fdf36b0e0086b8d676e024539d52d541582c9f41e063ed24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.5 KB (724455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8758812fd52c11e30054af7f1f6afd3dc1d32b6bffee934556cc4642587c469e`

```dockerfile
```

-	Layers:
	-	`sha256:30f938cb5f53250c3b423cd92520cd8df1cd4fbbc6f7610f85795ac313fbb787`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 713.7 KB (713741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ec1f9818cc762ca92550827ee60d791ab5ba54775746c16d27c288d6446876`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee73aa941f7f42a52806c7623cb5b5271b90181aa05abaf14151a2320c9491b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9fd4d3a567c83547ff5ee24912a3772e77b46a60ca37f8b1c3c499f99ef27f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebc171e95d6bf960ff3cf365c04babb4ca82931639761616e97fc9f7699ba75`  
		Last Modified: Wed, 13 Nov 2024 00:35:25 GMT  
		Size: 53.0 MB (52995408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae93b63d515bac85a5051eab1aacd3ca57f69ea278af4f11e768c8134d6c6a1`  
		Last Modified: Wed, 13 Nov 2024 00:35:29 GMT  
		Size: 241.8 MB (241799098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:45f9c9f8dc8a5dd916bf7e5e98fca928095ec5e91f383dde541787d0b64d4f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.6 KB (760560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a5caaf1b41326160ade3e1bac141e929552ae2120a7d52fa9a8bd4e1b8581`

```dockerfile
```

-	Layers:
	-	`sha256:ecc6747c67076702a78a1077b6c1658fc362defe289e25d04437932f7de077d0`  
		Last Modified: Wed, 13 Nov 2024 00:35:24 GMT  
		Size: 749.7 KB (749728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5adc7278371532a6e6c52aa5a4f51f4408fc55e2fd059c1d42c48f0eec6b3a0`  
		Last Modified: Wed, 13 Nov 2024 00:35:23 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-alpine3.20`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.82-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-bookworm`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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

### `rust:1.82-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-bullseye`

```console
$ docker pull rust@sha256:821c41ed8d70347b32c2a3e4779fa0f05354773adf627aa388d0904494e0d21f
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

### `rust:1.82-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ac7fe7b0c9429313c0fe87d3a8993998d1fe2be9e3e91b5e2ec05d3a09d87128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515318572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3a03a3335d927012667a8b813477a2783f016be5e4a6ae0a648e64402f08b7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf13695a4667af089ddeff6d2392e21ee9a9600a153405de88278675194f82`  
		Last Modified: Tue, 12 Nov 2024 04:58:34 GMT  
		Size: 192.8 MB (192841813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dbf4f736b889695983fe0f74ac4895df43b1ddba6c62c09ca12b4c7042c4b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc97b7bb10c521654d8058f494bdccbbe29e6b0c72d47b53c1f54f075404c0a`

```dockerfile
```

-	Layers:
	-	`sha256:8c22210fba04d18da54e27688ea2ebc19dc1495b47987f7d8e2473f924c87de6`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 15.1 MB (15100321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834cec5d6d5bd036412098f75fdff73b866b61622fe68d26312d54769721b4be`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:db7987a6a911e3886d3cb8f0b9d8f8b1964a38a6657964856baaea66d98941c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.0 MB (512008019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2c0509b956e675536faf99961931c405854d284801b023610ba3b6c1660a19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b22721db94b1c5fff4e7c6f09aa650c06de76f3b42c9ec977d76b8bf11c268`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 50.6 MB (50624136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb575aeaeee118c4f0db03d2fd601e49cd3f7cc07844c7bc2872425a446e4581`  
		Last Modified: Wed, 13 Nov 2024 15:27:10 GMT  
		Size: 167.5 MB (167519575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4061e9ce1ac5c8ce1e6c1271fd215f85fd0caebf6a11b4bf5a559a169ead00e5`  
		Last Modified: Thu, 14 Nov 2024 01:11:49 GMT  
		Size: 228.9 MB (228918662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f4c0fd57647af42bfd08c8162dfa75b9f36e0a793e947b5d3dc941013f0fdb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deef6ec419164cf481190c3102f81bf86ad0d0352e7347206b514f9fd7b48911`

```dockerfile
```

-	Layers:
	-	`sha256:a8eaf9bf0d7f500e7114791b6823f3b1b42423249f2e4cf95802db52cbe532a1`  
		Last Modified: Thu, 14 Nov 2024 01:11:45 GMT  
		Size: 14.9 MB (14900833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa22d22ca7c1e99c5fb92ba9ffd957995e50b04e0e5d965fd84e8196fded821`  
		Last Modified: Thu, 14 Nov 2024 01:11:44 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3c1b8b6487513ad4e753d008b960260f5bcc81bf110883460f6ed3cd72bf439b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570127971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c848f57e79cdedc6cd3735c641da59e5b67b257ee5e425a3bbed79e4bac60e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8ab89b79ca6b4fbc5b7006d242a238846ed57f82ebef3fc069e6bb0aa0532`  
		Last Modified: Wed, 13 Nov 2024 08:04:21 GMT  
		Size: 190.0 MB (189977453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc648336fb27f4a381de2ee878010c61a10dfff0f5076696589bb3f361cd0d`  
		Last Modified: Wed, 13 Nov 2024 16:38:36 GMT  
		Size: 256.0 MB (256007774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a55d070e2b801c4e7b3f26c4a383d1f5eddb1e4b258528e346640a42320bfccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05549fa930481c360c81fafd9e514010d1691a05f4944fe6edcd4d7d1afd2ead`

```dockerfile
```

-	Layers:
	-	`sha256:efc4fe85574fe6d885a0135708bfd7d7542ae71f6c6575075661d61cbe0231ae`  
		Last Modified: Wed, 13 Nov 2024 16:38:31 GMT  
		Size: 15.1 MB (15102584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b2c9fefb8cc2c49cbf1fbcf62430363a686afb9b8f600552b5a21c42078ae7`  
		Last Modified: Wed, 13 Nov 2024 16:38:30 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bullseye` - linux; 386

```console
$ docker pull rust@sha256:bb93303cbbf2a6f13285a70752f54d8a38bef5bcb3062466b9e1f989017fe702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 MB (533944108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f612b8e9426a4b0877d8ab94ea3f429c9e0bf9b77f33be696a50599b2596a247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd146822c599cb06a479cc8a6b587e7e18c5d0a349e0ff98559b0f8ef702bff7`  
		Last Modified: Tue, 12 Nov 2024 05:00:40 GMT  
		Size: 205.8 MB (205777260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:57a1081dab6ba9c47e9f720f8173aede6afd9004489dd73aaf8cccc3924c05e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b58c341cb8c133e64f996d0142603f99482f576f3e5f87f06556d9ca780e2`

```dockerfile
```

-	Layers:
	-	`sha256:24739993ed260b2f5d9fed21b83b4cee87d793c1bd2be864e0f4c6e5eb64f04b`  
		Last Modified: Tue, 12 Nov 2024 05:00:36 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba69b43f8ff46a09b75e788fc87bf05a66f1f3cb8d09342462ffbc2be63eb180`  
		Last Modified: Tue, 12 Nov 2024 05:00:35 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-slim`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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

### `rust:1.82-slim` - linux; amd64

```console
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-slim-bookworm`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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

### `rust:1.82-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-slim-bullseye`

```console
$ docker pull rust@sha256:426a0b287a98f7410fb4d84e5401d6ea65b75689ba10954dc73fc1fcee1ae578
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

### `rust:1.82-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:46bad2a122975b3d3f7443e137015e0567bc4c63e467a818d9b92517def5f4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284233275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20005414bebc60c5e0e08412413bebf1a7a9685c7ae5411b6e0fd371eed0c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ca049328c7f2e77bd9aafe9ffb887994cf0637a356d52b36402517bb8ff41`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 252.8 MB (252781714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b24a3c097f184d33a580a49ae0f91e1f5ac1b3c79149c3cd79217d518767f2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1192d242e71bdf8d75dc252c942825e2d222c60589b4126b05d82300741bd98e`

```dockerfile
```

-	Layers:
	-	`sha256:c286e2858ed675836066788d3c16ed369b62052679d7642f2742efdad5df00b3`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 4.2 MB (4180445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8ffaaca173ca6838a3831e1eea198848e426424e8bceb80bb4731eafb5114a`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:76576a36e6ad266cccfa0044392a83b85fca6968b6f07fd76236d8603b4afb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297576818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68c6648bd2f42e819f5b39f925030ed571d2650c70c2f07280aca4f332620b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf03adada101d85359afaebfbc1d698d434dad47cf1a9dafcb16911b27c4b867`  
		Last Modified: Wed, 13 Nov 2024 06:45:26 GMT  
		Size: 271.0 MB (270967561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c575f6124afb181b7f79518350ff888d118fcbc148de5d2e0b391dab13df7b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c08ed3ad7250cd9730a1c4fb8455c796f0de9238b7b4ae900823d05fb6d7a6`

```dockerfile
```

-	Layers:
	-	`sha256:12e739030d49ed6aacd7db0ddedd88fa58c190294ad641a4ce3b5f9e5e3ef8d7`  
		Last Modified: Wed, 13 Nov 2024 06:45:20 GMT  
		Size: 4.0 MB (3989372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248b0521bdab09596cf4057ce0d64b69c8a46f51da17be753b2931a5043a6461`  
		Last Modified: Wed, 13 Nov 2024 06:45:19 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d1b01f909e5ba4510de1683935432ae49a4cc229593f2e2db5515ed7a142c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341577259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3624a5f3bf954bd9d6cbfd3daaf86be98102d31aa008ef0197e584f3fb1abdf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3a97815435189dd53bc1eb929e5332889ac83992be4a9447a0003d6cb04e6f`  
		Last Modified: Wed, 13 Nov 2024 00:32:40 GMT  
		Size: 311.5 MB (311485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fb8084595c3540aacedd7c1ce79105f1ac40be4b59940a81eafa9ec2622edf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adfc1595344e5ac0cabc50fe5884d5188f86429a0f0a0b5ecdbe65d43d9001c`

```dockerfile
```

-	Layers:
	-	`sha256:f57e0e66aad4bb0ea22da924e559e24e7f91b79738fee570bb47625815ef277f`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 4.2 MB (4177121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea60ed2a103340d5408146aac5f4caa9f1930e826771dd79d6a19aa6637b5545`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 11.5 KB (11459 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3bdeb9e24e380d38f6a23d0c9782a72e34654b369e55453c9dd16117cbdd0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298773484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c62dd3561fec89c84a360fab38b6e9e8003d483764def127392706f674a1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3673d63c7e778356d62082b73f2357833a19e623f528d8e62dac957eda0b1`  
		Last Modified: Tue, 12 Nov 2024 02:21:10 GMT  
		Size: 266.4 MB (266350133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:267b340e78c456f02251bc3627d2d7de83ef717be46dc8058590516f34fee8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5484b707a28f321ab31fe64503300cd90613dbb93744d2cac76d4130d5989177`

```dockerfile
```

-	Layers:
	-	`sha256:1bee8187641b794234139ce1a879c7fc7c8213884bc1e7a71f0cf257c38e00bb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccf11ed2511f7334e4dbabbd3d36b7bb3df5f402a672da7b8ac3616d0397aa`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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

### `rust:1.82.0` - linux; amd64

```console
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-alpine`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.82.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-alpine3.19`

```console
$ docker pull rust@sha256:97f288e992a424decbe9615f79e3c30a00e402d9ad1c51d17b801d9101ae1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.82.0-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:cd6e942d21a09065bb77508e0652cad35ef32938cee4727f8e00c4ef3ae4f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291926676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52bab6d057387ec516cb502d1d9be60aaa9ae67f887fa4204ad3778c824deef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7f9aa2a63c77c6dfea9a616ba8de311167963accbb062595e525a14855dd77`  
		Last Modified: Tue, 12 Nov 2024 02:49:15 GMT  
		Size: 55.3 MB (55346808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e15e1bb1f3d07546e99251b81032a4a9038fadbf9b9ebd27e2afbf930429d`  
		Last Modified: Tue, 12 Nov 2024 02:49:19 GMT  
		Size: 233.2 MB (233160140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7dbbbafbd89f297fdf36b0e0086b8d676e024539d52d541582c9f41e063ed24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.5 KB (724455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8758812fd52c11e30054af7f1f6afd3dc1d32b6bffee934556cc4642587c469e`

```dockerfile
```

-	Layers:
	-	`sha256:30f938cb5f53250c3b423cd92520cd8df1cd4fbbc6f7610f85795ac313fbb787`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 713.7 KB (713741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ec1f9818cc762ca92550827ee60d791ab5ba54775746c16d27c288d6446876`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee73aa941f7f42a52806c7623cb5b5271b90181aa05abaf14151a2320c9491b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9fd4d3a567c83547ff5ee24912a3772e77b46a60ca37f8b1c3c499f99ef27f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebc171e95d6bf960ff3cf365c04babb4ca82931639761616e97fc9f7699ba75`  
		Last Modified: Wed, 13 Nov 2024 00:35:25 GMT  
		Size: 53.0 MB (52995408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae93b63d515bac85a5051eab1aacd3ca57f69ea278af4f11e768c8134d6c6a1`  
		Last Modified: Wed, 13 Nov 2024 00:35:29 GMT  
		Size: 241.8 MB (241799098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:45f9c9f8dc8a5dd916bf7e5e98fca928095ec5e91f383dde541787d0b64d4f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.6 KB (760560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a5caaf1b41326160ade3e1bac141e929552ae2120a7d52fa9a8bd4e1b8581`

```dockerfile
```

-	Layers:
	-	`sha256:ecc6747c67076702a78a1077b6c1658fc362defe289e25d04437932f7de077d0`  
		Last Modified: Wed, 13 Nov 2024 00:35:24 GMT  
		Size: 749.7 KB (749728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5adc7278371532a6e6c52aa5a4f51f4408fc55e2fd059c1d42c48f0eec6b3a0`  
		Last Modified: Wed, 13 Nov 2024 00:35:23 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-alpine3.20`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.82.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-bookworm`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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

### `rust:1.82.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-bullseye`

```console
$ docker pull rust@sha256:821c41ed8d70347b32c2a3e4779fa0f05354773adf627aa388d0904494e0d21f
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

### `rust:1.82.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ac7fe7b0c9429313c0fe87d3a8993998d1fe2be9e3e91b5e2ec05d3a09d87128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515318572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3a03a3335d927012667a8b813477a2783f016be5e4a6ae0a648e64402f08b7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf13695a4667af089ddeff6d2392e21ee9a9600a153405de88278675194f82`  
		Last Modified: Tue, 12 Nov 2024 04:58:34 GMT  
		Size: 192.8 MB (192841813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dbf4f736b889695983fe0f74ac4895df43b1ddba6c62c09ca12b4c7042c4b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc97b7bb10c521654d8058f494bdccbbe29e6b0c72d47b53c1f54f075404c0a`

```dockerfile
```

-	Layers:
	-	`sha256:8c22210fba04d18da54e27688ea2ebc19dc1495b47987f7d8e2473f924c87de6`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 15.1 MB (15100321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834cec5d6d5bd036412098f75fdff73b866b61622fe68d26312d54769721b4be`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:db7987a6a911e3886d3cb8f0b9d8f8b1964a38a6657964856baaea66d98941c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.0 MB (512008019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2c0509b956e675536faf99961931c405854d284801b023610ba3b6c1660a19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b22721db94b1c5fff4e7c6f09aa650c06de76f3b42c9ec977d76b8bf11c268`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 50.6 MB (50624136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb575aeaeee118c4f0db03d2fd601e49cd3f7cc07844c7bc2872425a446e4581`  
		Last Modified: Wed, 13 Nov 2024 15:27:10 GMT  
		Size: 167.5 MB (167519575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4061e9ce1ac5c8ce1e6c1271fd215f85fd0caebf6a11b4bf5a559a169ead00e5`  
		Last Modified: Thu, 14 Nov 2024 01:11:49 GMT  
		Size: 228.9 MB (228918662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f4c0fd57647af42bfd08c8162dfa75b9f36e0a793e947b5d3dc941013f0fdb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deef6ec419164cf481190c3102f81bf86ad0d0352e7347206b514f9fd7b48911`

```dockerfile
```

-	Layers:
	-	`sha256:a8eaf9bf0d7f500e7114791b6823f3b1b42423249f2e4cf95802db52cbe532a1`  
		Last Modified: Thu, 14 Nov 2024 01:11:45 GMT  
		Size: 14.9 MB (14900833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa22d22ca7c1e99c5fb92ba9ffd957995e50b04e0e5d965fd84e8196fded821`  
		Last Modified: Thu, 14 Nov 2024 01:11:44 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3c1b8b6487513ad4e753d008b960260f5bcc81bf110883460f6ed3cd72bf439b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570127971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c848f57e79cdedc6cd3735c641da59e5b67b257ee5e425a3bbed79e4bac60e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8ab89b79ca6b4fbc5b7006d242a238846ed57f82ebef3fc069e6bb0aa0532`  
		Last Modified: Wed, 13 Nov 2024 08:04:21 GMT  
		Size: 190.0 MB (189977453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc648336fb27f4a381de2ee878010c61a10dfff0f5076696589bb3f361cd0d`  
		Last Modified: Wed, 13 Nov 2024 16:38:36 GMT  
		Size: 256.0 MB (256007774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a55d070e2b801c4e7b3f26c4a383d1f5eddb1e4b258528e346640a42320bfccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05549fa930481c360c81fafd9e514010d1691a05f4944fe6edcd4d7d1afd2ead`

```dockerfile
```

-	Layers:
	-	`sha256:efc4fe85574fe6d885a0135708bfd7d7542ae71f6c6575075661d61cbe0231ae`  
		Last Modified: Wed, 13 Nov 2024 16:38:31 GMT  
		Size: 15.1 MB (15102584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b2c9fefb8cc2c49cbf1fbcf62430363a686afb9b8f600552b5a21c42078ae7`  
		Last Modified: Wed, 13 Nov 2024 16:38:30 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:bb93303cbbf2a6f13285a70752f54d8a38bef5bcb3062466b9e1f989017fe702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 MB (533944108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f612b8e9426a4b0877d8ab94ea3f429c9e0bf9b77f33be696a50599b2596a247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd146822c599cb06a479cc8a6b587e7e18c5d0a349e0ff98559b0f8ef702bff7`  
		Last Modified: Tue, 12 Nov 2024 05:00:40 GMT  
		Size: 205.8 MB (205777260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:57a1081dab6ba9c47e9f720f8173aede6afd9004489dd73aaf8cccc3924c05e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b58c341cb8c133e64f996d0142603f99482f576f3e5f87f06556d9ca780e2`

```dockerfile
```

-	Layers:
	-	`sha256:24739993ed260b2f5d9fed21b83b4cee87d793c1bd2be864e0f4c6e5eb64f04b`  
		Last Modified: Tue, 12 Nov 2024 05:00:36 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba69b43f8ff46a09b75e788fc87bf05a66f1f3cb8d09342462ffbc2be63eb180`  
		Last Modified: Tue, 12 Nov 2024 05:00:35 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-slim`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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

### `rust:1.82.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-slim-bookworm`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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

### `rust:1.82.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-slim-bullseye`

```console
$ docker pull rust@sha256:426a0b287a98f7410fb4d84e5401d6ea65b75689ba10954dc73fc1fcee1ae578
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

### `rust:1.82.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:46bad2a122975b3d3f7443e137015e0567bc4c63e467a818d9b92517def5f4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284233275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20005414bebc60c5e0e08412413bebf1a7a9685c7ae5411b6e0fd371eed0c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ca049328c7f2e77bd9aafe9ffb887994cf0637a356d52b36402517bb8ff41`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 252.8 MB (252781714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b24a3c097f184d33a580a49ae0f91e1f5ac1b3c79149c3cd79217d518767f2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1192d242e71bdf8d75dc252c942825e2d222c60589b4126b05d82300741bd98e`

```dockerfile
```

-	Layers:
	-	`sha256:c286e2858ed675836066788d3c16ed369b62052679d7642f2742efdad5df00b3`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 4.2 MB (4180445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8ffaaca173ca6838a3831e1eea198848e426424e8bceb80bb4731eafb5114a`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:76576a36e6ad266cccfa0044392a83b85fca6968b6f07fd76236d8603b4afb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297576818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68c6648bd2f42e819f5b39f925030ed571d2650c70c2f07280aca4f332620b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf03adada101d85359afaebfbc1d698d434dad47cf1a9dafcb16911b27c4b867`  
		Last Modified: Wed, 13 Nov 2024 06:45:26 GMT  
		Size: 271.0 MB (270967561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c575f6124afb181b7f79518350ff888d118fcbc148de5d2e0b391dab13df7b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c08ed3ad7250cd9730a1c4fb8455c796f0de9238b7b4ae900823d05fb6d7a6`

```dockerfile
```

-	Layers:
	-	`sha256:12e739030d49ed6aacd7db0ddedd88fa58c190294ad641a4ce3b5f9e5e3ef8d7`  
		Last Modified: Wed, 13 Nov 2024 06:45:20 GMT  
		Size: 4.0 MB (3989372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248b0521bdab09596cf4057ce0d64b69c8a46f51da17be753b2931a5043a6461`  
		Last Modified: Wed, 13 Nov 2024 06:45:19 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d1b01f909e5ba4510de1683935432ae49a4cc229593f2e2db5515ed7a142c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341577259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3624a5f3bf954bd9d6cbfd3daaf86be98102d31aa008ef0197e584f3fb1abdf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3a97815435189dd53bc1eb929e5332889ac83992be4a9447a0003d6cb04e6f`  
		Last Modified: Wed, 13 Nov 2024 00:32:40 GMT  
		Size: 311.5 MB (311485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fb8084595c3540aacedd7c1ce79105f1ac40be4b59940a81eafa9ec2622edf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adfc1595344e5ac0cabc50fe5884d5188f86429a0f0a0b5ecdbe65d43d9001c`

```dockerfile
```

-	Layers:
	-	`sha256:f57e0e66aad4bb0ea22da924e559e24e7f91b79738fee570bb47625815ef277f`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 4.2 MB (4177121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea60ed2a103340d5408146aac5f4caa9f1930e826771dd79d6a19aa6637b5545`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 11.5 KB (11459 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3bdeb9e24e380d38f6a23d0c9782a72e34654b369e55453c9dd16117cbdd0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298773484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c62dd3561fec89c84a360fab38b6e9e8003d483764def127392706f674a1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3673d63c7e778356d62082b73f2357833a19e623f528d8e62dac957eda0b1`  
		Last Modified: Tue, 12 Nov 2024 02:21:10 GMT  
		Size: 266.4 MB (266350133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:267b340e78c456f02251bc3627d2d7de83ef717be46dc8058590516f34fee8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5484b707a28f321ab31fe64503300cd90613dbb93744d2cac76d4130d5989177`

```dockerfile
```

-	Layers:
	-	`sha256:1bee8187641b794234139ce1a879c7fc7c8213884bc1e7a71f0cf257c38e00bb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccf11ed2511f7334e4dbabbd3d36b7bb3df5f402a672da7b8ac3616d0397aa`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:97f288e992a424decbe9615f79e3c30a00e402d9ad1c51d17b801d9101ae1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:cd6e942d21a09065bb77508e0652cad35ef32938cee4727f8e00c4ef3ae4f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291926676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52bab6d057387ec516cb502d1d9be60aaa9ae67f887fa4204ad3778c824deef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7f9aa2a63c77c6dfea9a616ba8de311167963accbb062595e525a14855dd77`  
		Last Modified: Tue, 12 Nov 2024 02:49:15 GMT  
		Size: 55.3 MB (55346808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e15e1bb1f3d07546e99251b81032a4a9038fadbf9b9ebd27e2afbf930429d`  
		Last Modified: Tue, 12 Nov 2024 02:49:19 GMT  
		Size: 233.2 MB (233160140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7dbbbafbd89f297fdf36b0e0086b8d676e024539d52d541582c9f41e063ed24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.5 KB (724455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8758812fd52c11e30054af7f1f6afd3dc1d32b6bffee934556cc4642587c469e`

```dockerfile
```

-	Layers:
	-	`sha256:30f938cb5f53250c3b423cd92520cd8df1cd4fbbc6f7610f85795ac313fbb787`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 713.7 KB (713741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ec1f9818cc762ca92550827ee60d791ab5ba54775746c16d27c288d6446876`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee73aa941f7f42a52806c7623cb5b5271b90181aa05abaf14151a2320c9491b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9fd4d3a567c83547ff5ee24912a3772e77b46a60ca37f8b1c3c499f99ef27f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebc171e95d6bf960ff3cf365c04babb4ca82931639761616e97fc9f7699ba75`  
		Last Modified: Wed, 13 Nov 2024 00:35:25 GMT  
		Size: 53.0 MB (52995408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae93b63d515bac85a5051eab1aacd3ca57f69ea278af4f11e768c8134d6c6a1`  
		Last Modified: Wed, 13 Nov 2024 00:35:29 GMT  
		Size: 241.8 MB (241799098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:45f9c9f8dc8a5dd916bf7e5e98fca928095ec5e91f383dde541787d0b64d4f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.6 KB (760560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a5caaf1b41326160ade3e1bac141e929552ae2120a7d52fa9a8bd4e1b8581`

```dockerfile
```

-	Layers:
	-	`sha256:ecc6747c67076702a78a1077b6c1658fc362defe289e25d04437932f7de077d0`  
		Last Modified: Wed, 13 Nov 2024 00:35:24 GMT  
		Size: 749.7 KB (749728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5adc7278371532a6e6c52aa5a4f51f4408fc55e2fd059c1d42c48f0eec6b3a0`  
		Last Modified: Wed, 13 Nov 2024 00:35:23 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:2f42ce0d00c0b14f7fd84453cdc93ff5efec5da7ce03ead6e0b41adb1fbe834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:01f65c4c991377411026324ba35c3c6279f42a0419c0aec27d7f6cd28af594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f93f251886ce9e4b6de080b8e8e9b76bf13be5003f817ca036e1980a851064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3526cdf812bc85e78f834ff61feb4d26ae57ce011f0157b212b6577cef81324`  
		Last Modified: Wed, 13 Nov 2024 00:36:34 GMT  
		Size: 52.9 MB (52946275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626220d818e00c1fd7c0ef48bfcbe7a88b3dd04b181ae8cf347583f60f5fc9aa`  
		Last Modified: Wed, 13 Nov 2024 00:36:39 GMT  
		Size: 241.8 MB (241799046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:88f04c5e6826ad9486046e3b922df38a1f4a3a738deed366d66a5d2a6e66e11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e0f6620ffa6ce7d31bfde708ff2c63862b75481b17ba660414fbc6fb78d55`

```dockerfile
```

-	Layers:
	-	`sha256:af6953ca23cb0961a76b4384d14d72e063cce561e0ed5627b5d3d56d3ef55baa`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 747.3 KB (747289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c78b3b3aebea426af055be170bb9b9c67455ff2e73bdd3da47ed8249d8cb5`  
		Last Modified: Wed, 13 Nov 2024 00:36:33 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:821c41ed8d70347b32c2a3e4779fa0f05354773adf627aa388d0904494e0d21f
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
$ docker pull rust@sha256:ac7fe7b0c9429313c0fe87d3a8993998d1fe2be9e3e91b5e2ec05d3a09d87128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515318572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3a03a3335d927012667a8b813477a2783f016be5e4a6ae0a648e64402f08b7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf13695a4667af089ddeff6d2392e21ee9a9600a153405de88278675194f82`  
		Last Modified: Tue, 12 Nov 2024 04:58:34 GMT  
		Size: 192.8 MB (192841813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dbf4f736b889695983fe0f74ac4895df43b1ddba6c62c09ca12b4c7042c4b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc97b7bb10c521654d8058f494bdccbbe29e6b0c72d47b53c1f54f075404c0a`

```dockerfile
```

-	Layers:
	-	`sha256:8c22210fba04d18da54e27688ea2ebc19dc1495b47987f7d8e2473f924c87de6`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 15.1 MB (15100321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834cec5d6d5bd036412098f75fdff73b866b61622fe68d26312d54769721b4be`  
		Last Modified: Tue, 12 Nov 2024 04:58:31 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:db7987a6a911e3886d3cb8f0b9d8f8b1964a38a6657964856baaea66d98941c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.0 MB (512008019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2c0509b956e675536faf99961931c405854d284801b023610ba3b6c1660a19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b22721db94b1c5fff4e7c6f09aa650c06de76f3b42c9ec977d76b8bf11c268`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 50.6 MB (50624136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb575aeaeee118c4f0db03d2fd601e49cd3f7cc07844c7bc2872425a446e4581`  
		Last Modified: Wed, 13 Nov 2024 15:27:10 GMT  
		Size: 167.5 MB (167519575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4061e9ce1ac5c8ce1e6c1271fd215f85fd0caebf6a11b4bf5a559a169ead00e5`  
		Last Modified: Thu, 14 Nov 2024 01:11:49 GMT  
		Size: 228.9 MB (228918662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f4c0fd57647af42bfd08c8162dfa75b9f36e0a793e947b5d3dc941013f0fdb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deef6ec419164cf481190c3102f81bf86ad0d0352e7347206b514f9fd7b48911`

```dockerfile
```

-	Layers:
	-	`sha256:a8eaf9bf0d7f500e7114791b6823f3b1b42423249f2e4cf95802db52cbe532a1`  
		Last Modified: Thu, 14 Nov 2024 01:11:45 GMT  
		Size: 14.9 MB (14900833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa22d22ca7c1e99c5fb92ba9ffd957995e50b04e0e5d965fd84e8196fded821`  
		Last Modified: Thu, 14 Nov 2024 01:11:44 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3c1b8b6487513ad4e753d008b960260f5bcc81bf110883460f6ed3cd72bf439b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570127971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c848f57e79cdedc6cd3735c641da59e5b67b257ee5e425a3bbed79e4bac60e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8ab89b79ca6b4fbc5b7006d242a238846ed57f82ebef3fc069e6bb0aa0532`  
		Last Modified: Wed, 13 Nov 2024 08:04:21 GMT  
		Size: 190.0 MB (189977453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc648336fb27f4a381de2ee878010c61a10dfff0f5076696589bb3f361cd0d`  
		Last Modified: Wed, 13 Nov 2024 16:38:36 GMT  
		Size: 256.0 MB (256007774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a55d070e2b801c4e7b3f26c4a383d1f5eddb1e4b258528e346640a42320bfccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05549fa930481c360c81fafd9e514010d1691a05f4944fe6edcd4d7d1afd2ead`

```dockerfile
```

-	Layers:
	-	`sha256:efc4fe85574fe6d885a0135708bfd7d7542ae71f6c6575075661d61cbe0231ae`  
		Last Modified: Wed, 13 Nov 2024 16:38:31 GMT  
		Size: 15.1 MB (15102584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b2c9fefb8cc2c49cbf1fbcf62430363a686afb9b8f600552b5a21c42078ae7`  
		Last Modified: Wed, 13 Nov 2024 16:38:30 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:bb93303cbbf2a6f13285a70752f54d8a38bef5bcb3062466b9e1f989017fe702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 MB (533944108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f612b8e9426a4b0877d8ab94ea3f429c9e0bf9b77f33be696a50599b2596a247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd146822c599cb06a479cc8a6b587e7e18c5d0a349e0ff98559b0f8ef702bff7`  
		Last Modified: Tue, 12 Nov 2024 05:00:40 GMT  
		Size: 205.8 MB (205777260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:57a1081dab6ba9c47e9f720f8173aede6afd9004489dd73aaf8cccc3924c05e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b58c341cb8c133e64f996d0142603f99482f576f3e5f87f06556d9ca780e2`

```dockerfile
```

-	Layers:
	-	`sha256:24739993ed260b2f5d9fed21b83b4cee87d793c1bd2be864e0f4c6e5eb64f04b`  
		Last Modified: Tue, 12 Nov 2024 05:00:36 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba69b43f8ff46a09b75e788fc87bf05a66f1f3cb8d09342462ffbc2be63eb180`  
		Last Modified: Tue, 12 Nov 2024 05:00:35 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:d9c3c6f1264a547d84560e06ffd79ed7a799ce0bff0980b26cf10d29af888377
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
$ docker pull rust@sha256:fc4cf6c302df3a3cb211027605fd61447cac29d873692041bd21d22c55b5b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542161226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea9ee7bf87e21c7fae8295ac0f11f22710e26469e542be2d0cf415f3b38aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83766a9c5ba751dbb37d14a7a7c3c8eb422d028bf42ebd3768c8eeec1460eef`  
		Last Modified: Tue, 12 Nov 2024 05:55:42 GMT  
		Size: 192.8 MB (192842008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:575e4f1b4327853ff4112b9a9ab639fea7980979d5d716af9d85693941ed5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db38dfc475248e74861362a9b30c57a88f3ef2ec9954ad3be3c6e166490d6bf3`

```dockerfile
```

-	Layers:
	-	`sha256:41861097c8938bbf6d9a956760c0dbc3b5237ec081c532ee7c4a22f15a4b20c8`  
		Last Modified: Tue, 12 Nov 2024 05:55:38 GMT  
		Size: 15.5 MB (15501302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b968d310ac40e246a53b19691d4799859e5ab64de42103f36c46b197ec4b96`  
		Last Modified: Tue, 12 Nov 2024 05:55:37 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:71e61026c43b612e67acebaf980ae213368f1cd5706ec5651f045022af6cbad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530913984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ba2919836c9af7787aa6dda2351dfbe16609528edd777e4af6d9e737ede19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2fc1f2113a24a2a110aaf5a4ae40ce0e157601ea6f6784faf6eb0b8936df9`  
		Last Modified: Thu, 14 Nov 2024 01:13:58 GMT  
		Size: 228.9 MB (228918576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:eae13a7155b047b8b5bcb8963793be357f231001e9a96cbcbd61aace7077dd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550ac390e7c5f8e8c78a20d4d4b1373f1ae2ca9fe3f1439b029736d096490c6`

```dockerfile
```

-	Layers:
	-	`sha256:47aaae48969084d7fe4f7841427b4d7e2235e9afd0896bea00b07b1bd7606d56`  
		Last Modified: Thu, 14 Nov 2024 01:13:53 GMT  
		Size: 15.3 MB (15305442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962bac89d8de05fa449644fb41983cdef1249a46b05a6ae7192a52ec3fca00b`  
		Last Modified: Thu, 14 Nov 2024 01:13:52 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33580ebd9ce59225f0f73cd4f88d8ea2236bd9fe5d0867c913e16aec2073da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3caeab5385e95f830d82c2c67f953a5f4838073395ecfd2ff6a03ac68b52b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fb464f40e4004f5fff10a919bcd33153996e0ec882130f780f84b38a68230b`  
		Last Modified: Wed, 13 Nov 2024 16:40:04 GMT  
		Size: 256.0 MB (256007778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:21933da7e970a83b16d5e4c54c9c1fdd53561173b5125e742fdf07cbaacbc905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d2711a99e715ba995a2123e25d38ee4b9115532e0cd6dff35d6def49dceb2`

```dockerfile
```

-	Layers:
	-	`sha256:62f581c915976ae3b128c2c535dd596599b613530f459ac35474c8e389418f8e`  
		Last Modified: Wed, 13 Nov 2024 16:39:59 GMT  
		Size: 15.5 MB (15529909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e67918c5a7e7f2757cdcb0190e467089315f901e31d185661e561847f6235`  
		Last Modified: Wed, 13 Nov 2024 16:39:58 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:852367d0018d9be704c5c4df9a89bf275e352d10a77e9af7f5b9bbbee8616307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557674518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39cacf4b2bc7e0a5e7e6f7b34a6902196c2d986e81d04636385f6b8eb676fae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba0a976980e11a538e5b1d3e16dccb6e2e44980db67607ca4e0eab4897ac741`  
		Last Modified: Tue, 12 Nov 2024 05:00:43 GMT  
		Size: 205.8 MB (205777146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:f6536ddb49f7d485c65e9771ac692f7106160d2a539185e7104c6c78d5544066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a0034a09983451613bc8283f491fb92db38f06844cea2e0c002620d43951a5`

```dockerfile
```

-	Layers:
	-	`sha256:1b3a6f357ab71eb0374bb90ad43b65c1bb8512da77759efdd295d5731ad4f1c1`  
		Last Modified: Tue, 12 Nov 2024 05:00:39 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048b488a0bdb47ce37360ea96babeb20514ee0ef4c4adb8fa234470c9b16f0f`  
		Last Modified: Tue, 12 Nov 2024 05:00:38 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:d87f1fc1699ce4268afd026535a1ed34c04f110b987f1be10bde0ac90c1680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e268081e5657b7d6c64556abfe113eb2a68e0b49fbb4d289a19d87514647d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0198e81a608fc02343d6c81cc130348a446e9ef9b91803e4580a44481adf378c`  
		Last Modified: Wed, 13 Nov 2024 06:18:21 GMT  
		Size: 252.6 MB (252582839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:43b109c28e3beb27577c6809723eb69a7711010d2dc479b73df3885cb761944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193041f0f4fbd0a3ec9215dbd05b18a52bb91be8b50d39690c5d57291766adc`

```dockerfile
```

-	Layers:
	-	`sha256:f7ee8b22e487498988d8bd0d5908ad623938d57c744fd5eae487e123e0280067`  
		Last Modified: Wed, 13 Nov 2024 06:18:10 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4918feb88dba7d80a047e53bf6ddd4baa4de8300adccd3a80789f267bf3a29dd`  
		Last Modified: Wed, 13 Nov 2024 06:18:09 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:b164f0c16d5309c17706a739fb8f7fb3e95720ca9edcd5749616532da91a96b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597405674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de50ba404c6f9b2a015d0d7504a781d72b2a6306ca282786da4fdde9be1800eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb716c9b096897ff19b9650912659236f44d57fd67de73c5e43efbab8fe4ac1`  
		Last Modified: Wed, 13 Nov 2024 12:05:08 GMT  
		Size: 278.6 MB (278608831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:bbe85f478f34763034feea44cc32fc591e7a8bfe1e100fabbb50dc78089b4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd2a450a069cb382b27e1d107d499145d8096eedd2f0303cb2534beafb34d4`

```dockerfile
```

-	Layers:
	-	`sha256:fd52613d7211210feaf3ab308cf8cc5f01d13cc791b162c21a1dfe2d9a57e5a6`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 15.3 MB (15313740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecfea8ad3195cc5ce71c4ede6118e53cf5fd5fb895663d0bb26adcca7fa64b`  
		Last Modified: Wed, 13 Nov 2024 12:05:03 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:1111c28d995d06a7863ba6cea3b3dcb87bebe65af8ec5517caaf2c8c26f38010
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
$ docker pull rust@sha256:2893c948181a4f145098f8461ba4dfc61d5b85e7f3c46d18dddc099f0d73217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292754476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2833ed20a43f85cc810338510502d0bc644da8dacee03a94e84eb9f731a84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7bb1afc6bf3ff1243a37703b04f24aa27f670988812d8abaddb6cda713de8`  
		Last Modified: Tue, 12 Nov 2024 03:17:01 GMT  
		Size: 263.6 MB (263626481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:911d1c7553d8cdad3ed926f19ec4fc884736b3adb5230a5d963002a83e1167ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d82c0a3905e1b92de97b88ba935d16d09647340ecb9f69ae3eea3f150bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4b15a346ffc5855be301468519ce460723bf51fa18f62784384f1db3fed41e`  
		Last Modified: Tue, 12 Nov 2024 03:16:56 GMT  
		Size: 4.0 MB (3961677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d9d17997eb743b5a5f40f6fe7067c942eb1e24410fb576ba90352c51fd0f87`  
		Last Modified: Tue, 12 Nov 2024 03:16:55 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:4547a4d5fc2c542fd7f87d2dc9f7e23ed25c6fd1cd4858119dfbe49680103b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b770df39e8ac4cb4345c0bc0beeda0083e800d4d3c71071878c669a7bd8188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427d71232eef3947bcbc3bf7564743b041ffe283cc970cc3052af345f1db2f`  
		Last Modified: Wed, 13 Nov 2024 06:47:24 GMT  
		Size: 276.7 MB (276742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd36a8d946285a22270538a45651a1814c7ca5ca425d1d971daa2c26b8f760d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c39703688a7ea788826717d69207212277440a246358138a194c82ebd09c7c`

```dockerfile
```

-	Layers:
	-	`sha256:ee2033491df845d1b8751c399d506c410281877080fa222528c2d58bae1b18d2`  
		Last Modified: Wed, 13 Nov 2024 06:47:18 GMT  
		Size: 3.8 MB (3777498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561a8711c5bcd71ddbb6e41627836dc77fb7bb8f4f22120267814264585d8faa`  
		Last Modified: Wed, 13 Nov 2024 06:47:17 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9928feb33d0d8e6a71d591baf2cd38a74543dc7ffefa67553c8218b8c2261da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b9b9cf33bc8933c84e1b99042945fcb34b9d511af9cc66a223aa5ff5e9edf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02197ef091919ee79b4af4f0ae56bc9d85178f4445419217fef00799f29312f0`  
		Last Modified: Wed, 13 Nov 2024 00:34:13 GMT  
		Size: 321.8 MB (321839700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a64f2e241e4374e32e259321c382464ae19a4e33516e9549caa4488035f7e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9826a27c92b569399dd8c5a40b2651e16585b05b28bc7ee25d632f577bc09f31`

```dockerfile
```

-	Layers:
	-	`sha256:e2cfc3a386ce30f87188e56fee4cd8684d7eddf47012597ae130898ec3807df7`  
		Last Modified: Wed, 13 Nov 2024 00:34:07 GMT  
		Size: 4.0 MB (3984046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c72cc06b2fc51b3fb44595113a69ef5a9aca1b8da9e14bf8eb8040d9ca015a`  
		Last Modified: Wed, 13 Nov 2024 00:34:06 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3d0031e4aaa9722d36a274513a29ae759c32150c509c2085b22967f28a70bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303524336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad205745f984e14dd262823b4c128bdde2fb6d56de2403672c3d33c26eb7df76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bab98167c34c98d1719666cdfd8c70be03bfb032bae844e2725511a9eca817`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 273.4 MB (273378886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4a99d4f6bd5c718365687d6d7a9f99f1648977be2c14cdf95929d6406fba1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9411df7a481a3113ca955405cd417eed3383722c93f7068413d653b4281d2`

```dockerfile
```

-	Layers:
	-	`sha256:c87e11afda609907b3665de5280153cf840ef677593599f8e9dde3b519403e29`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4a2a77ca715d6f6ca60a14ebe837f687c163eb7f633119b9d5832d556b3c84`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:2e14cfbb0365f6721895cef4ef100afb54bab201058a665abf325440179bf7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354472935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704096e00a8dcf4117e79d1171f7124354dd3111c9257bc50b6d76bd9ea01368`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991f3ac767497bf258cf4d8eda4e6f05f71aa5ac8aa50bf7c8070e638912c41`  
		Last Modified: Tue, 12 Nov 2024 14:46:49 GMT  
		Size: 321.3 MB (321347582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e51098e74f240116e80b66fbd0cdabac507ab3757026bd1259bba8b05117f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c788d51115cf625d27b66b64e1d1a53b86d88c8588199d085fbaccad8b878`

```dockerfile
```

-	Layers:
	-	`sha256:8e299d6bf68ecfe1095728eb14c2003ce26de12efe53c8bd352097073d283a13`  
		Last Modified: Tue, 12 Nov 2024 14:46:40 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a42d5c4ef2f2264ffaa9bc5f629c76e169c4bc25e6ebddc1d45fa6a7a9fbe2`  
		Last Modified: Tue, 12 Nov 2024 14:46:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:29169fbbc2f4a93bf34aa53e553925dc0dd82bacbab00e426f9103c863f89ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356220993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695cf49b45c261ea6e841dd2e71437837d69f636ff00fb87a1de12610f2445f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c15ad11127abef212973a42ff2714e96ad0c89a84d3b5a9df485eacf92c1b`  
		Last Modified: Tue, 12 Nov 2024 22:27:46 GMT  
		Size: 328.7 MB (328729365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a0fd115078a7cfe8bb75bc1cbc8bea6a8d1c4019661537cb3012e23fa2c3c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2010d9ed2f3f42b27ffa64f4cb42efaa41bb66f7df91e5f8b3627beb7795b33c`

```dockerfile
```

-	Layers:
	-	`sha256:19d80ba16ba589bae012b270b9854d39cc229d44446f30d4c6cb34a2c74070f6`  
		Last Modified: Tue, 12 Nov 2024 22:27:41 GMT  
		Size: 3.8 MB (3803366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99184b11f0030fe082ce5ab2a09c5b27ab26c7f1e9a04d3d33f42201b3db71eb`  
		Last Modified: Tue, 12 Nov 2024 22:27:40 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:426a0b287a98f7410fb4d84e5401d6ea65b75689ba10954dc73fc1fcee1ae578
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
$ docker pull rust@sha256:46bad2a122975b3d3f7443e137015e0567bc4c63e467a818d9b92517def5f4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284233275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20005414bebc60c5e0e08412413bebf1a7a9685c7ae5411b6e0fd371eed0c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ca049328c7f2e77bd9aafe9ffb887994cf0637a356d52b36402517bb8ff41`  
		Last Modified: Tue, 12 Nov 2024 02:21:07 GMT  
		Size: 252.8 MB (252781714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b24a3c097f184d33a580a49ae0f91e1f5ac1b3c79149c3cd79217d518767f2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1192d242e71bdf8d75dc252c942825e2d222c60589b4126b05d82300741bd98e`

```dockerfile
```

-	Layers:
	-	`sha256:c286e2858ed675836066788d3c16ed369b62052679d7642f2742efdad5df00b3`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 4.2 MB (4180445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8ffaaca173ca6838a3831e1eea198848e426424e8bceb80bb4731eafb5114a`  
		Last Modified: Tue, 12 Nov 2024 02:21:03 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:76576a36e6ad266cccfa0044392a83b85fca6968b6f07fd76236d8603b4afb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297576818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68c6648bd2f42e819f5b39f925030ed571d2650c70c2f07280aca4f332620b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf03adada101d85359afaebfbc1d698d434dad47cf1a9dafcb16911b27c4b867`  
		Last Modified: Wed, 13 Nov 2024 06:45:26 GMT  
		Size: 271.0 MB (270967561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c575f6124afb181b7f79518350ff888d118fcbc148de5d2e0b391dab13df7b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c08ed3ad7250cd9730a1c4fb8455c796f0de9238b7b4ae900823d05fb6d7a6`

```dockerfile
```

-	Layers:
	-	`sha256:12e739030d49ed6aacd7db0ddedd88fa58c190294ad641a4ce3b5f9e5e3ef8d7`  
		Last Modified: Wed, 13 Nov 2024 06:45:20 GMT  
		Size: 4.0 MB (3989372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248b0521bdab09596cf4057ce0d64b69c8a46f51da17be753b2931a5043a6461`  
		Last Modified: Wed, 13 Nov 2024 06:45:19 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d1b01f909e5ba4510de1683935432ae49a4cc229593f2e2db5515ed7a142c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341577259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3624a5f3bf954bd9d6cbfd3daaf86be98102d31aa008ef0197e584f3fb1abdf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3a97815435189dd53bc1eb929e5332889ac83992be4a9447a0003d6cb04e6f`  
		Last Modified: Wed, 13 Nov 2024 00:32:40 GMT  
		Size: 311.5 MB (311485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fb8084595c3540aacedd7c1ce79105f1ac40be4b59940a81eafa9ec2622edf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adfc1595344e5ac0cabc50fe5884d5188f86429a0f0a0b5ecdbe65d43d9001c`

```dockerfile
```

-	Layers:
	-	`sha256:f57e0e66aad4bb0ea22da924e559e24e7f91b79738fee570bb47625815ef277f`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 4.2 MB (4177121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea60ed2a103340d5408146aac5f4caa9f1930e826771dd79d6a19aa6637b5545`  
		Last Modified: Wed, 13 Nov 2024 00:32:33 GMT  
		Size: 11.5 KB (11459 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3bdeb9e24e380d38f6a23d0c9782a72e34654b369e55453c9dd16117cbdd0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298773484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c62dd3561fec89c84a360fab38b6e9e8003d483764def127392706f674a1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 17:01:39 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3673d63c7e778356d62082b73f2357833a19e623f528d8e62dac957eda0b1`  
		Last Modified: Tue, 12 Nov 2024 02:21:10 GMT  
		Size: 266.4 MB (266350133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:267b340e78c456f02251bc3627d2d7de83ef717be46dc8058590516f34fee8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5484b707a28f321ab31fe64503300cd90613dbb93744d2cac76d4130d5989177`

```dockerfile
```

-	Layers:
	-	`sha256:1bee8187641b794234139ce1a879c7fc7c8213884bc1e7a71f0cf257c38e00bb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccf11ed2511f7334e4dbabbd3d36b7bb3df5f402a672da7b8ac3616d0397aa`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json
